# gororoba-documents-public

Research papers used across the gororoba workspace (gororoba-quantum,
gororoba-open, math) whose license permits redistribution: a Creative
Commons license, CC0, public-domain status, or another license that grants
redistribution (the Project Gutenberg License). Each file keeps its own
license; this repository adds no license of its own to any paper, and every
reuse follows the license the file's row names, including its attribution,
NonCommercial, NoDerivatives and ShareAlike terms.

## Layout

- `pdf/` holds the unchanged PDFs under readable names.
- `manifest.tsv` lists every file with the columns `sha256`, `bytes`, `path`,
  `source_url`, `license` and `license_evidence`, sorted by path. The
  evidence names the metadata record (an exact-version arXiv abstract page or
  a Crossref version-of-record license entry) or the license statement and
  its page inside the PDF. Verify the checkout with

      awk -F'\t' 'NR > 1 { print $1 "  " $3 }' manifest.tsv | sha256sum -c --quiet

## Resolving a document

Tools find a file by its sha256 through `manifest.tsv`: gororoba-quantum's
`scripts/fetch_source_cache.py --from-documents` and gororoba-open's
`repo-utilities document-cache` read this checkout beside the private
sibling repository gororoba-documents-private, which holds the papers whose
license grants no redistribution.
