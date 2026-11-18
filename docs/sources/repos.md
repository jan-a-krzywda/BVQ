# Repositories

Software BVQ reads, cross-checks against, or may wrap. Rule: BVQ only wraps permissively licensed code. GPL tools are named but not integrated.
See also [papers](papers.md) and [standards](standards.md).

## Characterization & benchmarking
| Tool | Use | Link |
|---|---|---|
| pyGSTi (Sandia) | GST, RB variants, mirror circuits, volumetric benchmarks | https://github.com/sandialabs/pyGSTi |
| qiskit-experiments | T1/T2/RB/IRB/tomography experiment library | https://github.com/qiskit-community/qiskit-experiments |
| qiskit-device-benchmarking | IBM device benchmarks incl. layer fidelity | https://github.com/qiskit-community/qiskit-device-benchmarking |
| Cirq | XEB, device characterization | https://github.com/quantumlib/Cirq |
| QED-C App-Oriented Benchmarks | Application benchmark suite | https://github.com/SRI-International/QC-App-Oriented-Benchmarks |
| SupermarQ | Application benchmark suite | https://github.com/SupertechLabs/SupermarQ |
| Metriq / metriq-gym (Unitary Fund) | Community benchmark results platform + runner | https://metriq.info · https://github.com/unitaryfund/metriq-gym |
| Mitiq | Error mitigation (to know/forbid in acceptance tests) | https://github.com/unitaryfund/mitiq |

## Fault-tolerant resource estimation (DARPA QB tools)
| Tool | Use | Link |
|---|---|---|
| BenchQ (Zapata) | FTQC resource estimation: graph-state compiler, distillation factories, decoder models; Apache-2.0 | https://github.com/zapatacomputing/benchq |
| pyLIQTR (USC-ISI / MIT LL) | Algorithm circuit generation for resource estimation | https://github.com/isi-usc-edu/pyLIQTR |
| Jabalizer.jl | Graph-state compilation | https://github.com/QSI-BAQS/Jabalizer.jl |
| Rigetti Resource Estimation | FT resource estimates for superconducting architectures | https://github.com/rigetti/rigetti-resource-estimation |
| LANL qc-applications | Quantum computing application specifications | https://github.com/lanl-ansi/qc-applications |
| liblsqecc | Lattice surgery compiler | https://github.com/latticesurgery-com/liblsqecc |
| Pandora | Circuit rewriting / optimization at scale | https://github.com/ioanamoflic/pandora |

## Candidate wrappers (reviewed, not yet integrated)

Licence column from a quick look at each repo on 2026-11-17. **[verify]** before wrapping. Reuse needs a licence check each time.

| Repo | Role | Licence note |
|---|---|---|
| https://github.com/munich-quantum-toolkit/bench | MQT Bench: circuit generator | check **[verify]** |
| https://github.com/QUARK-framework/QUARK | Application benchmark framework | check **[verify]** |
| https://github.com/terra-quantum-public/benchmarking | Terra Quantum benchmarking | check **[verify]** |
| https://github.com/PCSS-Quantum/open-qbench | Open benchmarking framework | check **[verify]** |
| https://github.com/usnistgov/benchqc | NIST BenchQC | NIST terms |
| https://github.com/AyanBarui/Extensive-Review-of-Benchmarking-Quantum-Computers | Review of benchmarks | no licence found: reference only, do not copy code |
| https://github.com/unitaryfoundation/metriq-gym | Benchmark runner | check **[verify]** |
| https://github.com/unitaryfoundation/mitiq | Error mitigation | GPL-3.0: **not wrapped** (licence conflict) |
