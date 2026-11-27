# gororoba-documents-public

Research papers used across the gororoba workspace (gororoba-quantum,
gororoba-open, math) whose license permits redistribution: a Creative
Commons license, CC0, the Apache License 2.0, the OSA Open Access License,
the Project Gutenberg License, a free-software or free-documentation
license (the GNU General Public License, the GNU Lesser General Public
License, the GNU Free Documentation License, the Open Publication License),
or public-domain status (including works of
the United States Government under 17 U.S.C. 105 and United States patent
documents that carry no copyright notice). Each file keeps its own
license; this repository adds no license of its own to any paper, and every
reuse follows the license the file's row names, including its attribution,
NonCommercial, NoDerivatives and ShareAlike terms.

## Layout

Every document sits at `<field>/<subject>/<file>`. [TAXONOMY.md](TAXONOMY.md) holds the fields, the subject slugs
with their scope rules and precedence, the kinds, the filename rules and the rule for adding a subject. The private sibling
gororoba-documents-private files its documents under the same vocabulary. A Markdown transcription sits beside the
PDF it transcribes, under the same stem with `.md`.

`manifest.tsv` lists every file with the columns `sha256`, `bytes`, `path`, `source_url`, `license`,
`license_evidence` and `kind`, sorted by path. Verify the checkout with

    awk -F'\t' 'NR > 1 { print $1 "  " $3 }' manifest.tsv | sha256sum -c --quiet

That command checks the bytes of every listed file; it does not check sizes, unlisted files or the vocabulary.

The evidence column names the metadata record (an exact-version arXiv abstract page, or a Crossref
version-of-record license entry with its URL, start date and record digest), the repository license and file path
that cover the file, or the license statement and its page inside the PDF. `LICENSES/` carries the license texts that the
files under those licenses require: `Apache-2.0.txt`, `GPL-2.0.txt`, `GPL-3.0.txt`, `LGPL-3.0.txt`, `GFDL-1.3.txt`,
`linux-COPYING-v6.12.txt` with `linux-syscall-note-v6.12.txt` (the Linux kernel documentation files), and
`rocq-doc-LICENSE-V9.3.0.txt` (the Rocq reference manual, which holds the Open Publication License v1.0).

## Resolving a document

Tools find a file by its sha256 through `manifest.tsv`, so a move only
updates the file's manifest row:

- gororoba-quantum: `"$PYTHON" scripts/fetch_source_cache.py --missing
  --from-documents ../gororoba-documents-private --from-documents
  ../gororoba-documents-public` restores `docs/local_source_cache/`, admitting a
  file only when its sha256 and size match `docs/SOURCES.json`, and
  `"$PYTHON" scripts/source_reading_copies.py --locate
  ../gororoba-documents-public ../gororoba-documents-private` refreshes the
  links of `docs/sources/reading-copies.md`.
- gororoba-open: cites documents by their `manifest.tsv` sha256, and their
  bytes live only in the documents repositories.
