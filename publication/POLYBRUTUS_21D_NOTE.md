# Polybrutus 21D: Exact Euclidean Completion and a Fifteenfold Weighted-Graph Mode

**Research author:** Gabriel St-Pierre  
**Affiliation:** Independent researcher  
**Programme:** Polybrutus-X72  
**Date:** 20 November 2026  
**Version:** 0.1.0  
**Status:** Reproducible computational mathematics preprint; not independently peer-reviewed by humans  
**Published predecessor:** Polybrutus 20D, DOI 10.5281/zenodo.24409424  
**Frozen scientific source:** https://github.com/Topbrutus/polybrutus-d21/tree/v0.1.0 (upon release)

## Abstract

We construct a particular exact **twenty-six-point labelled Euclidean distance metric** with minimal affine embedding dimension **twenty-one**, by conservative perpendicular extension of the frozen Polybrutus 20D metric. All **300 predecessor labelled pairwise squared distances** remain identical. One new orthogonal radius-R unit-direction point adds **25 squared pair distances of exactly 2R²**, producing **325 labelled unordered pair distances** in eight exact normalized families. Exact rank of coordinate differences and exact centered squared-distance Gram rank both equal 21; the positive-semidefinite Gram property follows from an algebraic factorization. A separately implemented rational verification program reproduces all 325 labelled distances and checks the Gram rank without importing the main coordinate generator.

For a deliberately **chosen theoretical complete weighted-graph scalar-oscillator model**, with equal scalar masses and edge weights `w_ij=R²/d_ij²`, the graph Laplacian of the twenty-six-vertex configuration has **an eigenvalue 13 with exact multiplicity fifteen** and **an eigenvalue 25/2 with exact multiplicity four**. Both are independently verified by complete exact characteristic-polynomial calculations. These are properties of an abstract mathematical model, not measured frequencies, discoveries of fundamental physical dimensions, or new universal mathematical theorems.

## 1. Research lineage and frozen source

Polybrutus starts with seven analytically defined points on a two-sphere of radius R embedded in three-dimensional Euclidean space. Its first 7D construction conservatively joined five vertices of a centered regular four-dimensional simplex in a subspace orthogonal to the original three-space, retaining the seven original labelled points and producing twelve vertices with sixty-six pair distances. That initial research was deposited as Polybrutus 7D (DOI **10.5281/zenodo.24407952**).

Subsequent exact computational dimension-specific cases were published: 8D (13 vertices, 78 labelled pairs, DOI 10.5281/zenodo.24408344), 9D (14, 91, 10.5281/zenodo.24408448), 10D (15, 105, 10.5281/zenodo.24408569), 11D (16, 120, 10.5281/zenodo.24408650), 12D (17, 136, 10.5281/zenodo.24408720), 13D (18, 153, 10.5281/zenodo.24408769), 14D (19, 171, 10.5281/zenodo.24408836), 15D (20, 190, 10.5281/zenodo.24408887), 16D (21, 210, 10.5281/zenodo.24408979), 17D (22, 231, 10.5281/zenodo.24409067), 18D (23, 253, 10.5281/zenodo.24409207), 19D (24, 276, 10.5281/zenodo.24409343) and 20D (25, 300, 10.5281/zenodo.24409424).

The present 21D configuration is derived **only from the frozen scientific Git tag** `Topbrutus/polybrutus-d20@v0.1.0`, commit `3e9ee3117f1c3c3e5ffc80236fa2026a5d825ce3`. The tagged ancestor programs and certificates are copied unchanged into `prior/`. No prior Polybrutus release, archived DOI, source tag, or original point coordinate is altered.

## 2. Exact construction: twenty-six unit-radius points

Normalize radius `R=1`. Let `p1,...,p25` be the twenty-five exact unit vectors from the frozen D20 configuration, represented in twenty-one coordinate-storage slots. Five of those slots describe the centered regular-simplex coordinates and obey one exact linear relation.

Embed each old vector in twenty-two storage slots by appending a zero:

```
q_i=(p_i,0),          i=1,...,25.
```

Add the twenty-sixth point as a perpendicular unit basis vector in the twenty-second storage coordinate:

```
q26=e22=(0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1).
```

All new and old vectors have norm one and the added vector is perpendicular to all prior vectors. Hence every one of the previous **300 squared labelled pair distances** remains unchanged. Each of the 25 new pairs satisfies

```
||q26-q_i||² = ||q26||² + ||q_i||² - 2<q26,q_i> = 2.
```

At general radius `R>0`, rescaling every vector by `R` gives 25 new squared distances equal to `2R²`. The full unordered labelled pair count is

```
C(26,2)=325=300+25.
```

Using normalized squared-distance parameter `k=4d²/R²`, the complete exact histogram is

| k | 4 | 7 | 8 | 9 | 10 | 12 | 13 | 16 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Labelled pairs | 6 | 2 | **294** | 3 | 10 | 6 | 2 | 2 |

The eight class multiplicities sum to 325. The exact sum of squared pair distances is

```
sum_{i<j} d_ij²/R² = 2647/4.
```

For unit radius, the centroid in twenty-two storage-coordinate slots is

```
G=(0,0,1/52,0,0,0,0,0,1/26,1/26,1/26,1/26,1/26,1/26,
   1/26,1/26,1/26,1/26,1/26,1/26,1/26,1/26).
```

The last 14 entries are each 1/26. The **affine rank is 21 rather than the storage count 22**, because of the single exact centered-simplex coordinate relation.

## 3. Exact centered Gram and minimal affine embedding dimension

Write `X` for the exact 26-by-22 coordinate array, `D` for the 26-by-26 symmetric **squared Euclidean distance** matrix and `H=I-11ᵀ/26` for the centering projector. Define

```
B=-(1/2)HDH.
```

The primary exact symbolic verifier proves the following identities, without floating-point approximations:

```
rank([q2-q1,...,q26-q1])=21;
rank(B)=21;
B=(HX)(HX)^T.
```

The final identity supplies an exact **positive-semidefinite Gram factorization**, certifying Euclidean realizability. Because a complete labelled Euclidean squared-distance matrix uniquely determines the centered Gram, **every Euclidean realization of these exact 325 labelled pair distances has minimum affine dimension 21**. This does not claim 21 physical spacetime dimensions.

The second, independently implemented rational metric verifier does not import the main point generator or previous geometry programs. It derives each squared distance from rational rules describing the canonical seven-point coordinates, five centered regular-simplex vertices with internal squared distances `5/2`, and fourteen mutually orthogonal radius-one unit directions. It confirms **325/325** exact labelled distances, all **300 predecessor pairs** and centered Gram rank **21**.

## 4. Fifteenfold mode of a chosen mathematical graph

Define a complete weighted graph on the 26 labelled points with hypothetical equal unit scalar oscillator masses and pair weights `w_ij=R²/d_ij²`. These couplings are explicitly **chosen** for a theoretical model, not measured from any instrument.

The newly added point lies at normalized squared distance 2 from every prior point. Consequently its 25 new edges each have weight 1/2. Let `L20` denote the predecessor 25-by-25 graph Laplacian and `L21` the new 26-by-26 Laplacian. They satisfy the exact block identity:

```
L21=[ L20+(1/2)I25    -(1/2)1 ]
    [ -(1/2)1ᵀ             25/2 ].
```

The global uniform zero mode, the intergroup differential mode and shifted predecessor zero-sum modes give the exact characteristic-polynomial recurrence:

```
chi26(z)=z(z-13)chi25(z-1/2)/(z-1/2).
```

The frozen D20 graph characteristic polynomial is

```
chi25(z)=z(z-25/2)^14(z-12)^4*f6(z-9),
f6(z)=chiP7(z)/z,
```

where `chiP7` refers to the initial seven-point ideal weighted graph and `f6` contains its six nonzero modes. Exact substitution yields

```
chi26(z)=z(z-13)^15(z-25/2)^4*f6(z-19/2).
```

The primary program calculates the **entire exact 26-by-26 characteristic polynomial**, and verifies its equality to the recurrence and closed form. Exact nonvanishing checks `f6(7/2) != 0` and `f6(3) != 0` exclude additional coincident factors at the named roots. The model eigenvalue **13** therefore has exact multiplicity **15**; eigenvalue **25/2** has exact multiplicity **4**.

The separate rational-metric checker reconstructs the weighted graph independently, calculates its full exact characteristic polynomial, and verifies both multiplicities by the vanishing/nonvanishing of successive polynomial derivatives. These eigenvalues are abstract dimensionless properties of one specified graph, **not frequencies in hertz**.

## 5. Reproduction and adversarial falsification

The scientific source contains `src/verify_d21.py` (exact geometry, rank, Gram and selected graph), `tests/independent_d21.py` (separate rational metric and spectral checks), `results/certificate_d21.json` (all 325 exact labelled squared distances), frozen predecessor source and certificates in `prior/`, formal specification, proof, provenance, GitHub Actions and SHA-256 Git blob index.

Reproduce with:

```sh
python -m pip install sympy==1.14.0
python src/verify_d21.py
python tests/independent_d21.py
```

Both programs must produce PASS and the same exact JSON certificate SHA-256. Four deliberately invalid controls are detected: modification of a labelled squared distance, duplication of a point causing affine rank loss, tilting the new unit vector to violate perpendicularity, and exchanging point labels while preserving the unlabelled distance histogram but not the labelled metric.

A controlled Zenodo release archives exactly three artifacts: the Git source ZIP created exclusively from the frozen tag, this PDF scientific preprint, and the exact JSON certificate. Their original sizes and cryptographic checksums permit later byte-level verification.

## 6. Scientific precedence, scope, authorship and licensing

Orthogonal Euclidean extension of point configurations, centered squared-distance Gram rank and uniform weighted-graph Laplacian joins are **established mathematical techniques**. This paper supplies one particular exactly reproducible Polybrutus 21D case study, not an original universal mathematical theorem or a verified physical theory. Its mathematical affine rank is not evidence for 21-dimensional physical spacetime, measured resonance or new particle phenomena.

**Research author and responsible investigator:** Gabriel St-Pierre, independent researcher. He originated the Polybrutus programme and directs the dimensional study and archival protocol.

**Generative AI disclosure:** OpenAI ChatGPT (Astra) substantially assisted the exact symbolic calculations, both verification programs including a separately implemented rational checker, theoretical graph spectral analysis, frozen source auditing, manuscript drafting, scientific documentation and controlled GitHub/Zenodo publication. The AI is **not a research author**. Independent human scientific peer review has not taken place.

**Licensing:** manuscript and prose CC BY 4.0; code source MIT.

**References:** canonical geometry https://github.com/Topbrutus/polybrutus/blob/main/SPECIFICATION.md ; frozen D20 parent source https://github.com/Topbrutus/polybrutus-d20/tree/v0.1.0 ; D20 DOI https://doi.org/10.5281/zenodo.24409424 ; full preceding DOI series in the repository's `PROVENANCE.md`.
