# Polybrutus D21 — Formal exact twenty-six-point Euclidean specification

**Frozen source:** `Topbrutus/polybrutus-d20@v0.1.0`, commit `3e9ee3117f1c3c3e5ffc80236fa2026a5d825ce3`, DOI `10.5281/zenodo.24409424`.

Let `p1,...,p25` be the predecessor exact radius-one points represented with 21 storage-coordinate slots. A single exact linear relation among the five centered regular-simplex slots makes the intrinsic dimension one lower.

Embed all preceding points as `q_i=(p_i,0)` in 22 storage slots, for `i=1,...,25`. Add `q26=e22=(0,...,0,1)`, a perpendicular unit basis vector. For every old point:

```
||q26-q_i||²=||q26||²+||q_i||²-2<q26,q_i>=2.
```

All **300** previous labelled pair squared distances remain unchanged, and the 25 new distances have square `2`. There are `C(26,2)=325` pairs, and the minimum intrinsic Euclidean affine dimension is **21** despite the 22 coordinate slots. Scaling the coordinates by `R>0` scales each squared distance by `R²`.

Histogram for `k=4d²/R²`: `{4:6,7:2,8:294,9:3,10:10,12:6,13:2,16:2}`. Squared-distance sum: `2647R²/4`. Unit-radius centroid: `(0,0,1/52,0,0,0,0,0,1/26,...,1/26)` with fourteen final entries `1/26`.

## Chosen theoretical graph

Define equal unit scalar masses and a complete hypothetical graph with weights `w_ij=R²/d_ij²`. The 26th point joins all old points at weight 1/2:

```
L21=[ L20+(1/2)I25   -(1/2)1 ]
    [ -(1/2)1ᵀ             25/2 ].
```

Let `f6(z)=chiP7(z)/z` denote the six-nonzero-mode factor of the canonical seven-point theoretical graph. Then

```
chi26(z)=z(z-13)*chi25(z-1/2)/(z-1/2)
        =z(z-13)^15(z-25/2)^4*f6(z-19/2).
```

The exact model eigenvalue **13** has multiplicity **15** and **25/2** has multiplicity **4**. These values are not empirically measured frequencies.
