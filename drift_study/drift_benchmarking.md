# Drift and benchmarking of an 18-qubit spin-qubit device

Working notes (2026-11-16). Context: acceptance tests for an 18-qubit spin-qubit
device; drift expected to be the dominant practical problem.

## 1. Core observation

Almost all standard benchmarks assume **time-stationary (Markovian, time-independent)
errors**. Drift breaks this assumption, so a single-snapshot benchmark does not catch it.

| Benchmark | What drift does to it |
|---|---|
| RB / IRB | Averages over the acquisition window: good 40 min + bad 20 min gives one "OK" number. If sequence lengths are acquired in order (short first), drift during the run bends the decay curve and biases the fitted error rate. |
| GST | Assumes time-independent errors. Drift appears as **model violation**: useful alarm, but no time-resolved picture. |
| QV, mirror circuits, layer fidelity (EPLG) | Single snapshot, usually right after calibration, so they show the best case. |
| Tender as usually written | Vendor calibrates, runs tests, passes. Performance hours later is never asked. |

## 2. Which benchmarks are still relevant at 18 qubits

| Benchmark | Relevance | Note |
|---|---|---|
| RB / simultaneous RB / IRB, per qubit and per pair | High | ~17 pairs on a linear chain, all measurable. Simultaneous RB catches crosstalk. |
| GST | Partial | Feasible only on 1–2 qubits; use on reference pairs as a precise gate spec. |
| Layer fidelity / EPLG on the chain | High | Cheap, scalable, one number for the whole device. |
| Mirror circuits | High | Map of achievable circuit width × depth. |
| GHZ fidelity, N ≤ 18 | High | Simple, hard to game. |
| Quantum Volume | Low | Linear connectivity makes it mostly a routing test. Optional. |
| Application suites | A few | 2–3 small circuits relevant to intended use. |

## 3. Drift timescales in spin qubits

1. **Fast (shot to shot, within one measurement):** 1/f charge noise. Shows up as
   dephasing (T2*); captured by standard benchmarks.
2. **Medium (minutes to hours):** qubit frequency wander, charge-trap switching
   (sudden jumps), drift of the readout sensor working point, microwave-heating
   frequency shifts depending on duty cycle (Undseth et al. 2023).
   **Main problem; not seen by standard benchmarks.**
3. **Slow (days, thermal cycles):** retuning needed. Belongs in operational
   acceptance tests.

## 4. How to make the tests catch drift

1. **Time-resolved battery.** Every 10–30 min for 24–72 h, run a cheap fixed set:
   - Ramsey on every qubit (frequency drift)
   - readout fidelity
   - RB at one or two fixed lengths
   - one mirror circuit or layer-fidelity measurement

   Result: time series per metric.
2. **Two modes:**
   - **No recalibration** (stability). Report: time after calibration until a
     metric falls below spec ("calibration half-life"), Allan deviation of each
     qubit frequency, rate of sudden charge jumps.
   - **Vendor auto-recalibration on** (delivered performance). Report: fraction of
     time in spec, fraction of time spent calibrating instead of computing.

   Contract on the second mode; require the first to be measured and delivered.
3. **Statistical drift test.** Proctor et al. 2020 spectral test on repeated
   circuits, with controlled false-alarm rate; implemented in pyGSTi. Requires raw
   data with timestamps.
4. **Data handling rules (put in the tender):**
   - timestamp every circuit/shot batch
   - randomize the order of RB lengths and circuits
   - realistic drive duty cycle (heating shifts frequencies)
   - raw data delivered to the buyer
5. **Pass/fail on percentiles over time**, not best value. Example: "2Q error < X
   for ≥ 95% of the 72 h window with auto-recalibration on."

## 5. Open questions

- Which drift metric to contract on: time-in-spec, calibration half-life, or both?
- Is drift correlated across the chain (shared source) or local? Affects whether
  one tracking qubit can stand in for all (see Yoneda et al. 2022).
- Does the vendor offer real-time frequency tracking/feedback (Berritta et al. 2023)?
  If yes, test with it on and quantify its overhead.
- Window length: 24 h vs 72 h vs 7 days, versus cost of cryostat time.

## 6. References (arXiv IDs verified)

- Proctor et al., *Detecting and tracking drift in quantum information processors*,
  Nat. Commun. 11, 5396 (2020). https://arxiv.org/abs/1907.13608
- Proctor et al., *Benchmarking quantum computers*, Nat. Rev. Phys. (2025).
  https://arxiv.org/abs/2407.08828
- Yoneda et al., *Noise-correlation spectrum for a pair of spin qubits in silicon* (2022).
  https://arxiv.org/abs/2208.14150
- Berritta et al., *Real-time two-axis control of a spin qubit* (2023).
  https://arxiv.org/abs/2308.02012
- Undseth et al., *Hotter is easier: unexpected temperature dependence of spin qubit
  frequencies*, PRX 13, 041015 (2023). https://arxiv.org/abs/2304.12984
- Nielsen et al., *Gate Set Tomography*, Quantum 5, 557 (2021).
  https://arxiv.org/abs/2009.07301
- McKay et al., *Benchmarking quantum processor performance at scale* (2023).
  https://arxiv.org/abs/2311.05933
- Tool: pyGSTi (drift module). https://github.com/sandialabs/pyGSTi
