# Bootstrapped Loess regression for soil depth profile comparison

- Purpose: Provide a non-parametric method to compare soil depth profiles and test for significant differences across land use transitions, accommodating non-linear profiles and avoiding parametric distribution assumptions; designed for general applicability across land uses and soil types.

- Core approach: Bootstrapped Loess Regressions (BLR)
  - Build an empty matrix to store Loess-predicted depth profiles from bootstrap samples.
  - Draw bootstrap samples from the union of data for the two land uses being compared and generate a confidence envelope representing the null hypothesis of no difference (P > 0.05).
  - Fit Loess predictions for the second land use alone; if this line falls outside the envelope, infer a significant difference.
  - Compute an overall P value by normalizing test statistics across bootstrap samples and taking the relevant percentile from bootstrapping of the second land use only.

- Data and example dataset
  - Dataset: LUC.soil.data.csv, used to illustrate the BLR approach; originates from a land-use change study in the UK focused on soil carbon under bioenergy crops.
  - Land uses: arable vs. Short-Rotation Coppice willow (SRC willow); a single LUC transition within a larger study.
  - Sampling design: nine nested sampling locations per field; three plots per land use; three soil cores per plot; cores taken at multiple depth increments (0–10 cm, 10–20 cm, etc.) with measurements of soil mass, soil carbon concentration, and soil C stock.
  - Depth profile data: depth.number (depth increment index) and depth.increment (depth range in cm) with corresponding soil C metrics.

- Outputs and visualization
  - Graphical outputs showing depth-profile comparisons with BLR-derived envelopes (confidence envelopes) and the second land use Loess path relative to the envelope.
  - Figure example (Figure 1) demonstrates BLR graphical output for comparing depth profiles of soil C content.

- Implementation details
  - Software: R statistical environment.
  - Code availability: BLR_example_code.R provides two examples of applying the BLR method.
  - Process steps: construct matrix for bootstrap Loess predictions, generate envelope under the null, assess significance by envelope crossing, and compute an overall P value.

- Context and acknowledgments
  - Example data drawn from ELUM (Ecosystem Land Use Modelling & Soil Carbon GHG Flux Trial) project; funded by the Energy Technologies Institute (ETI).

- Relevance for environmental monitoring
  - Supplies a standardised, non-parametric framework to compare soil depth profiles over land-use transitions.
  - Facilitates robust detection of differences in soil carbon profiles, aiding environmental health assessments and policy evaluations.
  - Emphasizes reproducibility and potential data reuse through openly demonstrated methods and datasets.