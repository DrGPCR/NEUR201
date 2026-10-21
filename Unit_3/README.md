# NEUR 201 — Unit 3

Functional imaging of brain activity, and testing whether a difference between two groups is real.

Everything runs in **Google Colab** in your browser — nothing to install, no Google Drive.
Click a badge and start.

## The story of this unit

In Unit 2, lidocaine blocked Na⁺ channels and made a neuron fire **less**. Now you test a drug expected
to do the opposite: **4-AP**, which blocks K⁺ channels and should make neurons fire **more**. This unit
follows that question from one living brain slice to a group of them:

- **W10 L1** — you watch 100 neurons in a living brain slice light up with calcium, count how often
  they fire before and after 4-AP, alongside a vehicle-control slice.
- **W11 L2** — you ask whether 4-AP's effect is *real*, or whether a gap that size between drug and
  control slices could appear just by chance.

## Notebooks — start here

| Lesson | What you'll do | Open it |
|---|---|---|
| **W10 L1** — Functional imaging: does 4-AP make neurons fire more? | Load a calcium-imaging recording of 100 neurons per slice. Convert raw brightness into **ΔF/F₀**, read a **heatmap** and **trace plots**, detect **calcium events** with a threshold, and turn them into an **event rate** — then see how much that result depends on the threshold you chose. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_3/notebooks/W10L1_Functional_imaging_analysis__STUDENT.ipynb) |
| **W11 L2** — From standard errors to t-tests: is 4-AP's effect real? | Compare 10 drug and 10 control slices. Calculate the **standard error (SEM)**, state the **null and alternative hypotheses**, compute a **t-score** by hand, convert it to a **p-value**, decide whether to **reject H₀**, and plot the result as a bar graph carrying its p-value. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/DrGPCR/NEUR201/blob/main/Unit_3/notebooks/W11L2_Inferential_statistics__STUDENT.ipynb) |

Work through them in order. W10 L1 measures activity in a single slice per group; W11 L2 repeats the
experiment on many slices and asks whether the difference is bigger than chance would produce.

## Before you start

**1. Save your own copy.** When a notebook opens, click **File → Save a copy in Drive** straight
away, or your work won't be saved.

**2. Run every cell, in order, from the top** (**Shift + Enter**).

**3. Watch for these:**

| | What to do |
|---|---|
| **Ordinary cells** | Just run them. |
| **⚙️ Try it** | One per step. Change the value it points to, re-run, and see what changes. |
| **💬 Discussion** | At the end of each notebook. Double-click and type your answers. |

## Submitting your work

1. Answer every question in the **💬 Discussion** at the end.
2. **Runtime → Run all** so every graph and answer is visible.
3. **File → Print → Save as PDF**, then upload the PDF to Canvas.
