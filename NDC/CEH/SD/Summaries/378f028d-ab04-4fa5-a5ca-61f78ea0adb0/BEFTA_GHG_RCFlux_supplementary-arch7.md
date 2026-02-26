# Nitrous oxide and methane fluxes from different understory treatments in Oil Palm plantations in Riau, Indonesia 2018-2019

- A study quantifying greenhouse gas fluxes (N2O, CH4, CO2) from an oil palm plantation under three understory vegetation management treatments (normal complexity, reduced complexity, enhanced complexity) to inform sustainable plantation practices and policy guidance.
- Data collected across two estates (Ujung Tanjung and Kandista) in Riau, Indonesia, during Oct 2018–Sep 2019, using static chambers and gas chromatography, with spatially explicit metadata for GIS analyses.

## Data access, licensing and citation

- Data licensing: Open Government Licence.
- Access: dataset available at https://doi.org/10.5285/378f028d-ab04-4fa5-a5ca-61f78ea0adb0
- Data citation: Drewer, J.; White, S.; Sionita, R.; Pujianto, P. (2020). Nitrous oxide and methane fluxes from different understory treatments in oil palm plantations in Riau, Indonesia 2018-2019. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/378f028d-ab044fa5-a5ca-61f78ea0adb0

## Study context and aims

- Oil palm cultivation is a major agro-economic activity in Southeast Asia with environmental concerns linked to biodiversity loss and greenhouse gas emissions.
- This study investigates how understory vegetation management affects soil GHG fluxes (N2O, CH4, CO2) to support sustainable plantation practices and inform policy makers (e.g., RSPO).
- The BEFTA program (Biodiversity and Ecosystem Function in Tropical Agriculture) provides the broader collaborative framework for this work.

## Experimental design and sampling regime

- Location: mature oil palm plantations at the Ujung Tanjung Estate, Sumatra; two estates (Ujung Tanjung and Kandista).
- Plot design: 18 plots total (9 per estate), each 2.25 hectares, arranged in six replicate blocks.
- Treatments (understory vegetation): 
  - Normal complexity (standard practice; intermediate herbicide spraying)
  - Reduced complexity (highly destructive; herbicide spraying of all understory)
  - Enhanced complexity (conservation; no herbicide, limited understory cutting)
- Chambers: 54 static chambers (six per plot, six replicates per treatment; three inside harvesting circles and three outside).
- Sampling cadence: typically over two days at the end of each month, from Oct 2018 to Sep 2019.

## Field collection methods and laboratory instrumentation

- Chamber setup: PVC collars (40 cm diameter) implanted to ~7 cm depth; lids used to seal with draft excluder; sampling port with three-way tap; 0–45 minute incubation with samples collected at 0, 15, 30, 45 minutes.
- Gas sampling: 100 mL samples drawn and transferred to 20 mL glass vials; samples shipped to UKCEH Edinburgh for GC analysis.
- Additional measurements: soil moisture recorded at 7 cm depth around each chamber using a Theta probe.
- Permits: Foreign Research Permits (two, corresponding to 2018 and 2019) issued by the Indonesian Ministry of Research and Technology/National Research and Innovation Agency (RISTEK).

## Analytical methods and quality control

- Instrumentation: Agilent 7890B gas chromatograph with μECD for N2O and FID for CH4 and CO2.
- Calibration: 4-point mixed gas standards run after roughly every 20 samples.
- Flux calculation: RCFlux R package fitted six models (linear, quadratic, asymptotic, and others) to concentration vs. time data; the best-fit model determined per chamber/gas; fluxes expressed in μmol m^-2 s^-1 with 95% CIs.
- Quality control: visual inspection of RCFlux regression plots; data flagged as valid/invalid; outliers treated conservatively given soil microbiome variability.
- Outputs:
  - BEFTA_GHG_RCflux.csv: fluxes per chamber, per sampling occasion, with multiple model flux estimates, best-fit flux, confidence intervals, model statistics (e.g., adj R^2), year/month/day, location, and metadata (treatment, block, inside/outside circle, soil moisture, chamber dimensions, etc.).
  - BEFTA_chambers.csv: details for all 54 chambers, including BEFTA_code, treatment, block, year_planted, location within/around harvesting circle, and geographic/elevation coordinates.

## Datasets and data structure (key points)

- BEFTA_GHG_RCflux.csv
  - For each chamber (1–54) and sampling occasion (monthly, Oct 2018–Sep 2019)
  - Contains gas names (CH4, CO2, N2O) and six model flux values (flux_linear, flux_quadratic, flux_linear2nd, flux_quadratic2nd, flux_asymptotic, flux_HMR) plus flux_bestfit
  - Includes 95% CIs and adjusted R^2 values for linear/quadratic models
  - Metadata: year, month, day; chamber; treatment; block_number; in_out_circle; soil_moisture; chamber dimensions; GPS coordinates; elevation
- BEFTA_chambers.csv
  - 54 chamber records with: BEFTA_code, treatment, block_number, year_planted, chamber, in_out_circle, location_details, lat, lon, ele_m

## GIS relevance and how to use

- Spatial visualization: map chamber locations with their treatments, inside vs outside harvesting circles, and elevation to explore spatial patterns in GHG fluxes.
- Attribute joins: link BEFTA_GHG_RCflux.csv flux estimates to chamber locations from BEFTA_chambers.csv for map-based analyses by treatment, block, or harvesting circle position.
- Temporal analysis: analyze monthly flux trends (Oct 2018–Sep 2019) by treatment and plot, enabling time-series GIS visualizations.
- Uncertainty assessment: incorporate 95% CIs and best-fit model indicators to assess reliability across plots and treatments.
- Data integration: combine GHG flux data with soil moisture and other GIS layers (vegetation structure, topography, management practices) to model drivers of emissions.

## References and project context

- BEFTA program: Luke et al. (2020) and related BEFTA publications detailing large-scale sustainable oil palm experiments.
- Related methodological references include RCFlux flux estimation (Levy et al., 2011) and prior GHG flux measurement protocols (Drewer et al., 2016; 2017).
- Broader context papers address oil palm expansion, biodiversity, and environmental impacts (e.g., Sayer et al., 2012; Foster et al., 2011).