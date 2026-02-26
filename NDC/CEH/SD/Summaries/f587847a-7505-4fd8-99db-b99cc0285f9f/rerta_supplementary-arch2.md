# Nitrous oxide and methane fluxes from different riparian restoration treatments in Oil Palm plantations in Riau, Indonesia 2019-2021

## Aim
- Quantify greenhouse gas emissions (N2O, CH4, and CO2) from four riparian buffer treatments in oil palm plantations.
- Provide guidance to oil palm growers and inform policymakers on the environmental impact of riparian management techniques.

## Context and study design
- Part of the Riparian Ecosystem Restoration in Tropical Agriculture (RERTA) project within BEFTA, a collaboration between University of Cambridge and SMARTRI.
- Two experimental sites exist; the present greenhouse gas study was conducted at the Ujung Tanjung estate.
- Four treatments tested in 50 x 400 m river-adjacent zones (on both sides of the river): 
  1) Immature oil palm – no restoration, replanting to river margin
  2) Mature oil palm – no restoration, maintain a 50 m buffer
  3) Native trees – enrichment planting with forest trees in a 50 m buffer, remove all mature oil palm
  4) Mature oil palm and native trees – enrichment planting with forest trees in a 50 m buffer, maintain mature oil palm
- Experimental setup: 40 static chambers total (6 replicates per treatment, plus 16 in surrounding plantation), with hourly GPS-located coordinates and treatment zones recorded.
- Sampling period: January 2019 to September 2021, with a break April–Oct 2019 for felling/replanting and another break Jan–Jun 2021 due to Covid-19.

## Field collection methods
- Chambers: round collars 40 cm in diameter, inserted to ~7 cm depth; lids create airtight closures with draft excluders; sampling ports and pressure compensation included.
- Sampling schedule: 100 mL samples drawn at 0, 15, 30, and 45 minutes during a 45-minute incubation; samples stored in 20 mL vials for transport.
- Ancillary measurements: volumetric soil moisture measured at the time of sampling (3 points around each chamber).
- Permits: Foreign Research Permit, with two RISTEK permit numbers covering different project years.

## Laboratory analysis and calibration
- Gas analysis: UKCEH Edinburgh performed on an Agilent 7890B GC with μECD for N2O and FID for CH4 and CO2.
- Calibration: four-point calibration using mixed gas standards with known concentrations; calibration runs after every ~20 samples.
- Flux calculation: using RCFlux R package, fitting six regression models per chamber and selecting the best-fit model (highest R-squared). Fluxes expressed as μmol m−2 s−1 with 95% confidence intervals.
- Data quality: flux regression plots visually inspected; data flagged as invalid only if clearly unreliable; otherwise, outliers retained due to natural soil microbiome variability.

## Data outputs and structure
- rerta_ghg_rcflux.csv
  - Fluxes for each chamber (1–40) on each sampling occasion (monthly: Jan 2019–Sep 2021).
  - Columns include gas name, multiple flux estimates from different models, best-fit method, 95% CIs, adjusted R2 values, year/month/date, chamber and location metadata, and soil moisture.
  - Missing data represented as NA where appropriate.
- rerta_chambers.csv
  - Details of the 40 static chambers (RERTA_code, position, plot, treatment_zone, treatment, date_planted, date_installed, lat, lon, ele, etc.).
- Data context
  - Includes notes on how to interpret column headings, units, and the various metadata fields used across the dataset.
  - Tables referenced for calibration concentrations and model details are described in the text (with exact concentrations and model options).

## Data management and accessibility
- Data are organized to support reproducibility and cross-chamber comparisons.
- The project emphasizes storing and uploading datasets to appropriate data portals for ongoing accessibility and reuse.

## Methods and QA details (summary)
- Field equipment and sampling protocol standardized to enable consistent measurements across treatments and time.
- Gas concentrations calibrated against known standards; fluxes computed with multiple regression approaches and the best fit selected.
- Quality control includes visual assessment of regression outputs and a conservative approach to handling questionable data points.

## Relevance to policy and practice
- Riparian buffers are known to improve water quality and biodiversity; this study extends understanding to greenhouse gas emissions.
- Findings intended to inform policy discussions on riparian restoration mandates and certification standards (e.g., RSPO) by clarifying environmental trade-offs related to GHG fluxes.

## Limitations and contextual notes
- Sampling gaps corresponding to plantation replanting and Covid-19 restrictions may affect continuity.
- Variability inherent in soil microbiomes means some fluxes have broader confidence intervals and require careful interpretation.

## References (contextual)
- Drewer et al. on related GHG flux studies in tropical systems and oil palm contexts.
- Methodological references for RCFlux, calibration, and gas chromatography approaches.
- Supporting literature on riparian buffers, biodiversity, and land-use changes in oil palm landscapes.