<h2 align="center">Catppuccin for lich</h2>

<p align="center">Soothing pastel theme for the high-spirited</p>

<p align="center">
    <a href="https://github.com/catppuccin/catppuccin">
        <img src="https://img.shields.io/badge/community-catppuccin-cba6f7?labelColor=1e1e2e&style=for-the-badge" />
    </a>
</p>

## Usage

1. Open lich → **Settings → Appearance → Import**.
2. Paste the repository URL: `https://github.com/omartelo/catppuccin-lich`
3. Click **Install**.
4. Pick a flavor in the theme picker. The terminal picker defaults to
   **Match app theme**, so one pick dresses both — or choose a different flavor
   there if you want the panes to differ.

To take a later release, hit **Update** on the theme's row.

### Local install

An absolute path is an accepted remote, so a clone installs the same way:

```bash
git clone https://github.com/omartelo/catppuccin-lich.git
```

Then paste the absolute path of the clone into **Settings → Appearance → Import**.

## Flavors

| Theme | `id` | `scheme` |
|---|---|---|
| Catppuccin Latte | `catppuccin-latte` | light |
| Catppuccin Frappé | `catppuccin-frappe` | dark |
| Catppuccin Macchiato | `catppuccin-macchiato` | dark |
| Catppuccin Mocha | `catppuccin-mocha` | dark |

## Thanks to

- [omartelo](https://github.com/omartelo) — port author
- [Catppuccin contributors](https://github.com/catppuccin) — original palette

## Contributing

Each flavor is one lich theme file — `catppuccin-latte.json`,
`catppuccin-frappe.json`, `catppuccin-macchiato.json`, `catppuccin-mocha.json`
— beside the `lich-theme.json` manifest that carries the pack's version.
Colors are mapped by role from the official palette (`base`/`mantle`/`crust`,
`surface0-2`, `overlay0-2`, `subtext0-1`, `text`, and the accent colors) and
edited directly in the theme files — there is no lich exporter in the official
[`catppuccin/palette`](https://github.com/catppuccin/palette) tooling.

To propose a tweak:

1. Fork the repo.
2. Edit the relevant flavor file.
3. Validate the **whole directory** — a repository installs all or nothing:
   `node validate.mjs .` (ships with the lich `theme` skill).
4. Bump `version` in `lich-theme.json` in the same commit. An unbumped version
   ships nothing: **Update** compares only that number.
5. Open a PR.

Palette reference: [catppuccin/palette](https://github.com/catppuccin/palette).

## License

[MIT](./LICENSE)
