# Hallet Notebooks

Teaching material for the experimental / data-analysis half of **CH3CO1 / CH4PA1**
(Dr Hallet). Module material, so it lives here rather than under `Resources/`,
which is reserved for external repositories mirrored in as submodules.

Original filenames are kept unchanged so they still map onto the Blackboard
downloads. Each notebook sits in its own folder together with the data it loads,
laid out exactly as the notebook's relative paths expect — so every notebook runs
as-is, with no edits to the lecturer's code.

---

## Contents

| Folder | Notebook | Topics |
|---|---|---|
| 1 - Data Analysis Basics | `compchem_experimental_1.ipynb` | functions, Gaussians, noise, `ndimage` smoothing, `signal.find_peaks`, `loadtxt`, pandas basics |
| 2 - Peak Fitting and Image Analysis | `compchem_experimental_2.ipynb` | looping over many CSVs, images as arrays, `trackpy` feature location, `KDTree` nearest neighbours |
| 4 - Time-Resolved UV-Vis | `4_time_resolved_uv_vis_example-script.ipynb` | absorbance from raw counts, blank subtraction, peak tracking over 800+ spectra, 4 set tasks |
| Workshop - 2D Object Tracking | `Tracking_2_workshop.ipynb` | cell tracking challenge data, `tp.locate` / `tp.batch`, pair correlation, 5 set tasks |
| Molecular Dynamics - Project 1 | `basic_LJ.ipynb` | Lennard-Jones MD, velocity Verlet — **the starting point for Project 1 Part 2** |

Folder numbers follow the lecturer's own filename numbering. There is no folder 3:
example script 3 was not in the set of files downloaded, so the gap is deliberate
rather than a mistake.

---

## Data

Datasets were supplied as four zip archives. Two of them (the time-resolved UV-Vis
runs and the cell-tracking images) both unpack to a folder called `data/`, which is
why each notebook gets its own folder — it keeps the two `data/` directories apart
without renaming anything the notebooks reference.

| Dataset | Size | In git? |
|---|---|---|
| `2 - .../UV_sweep/` (101 CSVs) | 12 MB | yes |
| `2 - .../BBBC015_v1_images/` (578 JPGs) | 24 MB | no |
| `4 - .../data/` (runs + blank_cell, 839 txt) | 85 MB | no |
| `Workshop - .../data/` (110 TIFs) | 43 MB | no |
| `_source-archives/` (the original zips) | 88 MB | no |

The three large sets are gitignored, following the same reasoning as the existing
`models/` rule in the root `.gitignore`: bulky, binary, and re-downloadable. The
original zips are kept in `_source-archives/` so everything can be rebuilt locally:

```bash
cd "Hallet Notebooks"
unzip -q _source-archives/UV_sweep.zip           -d "2 - Peak Fitting and Image Analysis"
unzip -q _source-archives/BBBC015_v1_images.zip  -d "2 - Peak Fitting and Image Analysis"
unzip -q _source-archives/data.zip               -d "4 - Time-Resolved UV-Vis"
unzip -q "_source-archives/data (1).zip"         -d "Workshop - 2D Object Tracking"
```

After a fresh clone on another machine the archives won't be there either, so the
bulk data has to come back from Blackboard.

### Known gaps

- `Reading_shield.jpg` is loaded by `compchem_experimental_2.ipynb` (the `plt.imread`
  cell) but was not among the supplied files. Any JPEG dropped in that folder under
  that name will do — the cell only demonstrates RGB channel indexing.
- `dopamine_d2_receptor.csv` is a byte-identical copy of the one in the repository
  root. The duplicate is intentional: it keeps folder 1 self-contained so the
  notebook's relative path resolves.

### Dependencies beyond the usual stack

`trackpy`, `pims` and `imagecodecs` (for TIFF reading) are needed by folder 2 and the
tracking workshop, on top of numpy / scipy / pandas / matplotlib.
