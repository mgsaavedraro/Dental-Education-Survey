# Dental Education Survey - CariesCare International (CCI) process evaluation

Analysis code and de-identified data for the manuscript *"One-Year Adoption of CariesCare International in Latin American Dental Schools:
A Process Evaluation"* (European Journal of Dental Education). After one academic year, the implementation of CCI and a digital oral-health
record (D-OHR) was evaluated among students and educators of seven Latin American dental-school clinics (implementation outcomes, Treatment
Evaluation Inventory, clinical adherence).

> **Revision note.** The analysis was corrected during peer review (`docs/revision_note.md`). The previous analysis is archived, unchanged,
> in `archive/previous_analysis/` and should not be used.

## Study population

| | n |
|---|---|
| Initial students | 71 |
| Withdrew | 7 |
| Without patients (could not complete the clinical implementation) | 4 |
| Students who completed the study | 60 (84.5%) |
| Educators | 16 |
| **Final participant-level analytic N** | **76** |
| D-OHRs selected for adherence (one per completed student) / assessable | 60 / 50 |

Each row of the analytic dataset is one participant: the CCI, D-OHR and TEI responses are linked within respondent.

## Repository structure

```
README.md, Dental-Education-Survey.Rproj, .gitignore
analysis/   CCI_Process_Evaluation_Final.Rmd        (renders all tables, Figure 1 and the reported numbers)
data/processed/
            CCI_final_participant_level_deidentified.csv   (76 rows: participant_code, respondent_group, dental_school, 51 items coded 1-5)
            CCI_final_adherence_deidentified.csv           (60 rows: one selected D-OHR per completed student; criteria 1 = adherent,
                                                            0 = not adherent, NA = not applicable or record not assessable)
data/raw/   (not public)
docs/       data_dictionary.xlsx, revision_note.md
outputs/    figures/Figure1_final.(pdf|png); tables/*.xlsx
session/    sessionInfo.txt
archive/previous_analysis/   superseded script, RDS objects, outputs and figures
```

## Requirements

R 4.3.3 (used for the final analysis) or later. Packages: readxl, dplyr, tidyr, purrr, stringr, stringi, tibble, janitor, knitr,
rmarkdown, psych, FactoMineR, factoextra, missMDA, polycor, ggplot2, ggpubr, MASS, writexl, jsonlite (versions in `session/sessionInfo.txt`).

## How to reproduce

1. Clone the repository and open `Dental-Education-Survey.Rproj`.
2. `rmarkdown::render("analysis/CCI_Process_Evaluation_Final.Rmd")` (about 15 minutes; the bootstrap uses a fixed seed).
3. Outputs are written to `analysis/`. Age and sex are not public, so the age/sex cells of Table 1 are not reproduced from the public files.

## Expected results

76 participants; no missing item responses and no imputation; MFA Dim1 43.0%, Dim2 22.6% (cumulative 65.6%);
adherence 134/187 applicable decisions (71.7%); TEI Cronbach's alpha 0.884 (students) and 0.78 (educators).
The Rmd stops with an error if participant counts, codes, Likert values or item counts differ from these specifications.

## De-identification and confidentiality

Only coded questionnaire items, respondent role, a sequential participant code and a school code (DS1-DS7) are published. Names, e-mail
addresses, institution names, free-text answers, age, sex and patient information are not included. The correspondence between school codes
and institutions is confidential and is not published.
