---
title: "Migrating the Blog from fastpages to Quarto"
description: An AI-assisted migration of this blog off fastpages and onto Quarto, done end-to-end by Claude Code.
date: '2026-07-14'
categories:
- quarto
- meta
toc: true
---

::: {.callout-important}
## This entire post was written by Claude Code

Everything below — the words in this post, and all of the migration work it describes — was written and carried out by [Claude Code](https://claude.com/claude-code), an AI coding assistant, working from Atun's instructions. This isn't Atun's writing or voice. It's here as an accurate, dated record of what changed on this site and why, so future-Atun (or anyone else digging through the repo history) has the full story in one place.
:::

# Summary

fastai has been asking fastpages users to [migrate to Quarto](https://nbdev.fast.ai/tutorials/blogging.html#migrating-from-fastpages) for a while now, and this blog was still running the old Jekyll-based fastpages setup from 2020. I migrated it: same content, same posts, same URLs (via redirects), new engine underneath.

# What changed

The mechanical part followed fastai's own migration guide:

- Installed Quarto and scaffolded a fresh `website:blog` project
- Copied the six existing notebooks and one hand-written markdown post into `posts/`
- Ran `nbdev-migrate`, which automatically rewrote each post's frontmatter into Quarto's format, added `aliases` so the old fastpages URLs (like `/jupyter/covid-19/altair/2020/04/02/covid-19-dataset`) keep resolving, and converted the old Jekyll YouTube shortcodes into Quarto's native video-embed shortcode
- Restored the real site title, description, and bio from the old `_config.yml` and `_pages/about.md`, rather than leaving Quarto's scaffold placeholders in place
- Fixed a handful of things the automated tool doesn't touch: a couple of `draft`/`search` flags that came through as quoted strings instead of real YAML booleans, and five leftover `{{site.baseurl}}` Jekyll tags in the very first post that had to be pointed at the right relative image paths by hand
- Removed the old Jekyll scaffolding entirely — `_notebooks`, `_posts`, `_layouts`, `_includes`, `Gemfile`, `Makefile`, the fastpages GitHub Actions workflows, all of it. The repo is Quarto-only now.

# The one post that fought back

Every post rendered cleanly except one: the [Covid-19 county map](2020-04-02-covid-19-dataset.html). Two separate problems, stacked:

1. **The chart itself was dead weight.** It had been saved back in 2020 through classic Jupyter's RequireJS-based chart embedding, which Quarto's site doesn't load. The real fix wasn't a config tweak — it was letting Quarto re-execute the notebook and generate the chart natively.
2. **Re-executing it exposed two more problems.** The notebook's Minnesota county boundary data lived at a GitHub URL that no longer exists — a plain 404, six years of link rot. And the notebook's own code used pandas and Altair APIs (`DataFrame.append`, `selection_single`) that have since been removed from both libraries.

Rather than paper over this or quietly leave the chart broken, I:

- Sourced Minnesota's 87 counties from [`us-atlas`](https://github.com/topojson/us-atlas), a topojson dataset that's actually maintained, pruned it down to just the ~21KB Minnesota needs, and bundled it directly into the repo — so the post no longer depends on someone else's GitHub repo staying alive
- Updated the handful of pandas/Altair calls to their modern equivalents (`pd.concat`, `selection_point`) without changing what the chart actually shows
- Verified it in a real browser: the map renders, the county click-to-filter interaction works, and the linked bar chart updates correctly

