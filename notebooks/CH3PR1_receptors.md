# CH3PR1: Docking receptors

These are the six receptor structures used by the
[computational drug docking practical](Vina_dock_3D_CafChem.ipynb) (step 3,
"Choose a receptor"). The notebook automatically downloads the files for the
receptor you pick from this page's folder (`notebooks/dock_receptors`), so you
don't need to download anything by hand — the links below are here if you want
to inspect the files yourself.

Each receptor comes as two files:

- **`_target.pdbqt`** — the protein structure in the format AutoDock Vina
  reads (hydrogens and partial charges added, non-essential hydrogens merged).
  This is a [PDBQT](https://autodock.scripps.edu/faqs-and-help/what-is-pdbqt/)
  file, derived from the PDB structure of the protein.
- **`_conf.txt`** — the search box: the center and size (in Ångströms) of the
  region of the binding pocket that Vina searches for poses.

## Receptors

**Download all:** [dock_receptors.zip](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors.zip)
(307 KB). Extract it next to the notebook and you get a `dock_receptors`
folder with all twelve files - the ready-to-use layout for step 3. Browsers
always download zip files rather than opening them.

The direct links below open the file in the browser instead (GitHub shows
text files inline); to save one, right-click the link and choose "Save link
as..." (Cmd-click on a Mac).

| Code | Protein | Structure | Search box |
|------|---------|-----------|------------|
| DRD2 | Dopamine D2 receptor | [DRD2_target.pdbqt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/DRD2_target.pdbqt) | [DRD2_conf.txt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/DRD2_conf.txt) |
| DRD3 | Dopamine D3 receptor | [DRD3_target.pdbqt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/DRD3_target.pdbqt) | [DRD3_conf.txt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/DRD3_conf.txt) |
| ESR1 | Estrogen receptor alpha | [ESR1_target.pdbqt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ESR1_target.pdbqt) | [ESR1_conf.txt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ESR1_conf.txt) |
| ESR2 | Estrogen receptor beta | [ESR2_target.pdbqt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ESR2_target.pdbqt) | [ESR2_conf.txt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ESR2_conf.txt) |
| ADRB1 | Beta-1 adrenergic receptor | [ADRB1_target.pdbqt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ADRB1_target.pdbqt) | [ADRB1_conf.txt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ADRB1_conf.txt) |
| ADRB2 | Beta-2 adrenergic receptor | [ADRB2_target.pdbqt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ADRB2_target.pdbqt) | [ADRB2_conf.txt](https://raw.githubusercontent.com/MauricioCafiero/CafChem_Teaching_Notebooks/main/notebooks/dock_receptors/ADRB2_conf.txt) |

## About the receptors

The dopamine receptors (DRD2, DRD3) are the targets of antipsychotic drugs;
the estrogen receptors (ESR1, ESR2) bind hormones such as estradiol and are
targets for breast-cancer therapies; the adrenergic receptors (ADRB1, ADRB2)
respond to adrenaline and are targeted by beta-blockers and asthma drugs.
All six are G-protein-coupled receptors except the two estrogen receptors,
which are nuclear hormone receptors. The structures used here are the same
ones used in the [DUD-E](https://dude.docking.org/) benchmark set for virtual
screening.