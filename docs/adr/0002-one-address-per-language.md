# One address per language, with the Plain View built into it

The portfolio has exactly two pages: `/` (English) and `/es` (Spanish). There is no page or link for a single **Project**, **Role** or other content file. If someone wants to show a Project, they share the portfolio and the visitor browses to it on the **Screen**. Landing in the **Plain View** by accident would skip the whole experience, and forwarding a single project is rare for a portfolio like this one.

So the **Plain View** is not a separate set of pages. Each of the two pages holds the full portfolio content as one plain HTML text page, built by Astro at build time, under the **Screen**:

- While the **Screen** runs, the text is hidden from sight but stays readable to screen readers and crawlers. The first Tab press shows a "Skip to Plain View" link.
- With JavaScript off, the text is all the visitor sees.
- `:plain` hides the **Screen** and shows the text on the same address. The print stylesheet applies to it.

## Considered options

- **One Plain View page per content file** (`/projects/<slug>`, with a `.md` copy next to each). This gives shareable and indexable links, but a visitor from Google or a forwarded link lands in the Plain View instead of on the Screen.
- **Every content address opens the Screen** on that **Buffer**, then switches the address back to `/`. This avoids landing in the Plain View, but it's still a way to link to a single Project, which isn't wanted.

## Consequences

- Google indexes only `/` and `/es`. The sitemap lists those two, each pointing to the other as its language twin.
- AI tools get all the content from one file, `/llms.txt`: English, with a line pointing to `/es`. There's no `llms-full.txt` and no per-file `.md` copies, since those would be per-Project addresses again.
- `robots.txt` allows every crawler, AI crawlers included, and blocks only `cv.pdf`, which may carry a phone number or address.
- The link preview uses one picture of the **Dashboard** per language with the CRT look. It's the only image file in the project, and it never shows on the Screen or in the Plain View.
- This matches #7: the **Screen** never changes the address, and the Back button leaves the site.
