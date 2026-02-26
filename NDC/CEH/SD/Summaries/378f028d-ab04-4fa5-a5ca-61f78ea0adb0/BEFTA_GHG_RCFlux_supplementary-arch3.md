# Nitrous oxide and methane fluxes from different understory treatments in Oil Palm plantations in Riau, Indonesia 2018-2019

- Purpose and scope
  - Quantify greenhouse gas (GHG) fluxes (N2O, CH4, CO2) under three understory management regimes in mature oil palm plantations.
  - Provide data to inform environmental assessments and policy guidance (e.g., RSPO) on understory management and biodiversity co-benefits.

- Study design
  - BEFTA programme collaboration between University of Cambridge and SMARTRI.
  - Location: mature oil palm plantations in Ujung Tanjung and Kandista, Riau, Sumatra.
  - Plots: 18 plots of 2.25 ha across two estates (9 plots per estate).
  - Treatments: six replicate blocks of three understory treatments — Normal complexity (standard practice), Reduced complexity (extensive herbicide use), Enhanced complexity (no herbicide, limited understory cutting).
  - Measurement framework: 54 static chambers (6 per plot) deployed to capture fluxes inside and outside harvesting circles.
  - Temporal scope: monthly measurements over Oct 2018–Sep 2019, typically over two days per month.

- Methods and instrumentation
  - Field collection: 40 cm diameter, ~7 cm deep chamber collars; airtight closure with lid and draft-excluder; sampling at 0, 15, 30, 45 minutes.
  - Gas analysis: GC with μECD for N2O and FID for CH4 and CO2; calibration with four-point gas standards.
  - Supporting measurements: soil moisture (Theta probe) at sampling.
  - Data handling: fluxes computed using RCFlux R package with multiple regression models; best-fit model selected; results include 95% confidence intervals.
  - Permits: Indonesian Ministry of Research and Technology permits covering the two-year study period.

- Data products and structure
  - BEFTA_GHG_RCflux.csv
    - Contains flux estimates for each chamber and sampling occasion, for each gas, across multiple models and the best-fit model.
    - Key fields: gasName, flux estimates (linear, quadratic, various models), ci95, adjr2, bestFitMethod, date, chamber, treatment, location (block, in/out circle), soil_moisture, chamber dimensions, geographic coordinates, elevation.
  - BEFTA_chambers.csv
    - Details of all 54 static chambers: chamber identifiers, treatment, block number, year planted, location coordinates, and chamber elevation.
  - Datasets include extensive metadata describing measurement context, location, and apparatus.

- Data access, licensing and citation
  - Access: Open Government Licence; dataset available at the provided DOI.
  - Citation: Drewer et al. (2020). Nitrous oxide and methane fluxes from different understory treatments in oil palm plantations in Riau, Indonesia 2018-2019. NERC Environmental Information Data Centre.

- Quality control and calibration
  - Calibration: four-point calibration with mixed gas standards roughly every 20 samples.
  - Data validation: visual QC of regression flux plots; outliers flagged as valid/invalid; flux calculations rely on statistically robust best-fit models (linear, quadratic, or other provided in RCFlux).
  - Uncertainty: 95% confidence intervals accompany all flux estimates.

- Relevance to monitoring frameworks and policy
  - Demonstrates a concrete workflow for monitoring GHG fluxes in agricultural tropical ecosystems, combining in-field measurement, laboratory analysis, and model-based flux estimation.
  - Shows how standardized metadata, data provenance, and open data sharing support policy scrutiny and future decision-making.
  - Highlights the importance of data governance, metadata completeness, and openness to enable cross-study comparability and reuse in monitoring frameworks.

- Challenges and considerations for monitoring frameworks
  - Data gaps and access barriers can hinder timely decision-making.
  - Organizational silos may impede data sharing across institutions.
  - Requiring public data sharing can be a barrier for some datasets.
  - Metadata adequacy is critical to verify data suitability for monitoring needs.
  - Data transformation and harmonization efforts are often needed to integrate datasets into broader monitoring systems.
  - Establishing data governance processes is essential to ensure data quality, storage, sharing, and ongoing updates.