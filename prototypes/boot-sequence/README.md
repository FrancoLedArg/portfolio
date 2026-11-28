# PROTOTYPE: Boot Sequence and power-off (throwaway)

Answers issue #8: what does the **Boot Sequence** look like, how long does it run, and what happens on quit?

Open `index.html` in a browser (it is also published as a private artifact). The Screen is painted onto a canvas and run through the bloom and CRT shaders from the #3 prototype (© 2026 David Haz, MIT + Commons Clause; see the header in `index.html`). Extra "tube" settings in the CRT shader squash the picture into a line or a dot for the power-on and power-off.

Switches compare the round 1 options: Q1 steps (no name banner / small badge / name banner), Q2 first-visit length (5–7s / 3–4s / always ~1s), first vs return visit, and reduce motion. A timeline under the Screen shows each step and where the boot is.

A **Screen content** panel freezes the Screen on any step and edits what it shows (self-test lines, banner, login, command).

**Verdict:** six steps with the name banner (Q1 c). The full boot (about 8.5s, self-test about 3.5s) plays on every visit and after every power-on, with no short version. Any key, click or tap skips it. Reduce motion means no boot. Power-off as shown. English only, on `/es` too. The `CT` object in `index.html` holds the final content; the real site works out the version (v26) and uptime from Franco's birth date. Not chosen: the calm boot, the dot power-on, the compact letters, the corner badge and the shorter lengths. The full decision is on issue #8.

Not production code: Dashboard entries only show a Notification, no tests.
