# BVQ: Benchmarking and V&V of Quantum computers

**Mission.** Buyer and vendor agree what "works" means. Before the tender. In numbers.
Then anyone can check it. Same data, same verdict, with uncertainty.

## Problem

- Tenders say "T2 = X". Benchmarks measure T2\*, echo T2, RB error. Vendor quotes the nice one.
- Standard benchmarks assume stable noise. Real devices drift. Pass after calibration, fail after lunch.
- No published standard says how to accept a quantum computer.
- Nobody checks that an acceptance suite actually catches bad devices.

## What BVQ is

- A **claims file**: parameter, comparator, value, unit, source.
- A **verdict engine**: measured value with confidence interval vs claim. PASS, FAIL or INCONCLUSIVE.
- **Time-resolved tests**: drift is first-class. Timeline mode, with and without recalibration.
- A **dummy QC** with known, time-dependent noise. We know the truth.
- A **failure-mode gallery**: parametric faults injected into the dummy QC. Suite must catch each one. Gallery is public.
- A **report** with raw data hashes. `bvq verify` shows tampering.

Wraps and cross-checks existing tools. Does not reimplement RB or GST. See [repos](docs/sources/repos.md).

## Who uses it

Buyer. Vendor. Factory test house. Arbiter (SURF-like institution). Same record for all four.
See [CONOPS](docs/CONOPS.md).

## Failure modes

Long list, public, parametric (severity, seed). Arbiter draws fresh instances. Passing means robust, not memorised.
See [failure modes](docs/FAILURE_MODES.md).

## Scope

- First target: spin-qubit device, about 18 qubits, linear chain.
- Tool is neutral. Not tied to one vendor or one hardware type.
- Variational and hybrid algorithms: planned after core.
- Draft annex (claim table + failure modes) for a standards body, for example DIN SPEC.

## Status

Notes and design only. No tool released yet.

## Sources

- [Papers](docs/sources/papers.md)
- [Standards and programmes](docs/sources/standards.md): no published normative text found. Said plainly.
- [Repositories](docs/sources/repos.md)
- [Drift notes](drift_study/drift_benchmarking.md)

## Diagrams

TikZ sources in [docs/diagrams](docs/diagrams). PNGs rendered with `pdflatex` + `pdftocairo`.
