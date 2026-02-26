# Nitrous oxide and methane fluxes from different understory treatments in Oil Palm plantations in Riau, Indonesia 2018-2019

- Purpose and relevance: Quantify greenhouse gas fluxes (N2O, CH4, CO2) under different understory management treatments in mature oil palm plantations to inform environmental assessments and policy guidance (e.g., RSPO) and to support sustainable plantation practices.

- Data access and licensing:
  - Open Government Licence; dataset accessible at the provided DOI.
  - Data must be cited as: Drewer et al. 2020, BEFTA dataset (NERC Environmental Information Data Centre).
  - Two primary data files described: BEFTA_GHG_RCflux.csv and BEFTA_chambers.csv.
  - Includes metadata on variables, units, and data provenance; governed by project permits.

- Datasets and structure (data assets):
  - BEFTA_GHG_RCflux.csv
    - Contains flux estimates for each chamber and sampling occasion across six modeling methods plus best-fit, with 95% CIs and model performance metrics (e.g., adj. R2).
    - Key fields: gasName, flux values for linear/quadratic/2nd/other methods, flux_bestfit, ci95lo/hi, adjr2 values, bestFitMethod, year, mon, mday, chamber, treatment, block_number, in_out_circle, soil_moisture, chamber dimensions (diameter, height, area, volume), lat/lon, ele, and location metadata.
  - BEFTA_chambers.csv
    - Details for the 54 static chambers (Chamber locations and contextual info).
    - Key fields: BEFTA_code, treatment, block_number, year_planted, chamber, in_out_circle, location_details, lat, lon, ele.

- Experimental design and field sampling:
  - BEFTA program collaboration between University of Cambridge and SMARTRI; part of BEFTA biodiversity and ecosystem function research.
  - Study site: mature oil palm plantations in Ujung Tanjung Estate and Kandista, Sumatra (established 1987–1989).
  - 18 plots (2 estates, 9 per estate) across 6 replicate blocks.
  - Three understory treatments:
    - Normal complexity: standard herbicide use (intermediate understory management).
    - Reduced complexity: heavy disturbance; complete understory herbicide spraying.
    - Enhanced complexity: conservation approach; no understory herbicide; limited understory cutting.
  - Gas measurements: N2O, CH4, CO2 using static chambers (40 cm diameter) with 7 cm insertion depth; 54 chambers (6 per plot across 9 plots) with inside/outside harvesting circle placement.
  - Sampling regime: usually over two days each month from Oct 2018 to Sep 2019.

- Field collection methods and instrumentation:
  - Chamber setup: fixed collars installed at start; lids closed to form an air-tight seal; sampling port and pressure compensation fitted.
  - Sampling protocol: 100 mL samples drawn at 0, 15, 30, 45 minutes; samples transferred to 20 mL vials for GC analysis.
  - Gas analysis: UKCEH Edinburgh analyzed samples with GC (μECD for N2O, FID for CH4/CO2).
  - Complementary measurements: volumetric soil moisture at three points per chamber.
  - Permits: Indonesian foreign research permits (RISTEK) for 2018 and 2019.

- Data processing and quality control:
  - Analytical setup: Calibration with four-point mixed gas standards; concentrations converted to fluxes via RCFlux (R package) using six regression models; best-fit model selected per chamber.
  - Flux units: micromoles per square meter per second (μmol m−2 s−1); fluxes include 95% confidence intervals.
  - Quality control: visual inspection of RCFlux regression plots; invalid samples flagged and excluded as needed; most flux estimates rely on linear or HM(R) models.
  - Data outputs include both model-specific flux estimates and the best-fit flux for each chamber and sampling event.

- Data governance, provenance, and updates:
  - Data linked to BEFTA programme publications and Frontiers in Forests and Global Change (2020) and related BEFTA literature.
  - Two-year study window with monthly sampling; metadata includes location, date, and chamber details for traceability.
  - Data files contain explicit column definitions to support discoverability and reuse.

- Practical considerations for data leaders:
  - Ensuring data assets are properly formatted, with clear metadata and field definitions for discoverability and reuse.
  - Understanding data provenance: field methods, calibration steps, and QC procedures to assess reliability and comparability with other datasets.
  - Licensing and citation requirements for reuse; explicit linkage to permits and governance documents.
  - Potential data gaps: variability in soil microbiome, occasional data exclusions, and model-based flux estimates with associated uncertainties.