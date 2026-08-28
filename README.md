# zellij-claude-theme

[Zellij](https://zellij.dev) themes matching the Claude desktop app palette, in
light and dark. Warm cream or warm charcoal, near-black or bone text, terracotta
accent (`#D97757`) in both.

Both use the granular styling spec (Zellij 0.41+) rather than the legacy 8-colour
palette, so tabs render as soft chips instead of pure black blocks and the focused
pane frame is terracotta.

Pairs well with:

- Ghostty's built-in `Claude Light` and `Claude Dark` themes
- Claude Code's built-in `light` and `dark` themes (`/theme`)
- A warm-paper Neovim colorscheme such as [flexoki](https://github.com/kepano/flexoki-neovim)

## Install

Zellij auto-loads any theme file in its themes directory:

```sh
mkdir -p ~/.config/zellij/themes
curl -o ~/.config/zellij/themes/claude-light.kdl \
  https://raw.githubusercontent.com/zarifaziz/zellij-claude-theme/main/claude-light.kdl
curl -o ~/.config/zellij/themes/claude-dark.kdl \
  https://raw.githubusercontent.com/zarifaziz/zellij-claude-theme/main/claude-dark.kdl
```

Then in `~/.config/zellij/config.kdl`:

```kdl
theme "claude-light"   // or "claude-dark"
```

Restart your Zellij sessions to pick it up. To try one without editing your config:

```sh
zellij options --theme claude-dark
```

### If the theme doesn't load

Zellij 0.44.0 shipped a bug where theme files in `~/.config/zellij/themes/` were
silently ignored ([#4909](https://github.com/zellij-org/zellij/issues/4909),
[#5013](https://github.com/zellij-org/zellij/issues/5013)), fixed by
[#4892](https://github.com/zellij-org/zellij/pull/4892). If you are on an affected
version, either upgrade or paste the file's `themes { ... }` block directly into
`~/.config/zellij/config.kdl`.

## Palette

| Role | Light | Dark |
| --- | --- | --- |
| Background | `#FAF9F5` | `#262624` |
| Panel | `#F0EEE6` | `#30302E` |
| Selection | `#E8E6DC` | `#363634` |
| Foreground | `#141413` | `#E5E4E1` |
| Muted text | `#5E5D59` | `#A6A59B` |
| Accent | `#D97757` | `#D97757` |
| Focused frame | `#C15F3C` | `#D97757` |
| Success | `#788C5D` | `#9ACA86` |
| Error | `#C15F3C` | `#D47563` |

The dark values come from Ghostty's built-in `Claude Dark` theme, so the two match
when Zellij runs inside Ghostty.

## Licence

MIT. "Claude" and "Anthropic" are trademarks of Anthropic, PBC. This is an
unofficial community theme, not affiliated with or endorsed by Anthropic.
