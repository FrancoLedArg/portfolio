# PROTOTYPE: Screen Effect (throwaway)

Answers issue #3: should the Screen be painted onto a canvas and run through real shaders, or stay HTML with CSS overlays?

Open `index.html` in a browser (it is also published as a private artifact). The editor is painted as a character grid onto a 2D canvas, then run through the bloom and CRT shaders adapted from React Bits Texture Lab (© 2026 David Haz, MIT + Commons Clause; see the header in `index.html`).

**Verdict:** the shader version won clearly over the CSS overlay. Keep the `style.json` values with curvature 0.15. No ASCII effect layer. Recorded in `docs/adr/0001-screen-painted-on-canvas.md` on main.

Not production code: no tests, no hidden HTML copy, simplified ASCII port.
