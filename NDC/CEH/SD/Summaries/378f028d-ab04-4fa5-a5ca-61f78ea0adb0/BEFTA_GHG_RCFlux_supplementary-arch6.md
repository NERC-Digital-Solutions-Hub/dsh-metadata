# Nitrous oxide and methane fluxes from different understory treatments in Oil Palm plantations in Riau, Indonesia 2018-2019

## Data access and licensing
- Data available under the Open Government Licence.
- Access at https://doi.org/10.5285/378f028d-ab04-4fa5-a5ca-61f78ea0adb0.
- Dataset citation: Drewer, J.; White, S.; Sionita, R.; Pujianto, P. (2020). Nitrous oxide and methane fluxes from different understory treatments in oil palm plantations in Riau, Indonesia 2018-2019. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/378f028d-ab044fa5-a5ca-61f78ea0adb0.
- Data files include BEFTA_GHG_RCflux.csv and BEFTA_chambers.csv, with field provenance and GPS coordinates.
- Associated field permits: RISTEK permits 323/SIP/FRP/E5/Dit.KI/X/2018 and 8B/TKPIPA/E5/Dit.KI/VIII/2019.

## Aim and context
- Objective: quantify greenhouse gas emissions (N2O, CH4, CO2) from different understory management treatments in mature oil palm plantations.
- Part of BEFTA (Biodiversity and Ecosystem Function in Tropical Agriculture) programme, a collaboration between University of Cambridge and SMARTRI.
- Study sites: mature oil palm plantations in Ujung Tanjung and Kandista estates, Riau, Sumatra (1987–1989 establishment).

## Experimental design and sampling regime
- 18 plots (2 estates × 9 plots), 2.25 ha each, in six replicate blocks.
- Three understory treatments, each with six replicates:
  - Normal complexity: standard herbicide use in understory.
  - Reduced complexity: complete understory destruction with herbicides.
  - Enhanced complexity: no understory herbicide; limited understory cutting.
- 54 static chambers deployed (6 chambers per plot, across harvesting circles and outside).
- Measurements: N2O, CH4, CO2 via static chambers, usually over two days per month from Oct 2018 to Sep 2019.

## Field collection methods and laboratory instrumentation
- Chamber setup: 40 cm diameter collars inserted ~7 cm deep; lids used to create airtight closures; sampling at 0, 15, 30, 45 minutes.
- Sample handling: 100 mL samples drawn into syringes and transferred to 20 mL vials; shipped to UKCEH Edinburgh for analysis.
- Gas analysis: GC with μECD for N2O and FID for CH4 and CO2.
- Calibration: 4-point standards (CH4, CO2, N2O) analyzed after ~every 20 samples.
- Soil moisture: measured with Theta probe at 7 cm depth.
- Compliance: field permits documented; two-year sampling period covered by permits.

## Analytical methods, calibration and quality control
- Flux calculations: using RCFlux R package; six regression models (linear, quadratic, asymptotic, and HM R variants) with best-fit selected by highest R-squared.
- Flux units: μmol m^-2 s^-1; 95% CI provided per flux estimate.
- Quality control: visual review of regression plots; data flagged as valid/invalid; outliers treated cautiously due to soil microbiome variability.
- Calibration details: four-point gas standards; periodic recalibration during GC runs.

## Data files and structure
- BEFTA_GHG_RCflux.csv
  - Contains fluxes for each chamber (1–54) across sampling occasions (Oct 2018 – Sep 2019).
  - Key columns: gasName, flux_linear, flux_quadratic, flux_linear2nd, flux_quadratic2nd, flux_asymptotic, flux_HMR, flux_bestfit, ci95lo_* and ci95hi_*, adjr2_* for each model, bestFitMethod, year, mon, mday, chamber, treatment, block_number, in_out_circle, soil_moisture, chamber dimensions (diameter_cm, height_cm, area_m2, volume_m3), location (lat, lon, ele_m).
- BEFTA_chambers.csv
  - Details of the 54 static chambers.
  - Key columns: BEFTA_code, treatment, block_number, year_planted, chamber, in_out_circle, location_details, lat, lon, ele_m.

## How to use the data (data support perspective)
- Data can be used to compare understory treatments in terms of N2O and CH4 fluxes across time (monthly 2018–2019) and spatial blocks.
- Use BEFTA_GHG_RCflux.csv for model-based flux best estimates and uncertainty (95% CI) per chamber and sampling date.
- Use BEFTA_chambers.csv to link flux data to exact chamber locations, treatment, block, and plot context.
- Consider multiple flux models; prefer flux_bestfit and consult ci95 ranges for uncertainty.
- Combine with environmental covariates (soil moisture, location coordinates, altitude) to explore drivers of GHG flux variability.
- Data licensing permits reuse under Open Government Licence with proper citation.
- Useful for informing plantation management decisions and policy discussions on understory management and GHG emissions in oil palm landscapes.

## Limitations and considerations
- Data quality may vary due to inherent soil microbiome variability; some samples flagged as invalid.
- Flux estimates come from multiple regression models; interpretation should consider model selection and uncertainty.
- Spatial coverage is constrained to two estates within a defined BEFTA study area; extrapolation beyond this context should be done cautiously.

## References and related materials
- BEFTA programme publications and dataset citations provided within the data access notice.
- Primary dataset citation: Drewer et al. (2020) NERC Environmental Information Data Centre. Dataset: Nitrous oxide and methane fluxes from different understory treatments in oil palm plantations in Riau, Indonesia 2018-2019.
- Related methodological references include RCFlux framework and prior BEFTA outputs.