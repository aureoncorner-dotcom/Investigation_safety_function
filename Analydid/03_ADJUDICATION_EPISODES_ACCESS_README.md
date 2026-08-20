# Episode-mapping access copies

The frozen `03_ADJUDICATION_EPISODES.csv` is retained unchanged. It is about 54 MB because it contains 13,309 member-record rows and repeats exact episode text on each membership row.

For ordinary viewing:

- `03_ADJUDICATION_EPISODES_COMPACT.csv` contains one row per canonical episode: 3,088 rows. It preserves episode/node IDs, provenance, typed missingness, source families, response/repair nodes, and exact initial/correction/repair text, while omitting member-record repetition.
- `03_ADJUDICATION_EPISODES_COMPACT_BY_CASE/` contains the same compact view split into 24 case files.
- `03_ADJUDICATION_EPISODES_BY_CASE/` contains the full member-record mapping split into 24 case files when record-level membership is needed.
- `03_ADJUDICATION_EPISODES_ACCESS_SHA256.csv` records byte counts and SHA-256 hashes for every accessibility copy.

These are supplemental access representations. They do not replace or modify the released frozen mapping or its release manifest.
