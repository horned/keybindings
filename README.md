# Keybindings Hub

A single-page reference for terminal power users collecting the shortcuts I reach for the most in Neovim, LunarVim, Lazygit, Lazydocker, and tmux. The site pairs quick-access hero sections with tabular cheat sheets so you can glance key combos without digging through multiple docs.

## Getting Started
- Open `index.html` directly in a browser for a fast offline reference.
- Or run a local server (e.g. `python3 -m http.server 4173`) to test anchor navigation and responsive layouts on mobile.

## What’s Inside
- **Neovim Essentials** – core movement, editing, visual, window, search, and misc commands.
- **LunarVim Essentials** – leader-based Telescope, LSP, completion, and config helpers tuned to the default LVim profile.
- **Lazygit** – staging, navigation, and workflow cards mirroring the tool’s panel layout.
- **Lazydocker** – container monitoring, log tailing, and context refresh shortcuts.
- **tmux** – session, window, pane, and copy-mode operations with a persistent prefix badge.

Each section ships with an introductory hero, focused tips, and a grid of tables so related shortcuts stay visually grouped. DaisyUI themes and Tailwind utility classes keep styling lightweight while remaining easy to extend—duplicate a card block to add your own mappings.

## Contributing
1. Update `index.html`; keep cards in pairs (`md:grid-cols-2`) and prefer semantic headings.
2. Verify anchor links and hero buttons target the new section.
3. Reload in the browser (or `python3 -m http.server`) to ensure tables wrap cleanly.
4. Submit a PR describing which editor/tool you touched and include screenshots if the layout changed.

Feel free to open issues for missing categories or shortcuts you’d like to see highlighted next.
