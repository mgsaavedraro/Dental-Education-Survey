# Previous analysis (archived, superseded)

This folder keeps, unchanged, the files of the analysis reported in the originally submitted manuscript (repository state at commit 5c83257):
`MultivariateAnalysis.Rmd`, `Data/survey_db.rds`, `Data/db_by_instrument.rds`, `outputs/` and `figures/`.

They are superseded and must not be used for inference. During the peer-review reproducibility audit it was found that this script
concatenated the instrument-specific datasets (CCI, D-OHR, TEI) by rows instead of linking them within respondents, which created
structural missing values that then entered the mode-imputation step; the RDS objects also contained a coding discrepancy in four
educator adoption/maintenance variables. The current analysis is `analysis/CCI_Process_Evaluation_Final.Rmd` (see docs/revision_note.md).
