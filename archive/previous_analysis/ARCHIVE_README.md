# Previous analysis (archived, superseded)

This folder preserves the superseded analysis script and associated historical outputs and figures from the analysis reported in the originally submitted manuscript (repository state at commit 5c83257). The two RDS objects used by the original script (`Data/survey_db.rds` and `Data/db_by_instrument.rds`) are not retained in the current repository tree. Their historical role is documented here for transparency. The corrected de-identified analytical datasets are available under `data/processed/`.

They are superseded and must not be used for inference. During the peer-review reproducibility audit it was found that this script
concatenated the instrument-specific datasets (CCI, D-OHR, TEI) by rows instead of linking them within respondents, which created
structural missing values that then entered the mode-imputation step; the RDS objects also contained a coding discrepancy in four
educator adoption/maintenance variables. The current analysis is `analysis/CCI_Process_Evaluation_Final.Rmd` (see docs/revision_note.md).
