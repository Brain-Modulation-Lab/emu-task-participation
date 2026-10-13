# EMU Task Participation

Which experimental tasks each EMU participant took part in, as a tasks × participants
check matrix.

**Live page:** https://brain-modulation-lab.github.io/emu-task-participation/

128 participants · 49 tasks · 450 task runs · 3.5 tasks per participant.

`index.html` is fully self-contained — it inlines its own data and loads nothing
externally, so it also works opened straight from disk or sent as an email attachment.

## Reading it

Rows are tasks, columns are participants, a check means the participant is listed for
that task. The right-hand bar is the per-task count; the bottom row is tasks per
participant. Hover any cell for the pair, filter tasks, re-sort rows and columns, toggle
dark mode, or export the matrix as CSV.

## Task names

The source `tasks` column is free text: roughly 120 distinct spellings for 49 tasks.
Variants were folded into one canonical task in three passes — case/spacing/typo fixes,
then trailing run numbers stripped for a known list of stems, so **a check means "ran
this task at least once", not a run count**.

11 look-alike names were deliberately **left as separate rows**, because merging them is
a research call rather than a typo fix:

| Name | n | Why |
|---|---|---|
| `ToM2` | 11 | may be a different paradigm, not a 2nd run of `ToM` |
| `esfMRI-bedside-stim` | 10 | stim vs non-stim bedside kept separate |
| `Olfaction` | 1 | could be `Olfactory/Gustatory` or `Olfactometer` |
| `Language_Localizer` | 1 | could be `LangLoc`, modality unspecified |
| `Mapping` | 1 | could be `ClinicalLangMapping` |
| `ESfMRI-plan` | 1 | a planning session, not a scan |
| `esfMRI-from-MIT` | 1 | provenance-tagged, site unclear |
| `AM`, `FN`, `LMM`, `aAAC` | 1 each | unexplained abbreviations (`LMM` possibly `LangMathMusic`) |

Hover a task name marked `◦` in the page to see the variants it absorbed.

Three participants are omitted for having no task listed.

## Source

Generated from `participants.csv` by `task-participation-viz/prepare_task_participation.py`
in the private `Brain-Modulation-Lab/seeg-visualization` repository. This repository holds
only the rendered page; regenerate it there and copy `index.html` across.
