# NEUR 201 — Unit 1

Coding activities for **NEUR 201: Research Methods & Data Analysis for Cellular Neuroscience**.

Everything runs in **Google Colab** in your browser. There is nothing to install and no
Google Drive to connect — click a badge below and start.

## Notebooks — start here

| Lesson | What you'll do | Open it |
|---|---|---|
| **W1 L2** — Intro to Jupyter & Python | No data needed. Learn how notebooks work, and the Python you'll see all term. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W1L2_Intro_to_Jupyter_and_Python__STUDENT.ipynb) |
| **W2 L2** — Colocalization analysis | Process a real confocal image: find Olig2⁺, Ki67⁺, and double-positive cells. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W2L2_Colocalization_analysis__STUDENT.ipynb) |
| **W3 L1** — Frequency tables & graphs | Turn a column of numbers into a distribution you can see. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W3L1_Frequency_tables_and_graphs__STUDENT.ipynb) |
| **W3 L2** — Measures of central tendency | Mean, median, and mode — and when each one misleads you. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W3L2_Measures_of_central_tendency__STUDENT.ipynb) |
| **W4 L1** — Measures of dispersion | Range, IQR, variance, and standard deviation. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_1/notebooks/W4L1_Measures_of_dispersion__STUDENT.ipynb) |


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

Sections of **cortex** and **hippocampus** were taken from control animals (**CON**)
and drug-treated animals (**DRUG**), and stained for two markers:

- **Olig2** (AF488 / green) — marks **oligodendrocyte-lineage** cells
- **Ki67** (AF647 / far-red) — marks cells that are **actively dividing**

A cell positive for **both** is a *proliferating oligodendrocyte-lineage cell*. In W2 L2 you
measure those cells in a real image. In W3 and W4 you analyse a table of results pooled from
the whole class.
