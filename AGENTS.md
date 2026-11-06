# Agent guide

This repository is public. Every push publishes its files, and a published
file stays cached and indexed after removal.

- A file enters here only when its license permits redistribution of the
  exact bytes: any Creative Commons license (NonCommercial and NoDerivatives
  included), CC0, a documented public-domain status, or another license that
  grants redistribution. A Crossref license counts only with
  `content-version` `vor`; an arXiv license covers only arXiv-stamped bytes of
  the version it names. Everything else goes to gororoba-documents-private.
- Every file has one `manifest.tsv` row (`sha256`, `bytes`, `path`,
  `source_url`, `license`, `license_evidence`, `kind`), added in the commit that adds
  the file; verify the checkout against the manifest before pushing.
- Files stay unchanged: a PDF keeps its license notices, attribution and
  bytes. Every file stays under 100 MB.
- File every document by `TAXONOMY.md` (in gororoba-documents-public): open the PDF to establish the work,
  settle the rights of the exact bytes, then place it at `<field>/<subject>/<file>` with its kind in the
  manifest's `kind` column, and a transcription beside its PDF. A change to the vocabulary waits for the
  owner's approval and raises the taxonomy version. Consumers resolve files by sha256, so a move updates
  the file's manifest row in the same commit. A PDF's or source archive's bytes never change, and a corrected
  copy enters under a new name with its own row; a transcription is a derived file that revises in place, its
  manifest row replaced in the same commit, and git keeps every earlier version.
- The transcription of a PDF under a NoDerivatives license lives in gororoba-documents-private at the
  PDF's own `<field>/<subject>/` path, because its corrections, transcriber's notes and figure descriptions
  go beyond a format shift; the PDF stays here, and the transcription's header names its sha256.
- Write committed text without emoji, in American English, with no local
  absolute paths.
- Land changes on `main` through `git push origin main:main`.
