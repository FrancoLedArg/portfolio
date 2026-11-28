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
The ASCII intro that plays on the **Screen** before the **Dashboard**, styled like an old machine powering on.
_Avoid_: Intro, loader, splash

**Plain View**:
The same portfolio content without the **Screen Effect** or the editor UI, readable by recruiters, screen readers and crawlers.
_Avoid_: Fallback, lite mode, accessible version

## The editor UI

**Dashboard**:
The start screen shown after the **Boot Sequence**: a big ASCII logo, a menu of single-key entries and a footer line, modelled on LazyVim's own start screen.
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
The sidebar showing the portfolio content as a file tree.
_Avoid_: Sidebar, file tree, navigator

**Statusline**:
The bar along the bottom of the **Screen** showing the mode, the active **Buffer**, the cursor position and a help hint.
_Avoid_: Status bar, footer

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
The identity content: name, role, location, availability, contact, skills and an ASCII portrait.
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
