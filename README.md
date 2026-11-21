# POLYBRUTUS 21D — Exact twenty-six-point Euclidean metric and a fifteenfold ideal graph mode

**Human research author and responsible investigator:** Gabriel St-Pierre, independent researcher.  
**Status:** Exact reproducible computational mathematics; not independently reviewed by human peers.  
**AI assistance disclosure:** OpenAI ChatGPT (Astra) substantially assisted two separate verification programs, mathematical calculation, theoretical graph modelling, research writing and release work; AI is not an author.

## Exact results (radius R = 1)

- **26 labelled vertices**, **325 exact squared pairwise distances**, and minimum Euclidean affine embedding dimension exactly **21**.
- All **300/300** labelled squared distances from the immutable Polybrutus D20 predecessor are conserved. One new perpendicular radius-one vector creates **25 new squared distances**, each exactly **2**.
- Eight normalized squared-distance families `k = 4d²/R²`: `{4:6,7:2,8:294,9:3,10:10,12:6,13:2,16:2}`.
- Sum of all unordered pair squared distances: **2647R²/4**.
- Coordinate-difference rank **21** and centered squared-distance Gram rank **21**. The exact positive-semidefinite Gram identity `B=(HX)(HX)^T` is symbolically verified. The 22 storage-coordinate slots contain one centered regular-simplex linear relation.
- **Chosen hypothetical complete weighted-graph model**, unit scalar masses and `w_ij = R²/d_ij²`: eigenvalue **13** of exact multiplicity **15**, and eigenvalue **25/2** of multiplicity **4**. These are dimensionless mathematical graph modes, not measured physical frequencies.
- Two separately implemented Python verifiers reproduce all **325 labelled distances** and both spectral multiplicities; four deliberately wrong control configurations are rejected.

## Exact reproduction

```sh
python -m pip install sympy==1.14.0
python src/verify_d21.py
python tests/independent_d21.py
```

The independent rational checker reconstructs all distances without importing the geometric point generator. `prior/` holds unchanged source files and certificates copied from **frozen** `Topbrutus/polybrutus-d20@v0.1.0`, commit `3e9ee3117f1c3c3e5ffc80236fa2026a5d825ce3`.

Key archive files: `src/verify_d21.py`, `tests/independent_d21.py`, `results/certificate_d21.json` (all 325 labelled exact squared distances), `SPECIFICATION_D21.md`, `PREUVE_D21.md`, `PROVENANCE.md`, `publication/POLYBRUTUS_21D_NOTE.pdf` and `.md`, GitHub Actions workflow and `SHA256SUMS.txt`.

**Published predecessor:** [Polybrutus D20 — DOI 10.5281/zenodo.24409424](https://doi.org/10.5281/zenodo.24409424). Code MIT; scientific note CC BY 4.0.

**Scientific limitations:** Orthogonal Euclidean completions and uniformly joined graph spectral shifts are established mathematical methods. This is one exact particular 21D metric and selected graph model—not a newly demonstrated physical extra dimension, observed resonance, or new general mathematical theorem.
