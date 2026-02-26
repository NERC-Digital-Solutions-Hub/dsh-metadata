# Nitrous oxide and methane fluxes from different understory treatments in Oil Palm plantations in Riau, Indonesia 2018-2019

## Aim
- Quantify greenhouse gas (N2O, CH4, CO2) fluxes under different understory management in mature oil palm plantations.
- Provide first steps toward guidance for plantation managers and policy makers (e.g., RSPO) and enable accurate environmental assessments.

## Data access, licensing and citation
- Open Government Licence; dataset accessible via doi: 10.5285/378f028d-ab04-4fa5-a5ca-61f78ea0adb0
- Citation required: Drewer et al. (2020). BEFTA dataset. NERC Environmental Information Data Centre.

## Experimental design / sampling regime
- Part of BEFTA programme (University of Cambridge + SMARTRI).
- Location: mature oil palm plantations in Ujung Tanjung Estate and Kandista, Riau, Sumatra.
- Plot design: 18 plots (2.25 ha each) across two estates; six replicate blocks; three understory treatments:
  - Normal complexity (standard practice; intermediate herbicide use)
  - Reduced complexity (extensive herbicide spraying; destructive)
  - Enhanced complexity (no herbicide; limited understory cutting)
- Measurements: six static chambers per plot (total 54 chambers) across three treatment types; inside and outside harvesting circles.
- Temporal coverage: monthly measurements from October 2018 to September 2019.

## Field collection methods
- Chamber setup: round collars (40 cm diameter) inserted to ~7 cm depth; lids with airtight seal; sampling port and pressure compensation plug.
- Sampling: 100 mL samples collected at 0, 15, 30, 45 minutes; transferred to 20 mL vials.
- Analysis: samples shipped to UKCEH Edinburgh for gas chromatography.
- In situ measurements: soil moisture (Θ) at ~7 cm depth at three points per chamber.
- Permits: two Indonesian research permits covering the two-year study period (RISTEK numbers provided).

## Analytical methods and quality control
- Gas analysis: Agilent 7890B GC with μECD (N2O) and FID (CH4, CO2).
- Calibration: four-point mixed-gas standards (CH4, CO2, N2O) analyzed after ~every 20 samples.
- Flux calculation: RCFlux R package applying six regression models; best-fit model selected based on R-squared; fluxes expressed as μmol m^-2 s^-1 with 95% CI.
- Quality control: visual check of regression plots; data flagged valid/invalid; outliers treated conservatively due to natural soil microbiome variability.
- Outputs: fluxes for each chamber and sampling occasion; multiple model flux values plus best-fit flux.

## Data outputs and structure
- BEFTA_GHG_RCflux.csv
  - Contains flux estimates for each chamber (54 total) across monthly sampling (Oct 2018 – Sep 2019) for each gas (N2O, CH4, CO2) and metadata (treatment, block, location, soil moisture, chamber dimensions, coordinates, etc.).
  - Includes: best-fit flux, six model fluxes, 95% CIs, adjusted R^2, best-fit method code, date, chamber, location details, and environmental variables.
- BEFTA_chambers.csv
  - Details of the 54 static chambers: BEFTA_code, treatment, block, year planted, chamber ID, location relative to harvesting circle, location details, coordinates, elevation.

## Calibration and data details
- Calibration: 4-point standards for CH4, CO2, N2O; regular calibration around sample runs.
- Data structure: comprehensive columns documenting gas, flux estimates by method, confidence intervals, fit statistics, and linking metadata (location, treatment, year, date, chamber).

## Permits and governance
- Data collected under Indonesian foreign research permits (RISTEK) for 2018 and 2019.

## Relevance to environment monitoring and policy
- Demonstrates a standardised approach to capturing GHG fluxes in agricultural ecosystems, enabling cross-site comparability and longitudinal monitoring.
- Aligns with the Analysts Monitoring the Environment aim: verified data from established sources, quality assured, transformed into usable outputs (datasets, maps, charts), and stored for access.
- Highlights ongoing challenges and opportunities:
  - Increasing the value of monitoring datasets by integrating with additional datasets (e.g., biodiversity, soil health, fertilizer inputs).
  - Enhancing accessibility to underlying data to support broader analysis and policy assessment.