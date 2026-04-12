# Molecular structure building and analysis with Avogadro2

**Avogadro2** is a graphical molecular editor and analysis tool available via
the **Mahti Open OnDemand (OOD)** service.

Use it to:

* Build molecular structures and export coordinates for use in ORCA or CP2K
* Generate ORCA input files via the built-in input generator
* Analyse ORCA output — visualise molecular orbitals, animate vibrational
  modes, and plot IR spectra by opening the `.out` file directly

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

### Structure building

1. **Build or import a structure** — use the draw tool or
   *File → Open* to load an existing file (`.xyz`, `.mol2`, etc.)
2. **Clean up the geometry** — use *Extensions → Open Babel → Optimize Geometry*
   for a quick force-field pre-optimisation
3. **Export coordinates** — *File → Export Molecule* → File name `mymolecule.xyz`
4. Use the exported `xyz` file as the coordinate input in your ORCA or CP2K notebook

### Analysing ORCA output

1. Open the ORCA output file directly: *File → Open* → select `.out` file
2. **Molecular orbitals** — select the orbital of interest in the
   *Molecular Orbitals* panel and click *Render*
   (requires `!PRINTMOS !PRINTBASIS` or the orbital printout option in the input generator)
3. **Vibrational modes** — *Analyze → Vibrational Modes...* to animate modes
   and plot the IR spectrum (requires a frequency calculation)

---

## Tips

* Avogadro2 runs inside the Desktop session — keep that session alive while using it
* **Copy-paste between your local machine and the desktop** works via
  the noVNC clipboard: open the **Clipboard** menu from the tab on the
  left edge of the desktop window, paste your text there, then paste
  normally inside the desktop
* A force-field pre-optimisation in Avogadro2 before running ORCA
  saves time by providing a reasonable starting geometry
