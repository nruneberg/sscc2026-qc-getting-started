# Molecular structure building with Avogadro2

**Avogadro2** is an optional graphical molecule editor available via
the **Mahti Open OnDemand (OOD)** service.

Use it to build or inspect molecular structures and export them as
input coordinates for ORCA or CP2K. All calculations are run in
Jupyter notebooks — Avogadro2 is a structure preparation tool only.

---

## Accessing Avogadro2 on Mahti

1. Log in to the Mahti web interface:
   [https://www.mahti.csc.fi](https://www.mahti.csc.fi)
2. Select **Desktop** and launch a session
3. Once the desktop has loaded, open a **terminal**
4. Load the Avogadro2 module:
```bash
    module use /projappl/project_2017403/modules
    module load avogadro2
```

5. Launch Avogadro2:
```bash
    avogadro2
```

---

## Basic workflow

1. **Build or import a structure** — use the draw tool or
   *File → Open* to load an existing file (`.xyz`, `.mol2`, etc.)
2. **Clean up the geometry** — use *Extensions → Optimize Geometry*
   for a quick force-field pre-optimisation
3. **Export coordinates** — *File → Save As* → choose `.xyz` format
4. Use the exported file as the coordinate input in your ORCA or CP2K
   notebook

---

## Tips

* Avogadro2 runs inside the Desktop session — keep that
  session alive while using it
* **Copy-paste between your local machine and the desktop** works via
  the noVNC clipboard: open the **Clipboard** menu from the tab on the
  left edge of the desktop window, paste your text there, then paste
  normally inside the desktop
* For simple molecules, the draw tool with auto-hydrogen addition
  is the fastest way to get started
* A force-field pre-optimisation in Avogadro2 before running ORCA
  saves time by providing a reasonable starting geometry
