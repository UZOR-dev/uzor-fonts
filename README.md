# uzor-fonts (heavy fonts)

The two large fonts that [uzor](https://github.com/UZOR-dev/uzor) can embed. They are kept out of the
`uzor-fonts` crate on crates.io, which stays light by default. A build that turns on the crate's
`color-emoji` or `cjk` feature downloads the file from here and checks its SHA-256. Offline builds and
docs.rs can set `UZOR_FONTS_DIR` to a directory that holds these files instead.

| file | bytes | sha256 | font |
|---|---|---|---|
| `NotoColorEmoji.ttf` | 10,673,480 | `72a635cb3d2f3524c51620cdde406b217204e8a6a06c6a096ff8ed4b5fd6e27b` | Noto Color Emoji 2.051 (noto-emoji 20250818, Google) |
| `NotoSansCJKsc-Regular.otf` | 16,437,364 | `2c76254f6fc379fddfce0a7e84fb5385bb135d3e399294f6eeb6680d0365b74b` | Noto Sans CJK SC Regular 2.004 (Adobe) |

Upstream: [googlefonts/noto-emoji](https://github.com/googlefonts/noto-emoji) and
[notofonts/noto-cjk](https://github.com/notofonts/noto-cjk) (`Sans/OTF/SimplifiedChinese`). These are
the same bytes that uzor-fonts up to 1.5.6 downloaded from uzor's old `fonts-v1` release.

URLs that uzor's build script uses, pinned to a commit of this repo:

    https://raw.githubusercontent.com/UZOR-dev/uzor-fonts/<commit>/NotoColorEmoji.ttf
    https://raw.githubusercontent.com/UZOR-dev/uzor-fonts/<commit>/NotoSansCJKsc-Regular.otf

Never rewrite this repo's history: published uzor-fonts versions point at its commits. To change
a font, add it as a new file, or replace it in a new commit, then update the URL and hash in
uzor-fonts' `build.rs`.

## License

Both fonts are licensed under the SIL Open Font License 1.1 (see `OFL.txt`).
