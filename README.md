# NEUR 201 — Research Methods & Data Analysis for Cellular Neuroscience

Welcome to the Coding activities for **NEUR 201**! These activities will be taught in **Google Colab**. Every notebook runs in a
browser — nothing to install, no Google Drive to connect, and all datasets load automatically
from this repository.

---

## The course at a glance

The three units follow one arc: **measure something → describe it → decide whether it's real.**

| Unit | Theme | Lessons |
|---|---|---|
| **[Unit 1](Unit_1/)** | Microscopy and descriptive statistics | W1 L2 → W4 L1 |
| **[Unit 2](Unit_2/)** | Electrophysiology and inferential foundations | W5 L1 → W6 L2 |
| **[Unit 3](Unit_3/)** | Functional imaging and hypothesis testing | W9 L2 → W11 L1 |

Each unit folder has its own README with the Colab links and setup details.

---

## Unit 1 — Cell density, colocalization, and describing data

Students count proliferating oligodendrocyte-lineage cells in a real confocal image, then learn
to describe the resulting numbers.

| Lesson | Notebook | What it covers |
|---|---|---|
| **W1 L2** | Intro to Jupyter and Python | Cells, variables, lists, loops, functions, DataFrames, error messages |
| **W2 L2** | Colocalization analysis | Thresholding, size filtering, labelling, mask overlap, cells per mm², proliferation fraction |
| **W3 L1** | Frequency tables and graphs | Frequency tables, binning, relative frequency, histograms, bar/pie charts, misleading axes, scatter plots |
| **W3 L2** | Measures of central tendency | Mean, median, mode; outliers; symmetric vs skewed distributions |
| **W4 L1** | Measures of dispersion | Range, IQR, variance, standard deviation, box plots |

**Data:** `images.csv` (40 images) and `cells.csv` (1000 nuclei) — simulated, in the shape the
Unit 1 pipeline exports. The confocal image `1_slide_1_R.czi` is **real** and lives in a GitHub
Release.

---

## How the notebooks are built

Every notebook follows the same shape, so students only learn the format once:

| | |
|---|---|
| **Five steps** | Each notebook is exactly five numbered steps, with sub-steps inside |
| **⚙️ Try it** | A value students change and re-run to see what happens |
| **💬 Discussion** | A question students type an answer into, discussed in class |
| **Symbol key** | Every statistics notebook lists what each symbol in its formulas means |
| **Submission** | Runtime → Run all, then File → Print → Save as PDF, then upload to Canvas |

Formulas and notation match the lecture slides, including the population/sample distinction
($\mu$, $\sigma$, $N$ versus $\bar{X}$, $s$, $n-1$).

---

## Notes on the data

All datasets are **simulated** except the confocal image in Unit 1. They're shaped so that
specific teaching points land — a bimodal distribution that resolves when split by brain region,
two staining batches with identical means but very different spread, group SDs that differ enough
to make Welch's t-test worth discussing.

Each unit's `scripts/` folder contains the generator that produced its data, so any dataset can be
regenerated or re-tuned. If you do change one, check the unit README first: it lists the property
each variable has to keep for the lesson to work.
