# PROTOTYPE: Keymap picker (throwaway)

Answers issue #7: which vim keys and mouse actions does the editor support?

Open `index.html` in a browser (it is also published as a private artifact). Rows can be ticked or unticked, and the Screen only responds to the ticked keys. A key log shows what each key did.

**Verdict:** the rows locked as "decided #7" (plus the ones decided in #3–#6 and ADR 0001) are the keymap. Every row left unlocked is out: `gg G`, `w b e`, `0 $`, `Ctrl-d/u`, `{ }`, number prefixes, `␣ b d`, Explorer keyboard focus, `␣ f f`, `f` in a Buffer, `n N`, Ctrl/Cmd+F, `:<number>` and a separate address per Buffer. `Esc` closes whatever is open first, then goes back to the Dashboard with Buffers kept open. Notifications fade after about 5 seconds or close on click. The full decision is on issue #7.

Not production code: plain HTML, no canvas or Screen Effect, example content.
