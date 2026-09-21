# Real Transparent Discord

Black, semi-transparent Discord theme — your wallpaper subtly shows through while text and images stay crisp. Uses version-proof selectors (no class-hash chasing) and zero remote `@import`s.

## Preview

- App background: black at 70% opacity (`rgba(0,0,0,0.3)`)
- Menus + settings: slight darkening + 6px blur
- Profile colors, badges and server images are preserved

## Install (Vencord)

1. Open Discord Settings → Vencord → **QuickCSS**
2. Paste the contents of `quickCss.css`
3. Reload Discord with `Ctrl+R`

## Requirements

- **Vencord** installed
- Settings → Vencord → **Transparent** enabled (transparent window)
- On Linux, launch Discord with this flag so the window can be transparent:
  `discord --enable-transparent-visuals`

## Customize

| What | Where |
|---|---|
| Background opacity | `.appMount__51fd7` → `rgba(0,0,0,0.3)` |
| Menu/settings tint | `[role="menu"], [role="dialog"]` → `rgba(0,0,0,0.5)` |
| Blur amount | `backdrop-filter: blur(6px)` |

## How it works

- A single rule makes all backgrounds transparent; profiles (`userProfile`), banners and images are excluded
- Menu/settings selectors rely on the `role` attribute — they keep working when Discord renames its classes

## License

MIT
