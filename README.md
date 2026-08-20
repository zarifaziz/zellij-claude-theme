# zellij-claude-theme

A [Zellij](https://zellij.dev) theme matching the Claude desktop app's light palette:
warm cream background (`#FAF9F5`), near-black text (`#141413`), terracotta accent (`#D97757`).

Pairs well with:

- [ghostty-claude-theme](https://github.com/zanehu-ai/ghostty-claude-theme) for Ghostty
- Claude Code's built-in `light` theme (`/theme` → light)
- A warm-paper Neovim colorscheme such as [flexoki](https://github.com/kepano/flexoki-neovim)

## Install

Zellij auto-loads any theme file in its themes directory:

```sh
mkdir -p ~/.config/zellij/themes
curl -o ~/.config/zellij/themes/claude-light.kdl \
  https://raw.githubusercontent.com/zarifaziz/zellij-claude-theme/main/claude-light.kdl
```

Then in `~/.config/zellij/config.kdl`:

```kdl
theme "claude-light"
```

Restart your Zellij sessions to pick it up.

## Palette

| Role | Hex |
| --- | --- |
| Background | `#FAF9F5` |
| Foreground | `#141413` |
| Accent (orange) | `#D97757` |
| Selection | `#E8E6DC` |

"Claude" and "Anthropic" are trademarks of Anthropic, PBC. This is an unofficial community theme.
