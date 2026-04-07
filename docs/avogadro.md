# Molecular structure building with Avogadro2

For visual inspection and editing of molecular structures we use
**Avogadro2** via the **Mahti Open OnDemand (OOD)** service.

Avogadro2 is used only as a graphical molecule editor.
All quantum chemistry calculations are performed in Jupyter notebooks
using ORCA or CP2K.

## Accessing Avogadro2 on Mahti

Avogadro2 is provided via a container installation available
in the Mahti OOD environment.

1. Log in to Mahti Open OnDemand  
   https://www.mahti.csc.fi
2. Start an **Interactive Desktop** session
3. Open a terminal inside the desktop session
4. Enable and load the Avogadro2 module:

```bash
module use /projappl/project_2017403/modules
module load avogadro2
```
