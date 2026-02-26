# Nitrous oxide and methane fluxes from different understory treatments in Oil Palm plantations in Riau, Indonesia 2018-2019

## Data access, licensing and citation
- Data are available under the Open Government Licence.
- Access URL: https://doi.org/10.5285/378f028d-ab04-4fa5-a5ca-61f78ea0adb0
- Citation: Drewer, J.; White, S.; Sionita, R.; Pujianto, P. (2020). Nitrous oxide and methane fluxes from different understory treatments in oil palm plantations in Riau, Indonesia 2018-2019. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/378f028d-ab044fa5-a5ca-61f78ea0adb0

## Dataset scope and purpose
- Measures nitrous oxide (N2O), methane (CH4), and carbon dioxide (CO2) fluxes from understory vegetation treatments in a mature oil palm plantation.
- Part of the BEFTA programme; aims to guide plantation management, enable accurate environmental assessments, and inform policy (e.g., RSPO).

## Experimental design
- Location: mature oil palm plantations in Ujung Tanjung and Kandista estates, Sumatra, Indonesia.
- Plot design: 18 plots (2 estates × 9 plots each) in 6 replicate blocks; three understory treatments:
  - Normal complexity (standard herbicide use)
  - Reduced complexity (extensive herbicide spraying)
  - Enhanced complexity (no herbicide, limited understory cutting)
- Sampling regime: 54 static chambers (6 per plot; 9 plots × 6 chambers); measurements monthly over Oct 2018–Sep 2019 (typically 2-day sampling per month).
- GPS coordinates provided for all chamber locations.

## Field collection methods and instrumentation
- Chamber setup: 40 cm diameter collars installed to ~7 cm depth; lids create airtight seals with draft excluder.
- Gas sampling: 0, 15, 30, 45 minutes; 100 mL samples drawn and transferred to 20 mL vials; samples shipped to UKCEH Edinburgh for analysis.
- Additional measurements: soil volumetric moisture (Theta probe) at 7 cm depth at three points per chamber.
- Permits: two Indonesian ministry research permits (RISTEK) covering the project period.

## Analytical methods and quality control
- Gas analysis: Agilent 7890B GC with μECD (N2O) and FID (CH4, CO2).
- Calibration: four-point mixed-gas standards; frequent calibration (~every 20 samples).
- Flux calculation: RCFlux R package evaluating six models; best-fit model selected per chamber; fluxes in μmol m^-2 s^-1 with 95% CIs.
- Data screening: visual QC of six regression models per chamber; outliers retained unless clearly unreliable; flagging mechanism (valid/invalid) for samples as needed.

## Data products and data structure
- BEFTA_GHG_RCflux.csv
  - Contains flux estimates for each chamber and sampling occasion, plus metadata (gas name, treatment, block, location, soil moisture, chamber dimensions, coordinates, elevation, date, best-fit method, model-specific flux values, confidence intervals, R^2, etc.).
- BEFTA_chambers.csv
  - Details of the 54 chambers (codes, treatment, block, year planted, location, and other location descriptors).

## Data provenance and governance
- Field data collected under BEFTA project guidelines; multi-year scope (2018–2019) with standardized protocols.
- Data identifiers, coordinates, and instrument/analysis details documented to support traceability.
- Permits and institutional affiliations noted to support data stewardship and compliance.

## Reuse notes, limitations, and context
- Flux estimates include model-based uncertainties (95% CIs) and are subject to inherent soil microbiome variability.
- Some data points may be invalid or excluded from flux analyses if reliability is in question.
- Study design reflects specific understory management practices in oil palm plantations; consider site specificity when generalizing.
- Data are structured for interoperability (CSV with explicit column definitions) and accompanied by a data dictionary-like description of fields.

## References and related materials
- Related methodological and thematic references listed, including BEFTA programme outputs and soil/greenhouse gas flux methodologies.