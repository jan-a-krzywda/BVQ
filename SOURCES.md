# Sources

Curated links for benchmarking and verification & validation (V&V) of quantum computers,
with emphasis on acceptance testing in procurement and on spin-qubit hardware.
Papers are linked (arXiv), not stored. Literature review comes later.

arXiv IDs verified against the arXiv API on 2026-11-16.

---

## 1. Programs and procurement precedents

| Resource | What it is | Link |
|---|---|---|
| DARPA Quantum Benchmarking (QB) | Completed program: application benchmarks + hardware resource estimates (chemistry, materials, CFD, ...) | https://www.darpa.mil/research/programs/quantum-benchmarking |
| DARPA Quantum Benchmarking Initiative (QBI) | Ongoing: is utility-scale QC possible by 2033? Stages A (concept) / B (R&D plan, prototypes) / C (gov-led V&V). Spin-qubit performers: Diraq (C), Quantum Motion (B), Silicon Quantum Computing (B) | https://www.darpa.mil/research/programs/quantum-benchmarking-initiative |
| QBI Q&A 2026 | Program Q&A document | https://www.darpa.mil/sites/default/files/attachment/2026-03/darpa-qbi-q-a-2026.pdf |
| QBI Proposers Day 2024 | PM slides: how DARPA frames V&V | https://www.darpa.mil/sites/default/files/attachment/2024-12/qbi-proposers-day-2024-program-manager.pdf |
| QBI IV&V solicitation | DARPA-PA-26-02-01, Independent Verification & Validation topic | https://sam.gov/workspace/contract/opp/3fc74819705a4a81b205327ba4537973/view |
| EuroHPC JU quantum computers | EU procurements of quantum computers hosted at HPC centres; tender docs (incl. acceptance sections) on TED | https://eurohpc-ju.europa.eu · https://ted.europa.eu |
| BACQ (France, LNE/Thales) | Application-oriented benchmarks, metrology-institute led | https://arxiv.org/abs/2403.12205 · https://www.lne.fr/en |
| QED-C | US industry consortium; application-oriented benchmark suite | https://qed-c.org |

## 2. Standards

| Body | Item | Link |
|---|---|---|
| IEEE | P7131: Standard for Quantum Computing Performance Metrics & Performance Benchmarking | https://standards.ieee.org/ieee/7131/10681/ |
| CEN-CENELEC | JTC 22 Quantum Technologies (EU standardisation roadmap, benchmarking WG) | https://www.cencenelec.eu/areas-of-work/cen-cenelec-topics/quantum-technologies/ |
| ISO/IEC | JTC 3 Quantum technologies (est. 2024) | TODO: find stable link (iso.org blocks scripted access) |

## 3. Reviews and tutorials (start here)

- Proctor, Young, Baczewski, Blume-Kohout, *Benchmarking quantum computers*, Nat. Rev. Phys. (2025). https://arxiv.org/abs/2407.08828
- Hashim et al., *A Practical Introduction to Benchmarking and Characterization of Quantum Computers*, PRX Quantum (2025). https://arxiv.org/abs/2408.12064
- Eisert et al., *Quantum certification and benchmarking*, Nat. Rev. Phys. 2, 382 (2020). https://arxiv.org/abs/1910.06343
- Kliesch & Roth, *Theory of quantum system certification: a tutorial*, PRX Quantum 2, 010201 (2021). https://arxiv.org/abs/2010.05925
- Blume-Kohout et al., *A taxonomy of small Markovian errors*, PRX Quantum 3, 020335 (2022). https://arxiv.org/abs/2103.01928

## 4. Component-level protocols (gates, SPAM, leakage)

- Knill et al., *Randomized Benchmarking of Quantum Gates*, PRA 77, 012307 (2008). https://arxiv.org/abs/0707.0963
- Magesan, Gambetta, Emerson, *Scalable and robust randomized benchmarking of quantum processes*, PRL 106, 180504 (2011). https://arxiv.org/abs/1009.3639
- Magesan et al., *Efficient measurement of quantum gate error by interleaved randomized benchmarking*, PRL 109, 080505 (2012). https://arxiv.org/abs/1203.4550
- Helsen et al., *A general framework for randomized benchmarking*, PRX Quantum 3, 020357 (2022). https://arxiv.org/abs/2010.07974
- Proctor et al., *Direct randomized benchmarking for multi-qubit devices*, PRL 123, 030503 (2019). https://arxiv.org/abs/1807.07975
- Nielsen et al., *Gate Set Tomography*, Quantum 5, 557 (2021). https://arxiv.org/abs/2009.07301
- Erhard et al., *Characterizing large-scale quantum computers via cycle benchmarking*, Nat. Commun. 10, 5347 (2019). https://arxiv.org/abs/1902.08543
- Wood & Gambetta, *Quantification and characterization of leakage errors*, PRA 97, 032306 (2018). https://arxiv.org/abs/1704.03081

## 5. System-level / holistic benchmarks

- Cross et al., *Validating quantum computers using randomized model circuits* (Quantum Volume), PRA 100, 032328 (2019). https://arxiv.org/abs/1811.12926
- Blume-Kohout & Young, *A volumetric framework for quantum computer benchmarks*, Quantum 4, 362 (2020). https://arxiv.org/abs/1904.05546
- Proctor et al., *Measuring the capabilities of quantum computers* (mirror circuits), Nat. Phys. 18, 75 (2022). https://arxiv.org/abs/2008.11294
- McKay et al., *Benchmarking quantum processor performance at scale* (layer fidelity, EPLG). https://arxiv.org/abs/2311.05933

## 6. Application-level benchmarks

- Lubinski et al., *Application-Oriented Performance Benchmarks for Quantum Computing* (QED-C), IEEE TQE (2023). https://arxiv.org/abs/2110.03137
- Tomesh et al., *SupermarQ: A Scalable Quantum Benchmark Suite*, HPCA (2022). https://arxiv.org/abs/2202.11045
- Barbaresco et al., *BACQ: Application-oriented Benchmarks for Quantum Computing*. https://arxiv.org/abs/2403.12205

## 7. DARPA QB program outputs (fault-tolerant resource estimation)

Applications studied in the DARPA QB program, with hardware resource estimates:

- Bellonzi et al. (Zapata), homogeneous catalyst discovery. https://arxiv.org/abs/2406.06335
- Penuel et al. (L3Harris), drag force / nonlinear CFD. https://arxiv.org/abs/2406.06323
- Elenewski et al. (MIT LL), NMR spectral prediction. https://arxiv.org/abs/2406.09340
- Agrawal et al. (NCSU), Fermi-Hubbard model. https://arxiv.org/abs/2406.06511
- Mozgunov et al. (USC), open system simulation. https://arxiv.org/abs/2406.06281
- Bärtschi et al. (LANL), applications at Los Alamos. https://arxiv.org/abs/2406.06625
- Saadatmand et al. (Rigetti), superconducting qubits in the millions / modularity. https://arxiv.org/abs/2406.06015
- Nguyen et al. (Boeing), corrosion-resistant materials. https://arxiv.org/abs/2406.18759
- Otten et al. (HRL), amyloid-beta binding affinity. https://arxiv.org/abs/2406.18744
- Watts et al. (HRL), cyclic ozone in nanoscale confinement. https://arxiv.org/abs/2408.13244

## 8. Spin-qubit specific

- Burkard, Ladd, Pan, Nichol, Petta, *Semiconductor spin qubits*, RMP 95, 025003 (2023). https://arxiv.org/abs/2112.08863
- Yoneda et al., *A >99.9%-fidelity quantum-dot spin qubit with coherence limited by charge noise*, Nat. Nano. 13, 102 (2018). https://arxiv.org/abs/1708.01454
- Xue et al., *Computing with spin qubits at the surface code error threshold*, Nature 601, 343 (2022). GST-based spec. https://arxiv.org/abs/2107.00628
- Noiri et al., *Fast universal quantum control above the fault-tolerance threshold in silicon*, Nature 601, 338 (2022). https://arxiv.org/abs/2108.02626
- Mądzik et al., *Precision tomography of a three-qubit donor quantum processor in silicon*, Nature 601, 348 (2022). https://arxiv.org/abs/2106.03082
- Mills et al., *Two-qubit silicon quantum processor with operation fidelity exceeding 99%*, Sci. Adv. 8, eabn5130 (2022). https://arxiv.org/abs/2111.11937
- Philips et al., *Universal control of a six-qubit quantum processor in silicon*, Nature 609, 919 (2022). Crosstalk, multi-qubit operation. https://arxiv.org/abs/2202.09252
- Undseth et al., *Hotter is easier: unexpected temperature dependence of spin qubit frequencies*, PRX 13, 041015 (2023). Drive duty cycle / heating matters for benchmarks. https://arxiv.org/abs/2304.12984
- Cywiński et al., *How to enhance dephasing time in superconducting qubits* (filter functions; defines what T2 Hahn/CPMG measure), PRB 77, 174509 (2008). https://arxiv.org/abs/0712.2225

## 9. Software tools

### Characterization & benchmarking
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

### Fault-tolerant resource estimation (DARPA QB tools)
| Tool | Use | Link |
|---|---|---|
| BenchQ (Zapata) | FTQC resource estimation: graph-state compiler, distillation factories, decoder models; Apache-2.0 | https://github.com/zapatacomputing/benchq |
| pyLIQTR (USC-ISI / MIT LL) | Algorithm circuit generation for resource estimation | https://github.com/isi-usc-edu/pyLIQTR |
| Jabalizer.jl | Graph-state compilation | https://github.com/QSI-BAQS/Jabalizer.jl |
| Rigetti Resource Estimation | FT resource estimates for superconducting architectures | https://github.com/rigetti/rigetti-resource-estimation |
| LANL qc-applications | Quantum computing application specifications | https://github.com/lanl-ansi/qc-applications |
| liblsqecc | Lattice surgery compiler | https://github.com/latticesurgery-com/liblsqecc |
| Pandora | Circuit rewriting / optimization at scale | https://github.com/ioanamoflic/pandora |
