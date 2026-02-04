<div align="center">
    <h1>Segfault.</h1>
    <p>A deliberately simplistic Hugo theme for command-line connoisseurs.</p>
</div>

# Installation

The theme is intended to be used as a Git submodule.

From your Hugo site root:
```sh
git submodule add https://github.com/inverted-tree/segfault.git themes/segfault
```

Then enable the theme in `hugo.toml`:
```toml
theme = "segfault"
```

# Customization options

## Basic configuration

A minimal recommended configuration looks like this:
```toml
theme = "segfault"
copyright = "Your Name"

[params]
launchYear = 2025
subtitle = [
  "Welcome to my Hugo site.",
  "Here I talk about my interests."
]
footer = "Set some footnote to your site"
```

- `launchYear` is used for copyright year ranges in the footer.
- `subtitle` renders as a multi-line site description.
- `footer` is optional text shown above the copyright line.

## QR code in the footer

The theme can optionally display a QR code (or any image) in the footer.

1. Place your QR code image in the site’s `static/` directory (for example: `static/img/qr-code.svg`).
2. Enable it in `hugo.toml`:
```toml
[params]
qrCode = "./img/qr-code.svg"
qrText = "scan for segfault"
```

- `qrCode` is the path to the image, relative to the site root.
- `qrText` is used as the image title and accessibility text.

**Note:** If `qrCode` is not set, the QR code is not rendered.

## License page

The theme includes a dedicated license page that can render the contents of a license file automatically.

1. Place your license file in the `assets/` directory (for example: `assets/LICENSE`).
2. Configure the path in hugo.toml:
```toml
[params]
license = "./LICENSE"
```

**Note:** The license file will be rendered verbatim on the `/license/` page. 
If the option is not set, the page will fall back to its content.
