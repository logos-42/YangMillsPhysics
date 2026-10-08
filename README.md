# YangMillsPhysics

**The Yang–Mills conjecture, proved in the gauge theory of the flowing-space framework.**

This repository is the third paper of the flowing-space series (paper/ and paper2/ live in
[Hibs-Physics](https://github.com/logos-42/Hibs-Physics)). It contains the bilingual paper
(English + Chinese) and points to the full Lean 4 formalization.

## The claim

Within the postulates of the flowing-space framework — space as a flowing medium; mass as
an integer count of excited strands, $m^2(N)=N M_0^2$; charge as the divergence of the flow;
the four forces as the Leibniz decomposition of the flow momentum — the two facts named by
the Yang–Mills conjecture are theorems, and the chain connecting them is closed:

- **The mass gap**: the mass spectrum is discrete by construction, the electron–photon
  transition $N\ge1\to N=0$ is an integer jump (MG3), the interval $(0,M_0^2)$ is empty
  (MG2b), the glueball mass squared is an integer (MG4).
- **The self-interaction**: the four-dimensional continuous gauge field strength carries the
  non-abelian term $[A_\mu,A_\nu]$ with $\mu\neq\nu$ (CC2), and the count-carrying sink
  contractions are noncommutative with the exact commutator $\lambda^2(v_q-v_p)$ (YM2–YM3).
- **The closed chain**: accelerated charge ⇒ varying field (CR1) ⇒ nuclear channel (CR2) ⇒
  self-flattening sink (CR9/YM1) ⇒ sink noncommutativity (YM2) ⇒ self-interaction $[A,A]$
  (CA3–CA4) ⇒ mass gap (CA7/MG2b). The continuum is intrinsic to the framework (CC1);
  the 4D field strength is non-abelian in the continuous setting itself (CC2–CC3).

Every step is a machine-checked theorem in Lean 4 with zero `sorry`.

## Files

| File | Description |
|---|---|
| `projection-yangmills-gap.tex` / `.pdf` | **English paper**: *Counting, Not Confinement — the Yang–Mills conjecture in the flowing-space gauge theory* |
| `projection-yangmills-gap-zh.tex` / `.pdf` | **Chinese paper**: 《质量间隙即计数——流动空间规范场理论中的杨–米尔斯猜想》 |
| `projection-physics.bib` | References (Yang–Mills 1954, Jaffe–Witten 2000, lattice glueball spectra, etc.) |

## Compile

```bash
cd paper3 && tectonic projection-yangmills-gap.tex
cd paper3 && tectonic projection-yangmills-gap-zh.tex
```

## The Lean formalization

Lives in the parent repository [Hibs-Physics](https://github.com/logos-42/Hibs-Physics),
modules:
- `MassGap.lean` — MG1–MG4 (mass gap from discreteness)
- `YangMillsSeed.lean` — YM1–YM3b (sink noncommutativity)
- `YangMillsLattice.lean` — CA1–CA10 (lattice gauge field)
- `YangMillsContinuum.lean` — CC1–CC10 (continuum is intrinsic; 4D field strength; path integral)
- `YangMillsStrict.lean` — L1–L3 (strict estimates)

## Honest boundary

"Proved" means: proved **within the gauge theory of the flowing-space framework**, with the
framework's postulates as axioms. Connecting this proof to the standard Wightman formulation
(the topological limit as a bridge to standard continuum QFT) is the stated open program.
