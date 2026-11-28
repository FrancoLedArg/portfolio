# PROTOTYPE: Mobile layout (throwaway)

Answers issue #10: how does the editor work on a phone?

Open `index.html` in a browser (it is also published as a private artifact). It works best on a real phone, where the Screen fills the page. The Screen is painted onto a canvas and run through the bloom and CRT shaders from the #3 prototype (© 2026 David Haz, MIT + Commons Clause; see the header in `index.html`). A pill at the bottom flips between three layouts: A) Pocket Neovim, B) Dashboard as the menu, C) Plain View on phones. Options switch the Screen Effect (full / lighter / off) and how the Self-test fits a narrow Screen.

**Verdict:** A) Pocket Neovim, as tuned in version 4. A **Tap Bar** at the bottom (Files, Find, Keys, `:`, Home; icon above label, equal widths, the selected one marked by an orange icon only), the Explorer as a drawer, one Buffer at a time with swipe to switch, page content 2 characters in from the glass edges while the bars run edge to edge, 13px text, slim line numbers, a smaller FRANCO logo on the Dashboard, the smaller font for the whole boot, and the full Screen Effect with no automatic drop. Not chosen: B, C, the lighter effect and the shorter dot leaders. The full decision is on issue #10.

Not production code: example content, no tests. Layouts B and C are kept only as the record of what was compared.
