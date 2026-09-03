# NEUR 201 — Unit 1

Coding activities for **NEUR 201: Research Methods & Data Analysis for Cellular Neuroscience**.

Everything runs in **Google Colab** in your browser. There is nothing to install and no
Google Drive to connect — click a badge below and start.

## Notebooks — start here

| Lesson | What you'll do | Open it |
|---|---|---|
| **W1 L2** — Intro to Jupyter & Python | No data needed. Learn how notebooks work, and the Python you'll see all term. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W1L2_Intro_to_Jupyter_and_Python__STUDENT.ipynb) |
| **W2 L2** — Colocalization analysis | Process a real confocal image: find Olig2⁺, Ki67⁺, and double-positive cells. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W2L2_Colocalization_analysis__STUDENT.ipynb) |
| **W4 L1** — Statistics of fluorescent imaging data | Eight steps from a raw column of numbers to a claim you can defend: histograms, mean/median/mode, skew, IQR, variance, and standard deviation. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W4L1_Statistics_of_fluorescent_imaging%20data_STUDENT.ipynb) |

Work through them in order: each one builds on the one before.

W4 L1 runs across **two sessions** — Steps 1–4 (shape and centre) in the first, Steps 5–8
(spread, and what you may claim) in the second. There are four **💬 Discussion** cells, two
per session.

## Before you start

**1. Save your own copy.** When a notebook opens in Colab, click **File → Save a copy in
Drive** straight away. If you skip this, your work will not be saved.

**2. Run every cell, in order, from the top.** Click a cell and press **Shift + Enter**.
Cells depend on the ones above them, so skipping around causes errors.

**3. Look out for these three things:**

| | What to do |
|---|---|
| **Ordinary cells** | Just run them. You don't need to understand every line. |
| **⚙️ Try it** | Change the highlighted value, re-run, and see what changes. |
| **💬 Discussion** | Double-click the cell and type your answer. |

**4. If something breaks,** the fix is almost always one of two things: you missed a cell
higher up (use **Runtime → Run all**), or a quotation mark or bracket got deleted by
accident. A red error box is normal and breaks nothing.

## Submitting your work

1. Answer every **💬 Discussion** cell, pressing **Shift + Enter** on each.
2. Click **Runtime → Run all** so every graph, table, and answer is visible.
3. **File → Print**, set the destination to **Save as PDF**, and save.
4. Upload the PDF to Canvas.

## The experiment behind the data

Sections of **cortex** and **corpus callosum** were taken from control animals (**CON**)
and drug-treated animals (**DRUG**), and stained for two markers:

- **Olig2** (AF488 / green) — marks **oligodendrocyte-lineage** cells
- **Ki67** (AF647 / far-red) — marks cells that are **actively dividing**

A cell positive for **both** is a *proliferating oligodendrocyte-lineage cell*. In W2 L2 you
measure those cells in a real image. In W4 L1 you analyse a table of results pooled from the
whole class, and work out what that table does — and does not — let you claim.

## Files in this folder

```
Unit_1/
├── notebooks/     the 3 student notebooks (+ instructor copies)
└── data/
    ├── images.csv   one row per image (40 images)
    └── cells.csv    one row per detected nucleus (1000 nuclei)
```

W4 L1 reads `images.csv` automatically from:

```
https://raw.githubusercontent.com/DrGPCR/NEUR201/main/Unit_1/data/
```

---

## For instructors

| Lesson | Instructor copy |
|---|---|
| **W1 L2** — Intro to Jupyter & Python | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W1L2_Intro_to_Jupyter_and_Python__INSTRUCTOR.ipynb) |
| **W2 L2** — Colocalization analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W2L2_Colocalization_analysis__INSTRUCTOR.ipynb) |
| **W4 L1** — Statistics of fluorescent imaging data | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W4L1_Statistics_of_fluorescent_imaging%20data_INSTRUCTOR.ipynb) |

Instructor copies add **model answers** in every Discussion cell, plus **📋 Instructor note**
cells with timing, marking guidance, and the common wrong answers to watch for.

### Setup checklist

1. **The repo must be public.** `raw.githubusercontent.com` will not serve the CSVs from a
   private repo, and students would get an error on the first cell.
2. **Upload the microscope image as a Release, not a file.** `1_slide_1_R.czi` is ~86 MB and
   GitHub's web uploader caps at 25 MB per file. Go to **Releases → Create a new release**,
   set the tag to exactly `unit1-image`, attach `1_slide_1_R.czi` as a binary, and publish.
   W2 L2 downloads it from:
   `https://github.com/DrGPCR/NEUR201/releases/download/unit1-image/1_slide_1_R.czi`
   If you use a different tag or filename, update `IMAGE_URL` in Step 1 of that notebook.
3. **Check one link before class.** Open
   `https://raw.githubusercontent.com/DrGPCR/NEUR201/main/Unit_1/data/images.csv` in a browser — you should see CSV text. If it 404s, the repo path,
   branch, or visibility is wrong, and every notebook will fail at Step 1.
4. If you rename the repo or the default branch isn't `main`, update the URL in this README,
   in each notebook's badge, and in the `DATA` variable in Step 1.

### Notes on the data

`images.csv` and `cells.csv` are **simulated**, shaped so specific teaching points land. The
ones W4 L1 depends on:

- CON and DRUG differ ~2× in `Colocalized_cells_per_mm2` (means 8.63 vs 16.66) with heavily
  overlapping ranges, so the group difference is real but no single image can be assigned to
  a group.
- Both groups are **positively skewed**, DRUG more strongly (mean − median = 1.10 vs 0.16),
  which drives the skew step and the choice between mean/SD and median/IQR.
- DRUG is ~2.5× more variable (SD 8.74 vs 3.54), so the drug shifted the centre *and* the
  spread — the point the final discussion turns on.
- The design is fully balanced: 10 images per Group × Batch and per Group × Region.

Other structure still present in the files, available if you want to extend: `AF488_intensity`
is right-skewed and smooth across the 2500 threshold; `Mean_AF488_intensity` has two batches
with matched means but very different spread; `AF488_cells_per_mm2` is bimodal by region.

The `.czi` image in W2 L2 is real.
