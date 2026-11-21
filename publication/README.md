# Polybrutus D21 — Controlled research release

This mathematical case study is **unreviewed** and AI-assisted (disclosed). There is no claim of a new general theorem or physical dimension.

1. Run both exact verification programs and compare their 325-pair certificate SHA-256.
2. Create GitHub D21 **privately**; run both programs in GitHub Actions, require success on the candidate source commit.
3. Freeze successful commit under annotated Git tag `v0.1.0`.
4. Produce ZIP with `git archive v0.1.0`; hash that ZIP, PDF and labelled certificate JSON.
5. Stage exactly **one** Zenodo draft with predecessor D20 DOI, exact Git source and commit, academic author, AI disclosure, CC BY 4.0 note license; verify remote file checksums.
6. Make GitHub public, confirm Git source via unauthenticated public GitHub API, publish that same draft, and confirm Zenodo DOI and three files by public API.
7. Record DOI, tag, HEAD, file SHA-256 and CI outcome in README, CITATION.cff, release manifest, and central Memoria.

Never expose secrets, private messages or unrelated files in public Git; avoid duplicate Zenodo deposits through automated GitHub harvesting.
