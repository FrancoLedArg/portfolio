# Portfolio

Franco's personal portfolio: a single **Screen** that looks like an old CRT monitor running a LazyVim-style editor, where the portfolio content is browsed the way you'd browse a project in Neovim.

## The Screen

**Screen**:
The whole browser viewport, presented as the glass of an old CRT monitor. There is no monitor object or bezel; the viewport *is* the glass.
_Avoid_: Monitor, frame, canvas

**Screen Effect**:
The CRT look laid over everything on the **Screen**: curved glass, scanlines, glow, bloom, vignette, a slow rolling band and a faint flicker.
_Avoid_: Filter, shader, texture

**Boot Sequence**:
The intro that plays on the **Screen** before the **Dashboard**, styled like an old machine powering on: the CRT power-on, the **Self-test**, a name banner, a login that types itself, and `nvim`.
_Avoid_: Intro, loader, splash

**Self-test**:
The joke BIOS check in the **Boot Sequence** that "loads" Franco as if he were a machine, one line per trait, ending with `Mounting ~/franco`.
_Avoid_: BIOS screen, POST, boot log

**Power-off**:
The CRT shutdown played when the visitor quits: the picture collapses to a line, then a dot, then the **Screen** waits for a key to play the **Boot Sequence** again.
_Avoid_: Quit animation, shutdown, exit

**Plain View**:
All the portfolio content as one plain text page, without the **Screen Effect** or the editor UI, readable by recruiters, screen readers and crawlers. It is built into the same page as the **Screen** (`/` and `/es`), not a separate address: hidden while the Screen runs, shown with JavaScript off or after `:plain`.
_Avoid_: Fallback, lite mode, accessible version

## The editor UI

**Dashboard**:
The start screen shown after the **Boot Sequence**: the FRANCO block logo (the only ASCII art on the site, shared with the Boot Sequence banner), a menu of single-key entries and a footer line, modelled on LazyVim's own start screen.
_Avoid_: Splash, home, landing, welcome screen

**Editor**:
The main area of the **Screen** after the **Dashboard**, showing the active **Buffer**.
_Avoid_: Viewer, content pane

**Buffer**:
One content file opened in the **Editor**.
_Avoid_: Page, document, tab

**Buffer Tabs**:
The row across the top of the **Screen** listing the open **Buffers**.
_Avoid_: Tabs, bufferline

**Explorer**:
The sidebar showing the portfolio content as a file tree. On phones it slides in as a drawer from the **Tap Bar**.
_Avoid_: Sidebar, file tree, navigator

**Statusline**:
The bar along the bottom of the **Screen** showing the mode, the active **Buffer**, the cursor position and a help hint.
_Avoid_: Status bar, footer

**Tap Bar**:
The row of five buttons along the bottom of the **Screen** on phones (Files, Find, Keys, `:`, Home), standing in for the keys.
_Avoid_: Tab bar, nav bar, bottom nav

**Which-key**:
The help popup that lists what each key does after pressing Space.
_Avoid_: Help menu, cheatsheet, keymap

**Picker**:
The fuzzy-search popup over all portfolio content.
_Avoid_: Search, finder, command palette

**Command Line**:
The popup where `:` commands are typed.
_Avoid_: Console, terminal, cmdline

**Notification**:
A short message that appears in the top-right corner of the **Screen**.
_Avoid_: Toast, alert, popup

## Portfolio content

**Whoami**:
The identity content: name, role, location, availability, contact and skills. Text only: no portrait or picture of any kind.
_Avoid_: About, bio, profile

**Project**:
Something Franco built.
_Avoid_: Work, repo

**Role**:
A position Franco has held. Exactly one **Role** can be current.
_Avoid_: Job, experience

**Milestone**:
A dated career event: education, certification or talk.
_Avoid_: Event, achievement

**Extra**:
A hobby, side quest or ongoing tinkering.
_Avoid_: Hobby, misc
