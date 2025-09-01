# Validity Study for Diagnostic Mathematical Assessment using IRT in R
This repository contains an operational psychometrics project focused on the analysis of the DAACS Reading Assessment (v2.0) data collected between May 2022 and May 2023 from two combined college samples. The project's primary goal was to evaluate the psychometric properties of 180 reading items using bifactor Item Response Theory (IRT) models and to test the items for Differential Item Functioning (DIF) across various demographic groups. The repository includes RMarkdown files documenting the entire research process, from initial data organization and cleaning to missing data analysis, IRT modeling, and logistic regression with factor scores to identify DIF. The included files provide a transparent and reproducible workflow, offering insights into the methodology used to refine the item pool and ensure the validity of the assessment for diverse student populations.
## Data Preparation (Read1_...Rmd)
This RMarkdown file describes the creation of several analytic samples from a combined dataset of 4626 reading assessment participants from UMGC1 and UA2. The key samples created include:

Analytic Sample 1 (AnSamp1): 4523 non-speedy respondents for IRT analyses.
Analytic Sample 2 (AnSamp2): 1563 students with complete demographic data for DIF and group comparisons.
Would-be Sample 2022 (sampW22): 2620 students from 2022 for missing data analysis.

## IRT Analysis (Read2_...Rmd & Read5_...Rmd)
A 2PL Bifactor model was used to analyze the 180 reading items. This model accounts for a general reading ability factor and specific factors for each of the 30 reading passages.
The initial 180-item model was refined to 173 items by removing items with poor general factor discrimination (aG) parameters. This 173-item model was found to fit the data better.
The item pool was further reduced to 124 "good" items that showed no DIF for age. This 124-item model fit better than both the 173-item and 180-item models.
The Proportion of Explained Common Variance (ECV) for the general factor was 64.9% for the 173-item model, indicating that a substantial portion of the variance in item responses is explained by the general reading ability factor.
Theta-Scores: Theta-scores from all three item pools (180, 173, and 124 items) were found to be normally distributed and statistically similar to each other.

## DIF Analysis (Read4_...Rmd)
A DIF analysis for age was conducted on the reading assessment, leading to the identification of 124 "good" items with no DIF.

## Missing Data Analysis (Read3_...Rmd & Read6_...Rmd)
The reading assessment data showed that 39.1% of the demographic data was missing, with systematic missingness from the UMGC1 college.
The missingness of age data was not found to have a significant impact on theta scores in the combined sample, umgc1, or ua2 subsamples, as evidenced by Wilcoxon rank sum tests that showed no significant differences in scores between groups with and without age data. The omnibus tests also found no evidence to reject MCAR.
