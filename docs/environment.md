# Working environment

The SSCC 2026 Quantum Chemistry hands‑on uses
**CSC Jupyter for Courses**, accessed via the Mahti web interface.

All hands‑on work is carried out in this environment.
No local installation or software setup is required.

The notebooks rely on:

* CSC‑provided installations of **ORCA** and **CP2K**
* A **custom Python environment** prepared for the course

---

## Access

Log in to the Mahti web interface using your **CSC or Haka account**:

👉 [https://www.mahti.csc.fi](https://www.mahti.csc.fi)

!!! warning "MFA required"
    The Mahti web interface requires **multi-factor authentication (MFA)**.
    Ensure MFA is active before the hands-on session.

    * [Activate MFA for Haka accounts](https://docs.csc.fi/accounts/mfa/#mfa-instructions-for-users-logging-in-with-haka-credentials)
    * [Activate MFA for CSC accounts](https://docs.csc.fi/accounts/mfa/#how-to-activate-mfa)

---

## Starting a notebook session

1. Go to [https://www.mahti.csc.fi](https://www.mahti.csc.fi)
2. Select **Jupyter for Courses**
3. Fill in the form:

    | Field | Value |
    |---|---|
    | **Project** | `project_2017403` |
    | **Course module** | see table below |
    | **Reservation** | see table below |
    | **Partition** | `small` (or as indicated) |

4. Click **Launch** and wait for the session to start (typically under a minute)
5. Once the Jupyter environment has opened, navigate to the notebook indicated during the session

### Which module do I pick?

| Session | Course module | Reservation |
|---|---|---|
| Core QC workflows (Thu) | `sscc-2026-qc` | `sscc_thu_small` |
| Multireference methods (Thu, optional) | `sscc-2026-qc-mr` | `sscc_thu_small` |
| CP2K (Thu, optional) | `sscc-2026-cp2k` | `sscc_thu_small` |
| PES exploration (Fri) | `sscc-2026-qc-pes` | `sscc_fri_small` |

Partition is `small` for all sessions except CP2K batch jobs (`medium`) —
see [Workflow](workflow.md#quick-reference) for details.

---

## During the session

* The notebooks are largely self‑contained — instructions are in the cells
* Do not hesitate to ask for help if something is unclear

All required software is preconfigured in the environment.
