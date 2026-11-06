# Native hex package provenance

Maintained repository: https://github.com/CrispStrobe/madedit2
Branch: `feature/crispcloud-hex-package`
Package path: `packages/madedit2_hex`

Upstream: https://github.com/madedit/madedit2
Upstream revision: `288d35747faccb1cb997c4a30afc40c6cb48b0ae` (v1.0.2), MIT.
The original copyright and permission notice are retained in LICENSE.

Initial implementation and regression suites copied from
`CrispStrobe/CrispCloud` at `bf12c3ac97526d2fd33a70b38148fa86c097db47`.
This preserves the existing integration work rather than restarting it.

`lib/hex_layout.dart` adapts the byte-column layout, offset and nibble helpers
from upstream `lib/editor/hex_view.dart`. The embeddable Flutter widget,
serialized controller and persistent byte-only AVL document are integration
code, not an unchanged upstream widget. The storage adapter stays in CrispCloud,
where account identity and save policy belong.

This package deliberately omits text newline indexing, encoding-aligned byte
mutations, global application settings, Rust, scripting and Tree-sitter. The
complete MadEdit2 application remains separate and unchanged by the extraction.

Consumers should pin an immutable commit and the package subdirectory rather
than depending on a moving branch. No changes have been merged to main.
