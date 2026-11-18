# Standards and programmes

Honest status first: **no published normative text found** for quantum-computer benchmarking.
Checked 2026-11-17. Everything below is in progress or pre-normative. BVQ does not claim conformance to any of it.
BVQ plan: write claim table and failure-mode gallery as a draft annex that a body can adopt.

## Standards bodies

| Body | Item | Status found | Link |
|---|---|---|---|
| IEEE | P7131, quantum computing performance metrics and benchmarking | Scope page only. No published definitions. PAR listed no active project when checked | https://standards.ieee.org/ieee/7131/10681/ |
| CEN-CENELEC | JTC 22 Quantum Technologies | Roadmap documents. No benchmarking standard listed | https://www.cencenelec.eu/areas-of-work/cen-cenelec-topics/quantum-technologies/ |
| ISO/IEC | JTC 3 Quantum technologies, JSC 3A, WG on quantum computing benchmarking | Group exists. No published standard found | search iso.org for "ISO/IEC JTC 3" (site blocks scripted access, no stable link yet) |
| DIN (Germany) | DIN SPEC on benchmarking with KPIs | Pre-normative, being prepared. Not checked in detail | no link yet |

## Programmes with a V&V structure (closest to acceptance practice)

| Programme | Why it matters | Link |
|---|---|---|
| DARPA Quantum Benchmarking Initiative (QBI) | Staged A / B / C. Stage C is government-led independent V&V | https://www.darpa.mil/research/programs/quantum-benchmarking-initiative |
| QBI Q&A 2026 | How DARPA frames the verification | https://www.darpa.mil/sites/default/files/attachment/2026-03/darpa-qbi-q-a-2026.pdf |
| QBI Proposers Day 2024 | PM slides | https://www.darpa.mil/sites/default/files/attachment/2024-12/qbi-proposers-day-2024-program-manager.pdf |
| QBI IV&V solicitation | Independent verification and validation topic | https://sam.gov/workspace/contract/opp/3fc74819705a4a81b205327ba4537973/view |
| DARPA Quantum Benchmarking (QB, finished) | Application benchmarks and resource estimates | https://www.darpa.mil/research/programs/quantum-benchmarking |
| EuroHPC JU | Quantum computers bought for HPC centres. Tenders with acceptance sections on TED | https://eurohpc-ju.europa.eu · https://ted.europa.eu |
| BACQ (LNE / Thales) | Metrology-institute-led application benchmarks | https://arxiv.org/abs/2403.12205 |
| QED-C | Industry consortium benchmark suite | https://qed-c.org |

## How BVQ uses this

- Each claim and each failure mode carries a `source` field.
- Source is a paper in [papers](papers.md), a programme above, or the sentence "standard unpublished".
- A test fails if a source is missing.
