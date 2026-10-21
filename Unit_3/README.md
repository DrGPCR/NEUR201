> ⚠️ **This file replaces the old README.** The `Unit_3/data/` folder needs all four CSVs listed
> below, and the notebooks belong in `Unit_3/notebooks/`. Delete `dFF_per_slice_2.csv` if it's still
> there — it has been superseded by `dFF_per_slice_assignment.csv`.

# NEUR 201 — Unit 3

Functional imaging, and the statistics of deciding whether an effect is real.

Everything runs in **Google Colab** in your browser — nothing to install, no Google Drive.

## Notebooks — start here

| Lesson | What you'll do | Open it |
|---|---|---|
| **W9 L2** — Functional imaging analysis | Turn a calcium-imaging movie into ΔF/F₀ traces, heatmaps, and event counts. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_3/notebooks/W9L2_Functional_imaging_analysis__STUDENT.ipynb) |
| **W11 L1** — From standard errors to t-tests | Sampling distributions and SEM, the t-score and the p-value, alpha, and an independent-samples t-test presented as a bar graph with its significance. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_3/notebooks/W11L1_Inferential_statistics__STUDENT.ipynb) |

Work through them in order. W9 L2 produces the measurement; W11 L1 decides what it means.

## Assignments

Do these after the lessons they follow from. Both are graded out of **10 points**.

They use **different data from the lessons** — a different drug, with a different effect. You cannot
reuse the lesson's conclusion, so read your own numbers.

| Assignment | What you'll do | Open it |
|---|---|---|
| **Unit 3 — Data Analysis** | Run the full imaging pipeline yourself: ΔF/F₀, heatmap, traces, event detection — then change the event threshold and defend the result. *(after W9 L2)* | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_3/notebooks/Unit_3_Data_Analysis_Assignment_STUDENT.ipynb) |
| **Unit 3 — Statistics** | Twelve slices per group: means, SD vs SEM, an independent-samples t-test, and a bar graph carrying its significance. *(after W11 L1)* | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_3/notebooks/Unit_3_Statistics_Assignment_STUDENT.ipynb) |

## Before you start

**1. Save your own copy** — **File → Save a copy in Drive** — or your work won't be saved.

**2. Run every cell, in order, from the top** (**Shift + Enter**).

**3. Watch for these:**

| | What to do |
|---|---|
| **Ordinary cells** | Just run them. |
| **⚙️ Try it** | A value in the code you can change. The Discussion for that step tells you what to set it to. |
| **💬 Discussion** | Double-click and type your answer. |

Every **💬 Discussion** sits directly under the step it belongs to, and each has exactly **two
questions**. Where a step has a **⚙️ Try it** value in its code, the Discussion is the only place
you're told what to set it to — so the Try it and the question you answer are one task, not two.

**4. Before you export, put any ⚙️ Try it values back to their defaults** so the figures in your PDF
match the numbers you report. Each notebook lists its defaults in the closing cell.

## Data

The notebooks read these straight from `Unit_3/data/` on GitHub — there is nothing to download. If a
download ever fails, each notebook tells you to upload the file by hand via the 📁 folder icon and
re-run the cell.

| File | Used by | What's in it |
|---|---|---|
| `functional_imaging_dummy.csv` | W9 L2 | Two recordings (CONTROL and DRUG), 100 cells each, 6 min at 10 fps. One row per frame, one column per cell. |
| `dFF_per_slice.csv` | W11 L1 | 10 slices per group; each slice's mean ΔF/F₀ (%) during application. |
| `functional_imaging_assignment.csv` | Unit 3 Data Analysis | Same format as the lesson recording, different drug. |
| `dFF_per_slice_assignment.csv` | Unit 3 Statistics | 12 slices per group, from the assignment study. Same three columns. |

## Submitting your work

1. Answer every **💬 Discussion** cell.
2. **Runtime → Run all** so every graph and answer is visible.
3. **File → Print → Save as PDF**, then upload the PDF to Canvas.
