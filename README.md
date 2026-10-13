# anisha-ahuja-site

Portfolio and dissertation site for Anisha Ahuja. Live at https://anisha-ahuja-site.pages.dev (Cloudflare Pages, auto-deploys from `main`).

## How to edit (for people and for Claude)

- The whole site is ONE file: `index.html`. No build step, no frameworks. CSS and JavaScript are inline; the 11 images are embedded as base64 data URIs.
- Commit a change to `main` and Cloudflare redeploys in about a minute.

### Layout of index.html

1. `<main id="view-home">` is the Portfolio page. Sections in order: hero, About (`#about`), Research threads, Teaching & experience, Consulting (`#consulting`), Publications teaser (`#publications`), Grants & awards, Dissertation feature panel, From the archive gallery, A long spectralization timeline.
2. `<main id="view-d">` is the Dissertation site. One `<article class="page" id="p-...">` per page: overview, intro, method, ch1-ch4, conclusion, sources, committee, credits.
3. `<main id="view-p">` is the Publications site. One `<article class="page" id="pp-...">` per page.
4. The `<script>` at the bottom holds a `sites` object listing every page for the dissertation (`d`) and publications (`p`) sidebars. To add a page: add an entry there AND an `<article>` with the matching id. Entries with `head:true` get collapsible sub-pages beneath them.

### House rules

- Colours are CSS variables on `:root` (light) with dark-mode overrides. The palette is sampled from the dissertation's own figures; the Image credits page shows the swatches.
- Only public-domain, open-access, or Anisha's own images are used. Do not add film, TV, Air India or other third-party stills without her explicit decision. Every image gets a caption and a line on the Image credits page.
- Panels with a dark background (`.feature`) use fixed ivory text, not the theme variables.
- Keep summaries of the dissertation faithful to the text; paraphrase rather than quote at length.
