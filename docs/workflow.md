# Hands‑on workflow

The SSCC 2026 Quantum Chemistry hands‑on consists of several
**notebook‑based sessions**, each focusing on a different topic
or methodology.

Detailed, step‑by‑step instructions are provided directly
in the notebooks used during each session.

---

## Session overview

### Quantum Chemistry hands‑on (Thursday 9.4.)

The Thursday sessions are organised around a **common core session**,
followed by optional, independent follow‑up sessions.

#### Core quantum chemistry workflows (common to all)

**QC engine:** ORCA

All participants begin with the **core quantum chemistry workflows**,
based on an introductory ORCA notebook.

After completing the core session, participants will be able to:

* Understand the key parts of **ORCA input files** for molecular systems
* **Optimise molecular structures** with ORCA
* **Compare total energies** of molecular isomers to identify the
  lowest‑energy structure
* **Calculate and interpret infrared vibrational spectra** for molecules

This core session provides the foundation for the optional follow‑up sessions.

---

#### Multireference electronic structure methods (optional)

**QC engine:** ORCA

Introduces cases where single‑reference methods are insufficient and
multireference approaches are needed. Topics include:

* Identifying situations that require multireference treatment
* Understanding the limitations of single‑reference methods
* Practical multireference calculations using ORCA

---

#### Electronic structure and molecular simulation with CP2K (optional)

**QC engine:** CP2K

Explores the **proton transfer step** in the interconversion of the two
enol forms of *2‑formylcyclohexanone* using DFT calculations.

!!! note "CP2K batch jobs use a different reservation"
    Interactive notebook work uses reservation `sscc_thu_small`, partition `small`.
    Batch jobs submitted from within the notebooks use reservation `sscc_thu_medium`,
    partition `medium`. The notebooks will indicate when this applies.

Materials: [https://github.com/csc-training/sscc-cp2k](https://github.com/csc-training/sscc-cp2k)

---

### Potential Energy Surface exploration (Friday 10.4.)

**QC engine:** ORCA

Held on Friday, consisting of a lecture followed by a hands‑on exercise.
Focuses on understanding and analysing molecular potential energy surfaces.
Independent of the Thursday sessions.

---

## Quick reference

| Session | Day | Course module | Reservation | Partition |
|---|---|---|---|---|
| Core QC workflows | Thu | `sscc-2026-qc` | `sscc_thu_small` | `small` |
| Multireference methods | Thu | `sscc-2026-qc-mr` | `sscc_thu_small` | `small` |
| CP2K (notebooks) | Thu | `sscc-2026-cp2k` | `sscc_thu_small` | `small` |
| CP2K (batch jobs) | Thu | — | `sscc_thu_medium` | `medium` |
| PES exploration | Fri | `sscc-2026-qc-pes` | `sscc_fri_small` | `small` |

---

## Relationship between sessions

* The **core QC workflows** session is common to all participants
* Follow‑up sessions are **optional** and largely **independent**
* Different QC engines (ORCA and CP2K) are used in different sessions
* All required software is provided via **CSC Jupyter for Courses**
