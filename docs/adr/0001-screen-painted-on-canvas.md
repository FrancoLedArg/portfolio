# The Screen is painted onto a canvas and run through shaders

The **Screen Effect** has to match the React Bits Texture Lab reference: curved glass, scanlines, bloom, a rolling band and flicker. A shader can only process pixels, not live HTML text. So the editor UI is painted as a character grid onto a `<canvas>`, the way terminals draw text, and that picture goes through the Texture Lab **bloom** and **CRT** shaders, adapted from React Bits. A clickable prototype (branch `prototype/screen-effect`) made the CSS-only overlay look clearly worse by comparison.

## Considered options

- **HTML text with CSS/SVG overlays.** Text stays selectable and readable by screen readers, but there's no real curvature or bloom. The #2 mockup used this, and it fell short of the reference.
- **HTML-in-Canvas** (`<canvas content="drawable">`, `drawElementImage`). This would feed live HTML to a shader, but in Nov 2026 it was a Chrome origin trial only, with the API still changing. Safari and Firefox had nothing, and clicks wouldn't line up under a non-affine warp.
- **SVG `feDisplacementMap` on HTML for fake curvature.** It's slow, especially in Firefox and Safari, and it blurs text. Hit-testing ignores filters, so clicks miss near the edges.

## Consequences

- Text on the **Screen** can't be drag-selected, found with Ctrl+F, or read by screen readers. The **Picker** covers search, `yy` copies a line, links and emails are clickable, and the **Plain View** (real HTML) serves screen readers, crawlers and LLMs.
- Clicks are mapped through the same `warp()` as the CRT shader, so they land on the right character cell even near the curved edges.
- The letters are drawn by our own small grid painter, not xterm.js. The React **Editor** decides what goes in each cell, and the painter draws it. Block and box-drawing characters are drawn as shapes, so the logo has no gaps between rows.
- Settings start from the Texture Lab `style.json`, with **curvature 0.15** instead of 0.18:
  - CRT: scan 0.35, mask none, glow 0.25, vignette 0.45, flicker 0.15, roll 0.25.
  - Bloom: threshold 0.25, intensity 0.9, radius 0.75.
- There is no ASCII effect layer anywhere. It turns text into unreadable mush, and the editor is already made of characters.
- With the system's "reduce motion" setting on, flicker and the rolling band are dropped, and curvature, scanlines and glow stay. `:set nocrt` and `:set crt` turn the whole effect off and on, with a **Notification**.
- Without WebGL2, the **Screen** shows the same painted editor with no effect, and the **Plain View** is still available.
- License: React Bits is MIT + Commons Clause. Ported shader files must keep David Haz's copyright and license notice. The shaders must not be published as a standalone reusable effect, library or pack.
