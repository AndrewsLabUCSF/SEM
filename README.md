# Orthogonal Contributions of Genetic, Clinical, and SDoH Risk Burdens on Alzheimer's Disease Pathology

This repository contains the analysis workflow for a cross-sectional structural equation modeling (SEM) study of multidomain Alzheimer's disease (AD) risk in the Health and Aging Brain Study–Health Disparities (HABS-HD). The project evaluates the independent contributions of genetic risk (APOE ε4 and an ADPRS), clinical risk burden (CogDRisk), and adverse social determinants of health (SDoH) to latent Aβ/tau pathology, neurodegeneration, and cognition.

The analyses use baseline Visit 1 data from HABS-HD. The primary analysis includes 2,173 participants; sensitivity analyses use the broader cohort (N = 3,116) with full-information maximum likelihood (FIML) to handle missing exogenous variables. The workflow also includes sex- and race/ethnicity-stratified analyses and invariance tests for the stratified analyses.

# Data
### Description

This project uses HABS-HD, an ongoing community-based cohort that includes non-Hispanic White, non-Hispanic Black, and Hispanic/Latinx older adults. The analytic data combine demographics, clinical and lifestyle measures, social determinants of health, genotype-derived variables, plasma biomarkers, neuroimaging, and neuropsychological measures.

### Data Source

- **Repository/Cohort:** Health and Aging Brain Study–Health Disparities (HABS-HD)
- **Study site:** University of North Texas Health Science Center, Fort Worth, Texas
- **Access:** HABS-HD data are controlled-access research data and are not distributed in this repository.

...

# Workflow/Scripts

1. **`sdoh.qmd` — SDoH latent-variable construction**  
   Splits the cohort into EFA/CFA samples; evaluates candidate SDoH indicators and factorability; performs EFA; fits the SDoH CFA using WLSMV for ordered indicators; fits the final second-order SDoH model in the total sample; extracts AX (anxiety), HEA (healthcare/economic adversity), SA (social adversity), and overall SDoH factor scores for each participant.

2. **`latent_analysis.qmd` — AD latent variables and main SEM analysis**  
   Fits the measurement model for Aβ/tau, neurodegeneration, and cognition; estimates the full SEM; performs sex- and race/ethnicity-stratified models; evaluates latent-score distributions; conducts FIML sensitivity analyses.

3. **`invariance.qmd` — multigroup invariance testing**  
   Compares models with structural regression paths freely estimated versus constrained across sex and race/ethnicity groups. Likelihood-ratio tests are used to assess whether structural paths differ across groups.

4. **`characteristics.qmd` — descriptive characteristics**  
   Descriptive summaries for the analytic cohort.

# Results

Outputs currently generated or referenced by the workflow include:

- SDoH EFA/CFA structures and the final second-order SDoH model.
- CFA results for the three AD-related latent variables.
- Full-cohort SEM estimates and model-fit statistics.
- Sex- and race/ethnicity-stratified SEM results.
- Multigroup likelihood-ratio tests for invariance testing.
- FIML sensitivity analyses.
- Latent-score distribution plots.

Participant-level source data are not stored here.


# Acknowledgement

The authors would like to thank all the participants, staff, researcher teams, and partners of the Health & Aging Brain Study - Health Disparities (HABS-HD). The HABS-HD is supported by the National Institute on Aging of the National Institutes of Health under Award Numbers R01AG054073, R01AG058533, R01AG070862, P41EB015922, and U19AG078109. The content is solely the responsibility of the authors and does not necessarily represent the official views of the National Institutes of Health. We gratefully acknowledge the contributions of our study partners and their families, whose help and participation made this work possible.

This work is supported by NACC P0568207, NIH-NIA R01AG057234, P30AG062422, P01AG019724, and U19AG079774; NIH-NINDS U54NS123985

