# Polybrutus D21 — Exact labelled Euclidean proof and spectral certificate

## 1. Conservative metric and class histogram

The frozen D20 configuration has 25 radius-one vectors and 300 exact labelled squared pair distances. Append a zero coordinate to each, and adjoin a new perpendicular unit vector. Every old pair remains identical; every new pair has squared distance `1+1=2`. Thus `325=300+25=C(26,2)` labelled pairs. The normalized `k=4d²/R²` histogram is `{4:6,7:2,8:294,9:3,10:10,12:6,13:2,16:2}`, summing exactly to 325 pairs, with total squared distance `2647R²/4`.

## 2. Minimal affine Euclidean dimension

Let `X` be the exact **26-by-22** stored coordinate matrix, `D` the exact **26-by-26 squared Euclidean distance matrix**, and `H=I-11ᵀ/26`. The primary symbolic verifier proves

```
rank([q2-q1,...,q26-q1])=21
rank(B)=21
B=-(1/2)HDH=(HX)(HX)^T.
```

The factorization is exact and proves positive semidefiniteness. Since the full labelled squared-distance matrix uniquely determines its centered Gram matrix, **all** Euclidean realizations of the same labelled 325-pair metric have minimum affine rank **21**. The one extra storage slot arises from an exact original simplex constraint.

## 3. Selected graph model

Take a **stipulated**, not measured, complete weighted graph with unit scalar masses and weights `w_ij=R²/d_ij²`. The new vertex couples to each of 25 predecessor vertices at weight 1/2:

```
L21=[ L20+(1/2)I25    -(1/2)1 ]
    [ -(1/2)1ᵀ              25/2 ].
```

The uniform global zero mode, intergroup mode, and shifted predecessor nonuniform modes yield the exact recurrence:

```
chi26(z)=z(z-13)*chi25(z-1/2)/(z-1/2).
```

From the frozen D20 factorization `chi25(z)=z(z-25/2)^14(z-12)^4 f6(z-9)` with `f6(z)=chiP7(z)/z`, substitution gives

```
chi26(z)=z(z-13)^15(z-25/2)^4 f6(z-19/2).
```

The primary verifier computes the full exact 26-by-26 characteristic polynomial and compares it to the recurrence and closed form. As `f6(7/2) != 0` and `f6(3) != 0`, the named model eigenvalues have **exact multiplicity 15 at 13** and **exact multiplicity 4 at 25/2**. A separately programmed rational-metric verifier independently checks all 325 squared distances, centered Gram rank, the full graph, and polynomial derivative tests of both eigenvalue multiplicities.

## 4. Falsification and scope

Four negative controls detect (1) a changed labelled distance, (2) a duplicated vertex causing a rank drop, (3) a tilted nonorthogonal point, (4) relabelled vertices preserving the histogram but not the complete labelled metric.

This specific synthetic Euclidean metric and a chosen graph model do not establish physical extra dimensions, experimental resonances or novel general mathematics. Independent human peer review has not occurred.
