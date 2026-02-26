# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose and scope: Document the Climoor climate change manipulation experiment, which uses automated roof technology to create drought and warming treatments reflecting projected UK climate for the next 20–30 years. Site established in 1998; located in Clocaenog Forest, North East Wales; upland moorland with Calluna vulgaris-dominated vegetation and Humo-ferric podzol soil.
- Authors and contact: Original author Alwyn Sowerby; edited by Sabine Reinsch. For data details, contact CEH Bangor (Sabine Reinsch, Bridget Emmett) and refer to on-site data documentation.

## Experimental design and climate treatments

- Treatments and replication:
  - Drought: retractable polyethylene roof reduces rainfall on 4 m x 5 m plots; ~20% annual rainfall reduction; effects vary by event size; operated May–Sept (1999–2011) and Apr–Oct since 2012. Three drought plots.
  - Warming: retractable aluminum mesh curtains over plots, reduces night-time heat loss; rainfall adjustments due to roof retraction after rain; mitigated by rain sensors; ~14% annual rainfall reduction. Three warming plots.
  - Controls: three control plots with scaffolding to mirror shading; total of nine plots (3 per treatment) arranged in blocks (Block mappings provided).
- Operational notes:
  - Wind restrictions: curtains do not operate in winds >10 m/s to prevent damage.
  - Scheduling history: drought period timing and reporting span 1997–2014; warming GDD changes tracked in selected years.
- Site and plot information:
  - Location coordinates and grid references provided; Appendix includes detailed plot and quadrat layouts.

## Data types, datasets, and data collection

- On-site data streams and datasets (typical cadence):
  - AWS meteorological data: daily, 1999–present; sensors for temperature, humidity, rainfall, wind, solar/thermal radiation, pressure; data logged hourly from minute-scale measurements.
  - Micro-meteorological plot data: daily; soil temperature and soil moisture measured at multiple depths; post-2008 using TDR sensors.
  - Rainfall data: storage rain gauge (biweekly site-level rainfall) and rainfall chemistry (biweekly bottles; pH, NO3, Cl, SO4, DOC, NH4 analyses).
  - Throughfall data: plot-level rainfall (biweekly); used to derive plot-specific rainfall by applying percent-change adjustments relative to site rainfall; data gaps infilled with averages in some years.
  - Water table depth: biweekly measurements from 2009 onward using permeable tubes to bedrock.
  - Soil respiration: fortnightly to routine automated measurements; multiple methods over time (CIRAS-2, LICOR LI-8100, automated collars); CO2 flux in mg CO2-C m-2 h-1; collar-based measurements with biomass adjustments.
  - Trace gases (CH4 and N2O): static chamber method using collars; sampling at 0, 15, and 30 minutes; GC analysis; legacy data with variable documentation.
  - Net ecosystem CO2 exchange (NEE): 2002–2004 and 2011 with different chamber systems; flux calculated and corrected for biomass; conversions to mg CO2-C m-2 h-1.
  - Photosynthesis: infrequent measurements (2001–2003); leaf cuvette and CIRAS-2 data; ambient light and standardized light conditions.
  - Vegetation biomass (Pin-point method): years 1998–2012 (and related surveys); three quadrats per plot; 100 pins per quadrat; biomass calibration using species-specific conversion factors.
  - Canopy reflectance: NDVI and PRI from ground-based spectrometry (2001–2002, 2003–2004); spectral bands 400–950 nm; exposure around solar noon.
  - Vegetation phenology, annual growth, and pathogen assessment: 30 leading shoots per species (C. vulgaris, V. myrtillus, E. nigrum); tracking budburst, shoot elongation, leaf counts, and pathogen signs (rust).
  - Vegetation chemistry: elemental analysis (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) for green and litter material.
  - Litterfall: collectors across plots (1999–2002 monthly; later less frequent); conversion to g m-2 and subsequent C/N analyses.
  - Root biomass: multiple methods (soil cores, extraction, WinRHIZO analyses); data 2003–2011 with varying approaches.
  - Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012) with DOC measurements; microbial biomass expressed per g soil organic matter.
  - Nitrogen mineralisation: 1998–2004, paired cores; KCl extractant analysis for NH4 and NO3; mineralisation rates derived from initial/final cores.
  - SOM, SOC and bulk density: cores analyzed for SOM, SOC, and bulk density; conversions to g m-2.
  - Soil solution and leachate chemistry: lysimeters and tensioned samplers (biweekly); analyzes for pH, NO3, Cl, SO4, DOC, NH4.
- Data availability:
  - Not all data stored in EIDC; contact Sabine Reinsch or Bridget Emmett for full details and access.

## Data processing, quality, and provenance

- Processing and unit conversions:
  - Soil respiration: multiple instruments over time; standardized conversions to mg CO2-C m-2 h-1; automatic calculations via HMR in R; linear regression slope used to estimate Rs.
  - NEE and related fluxes: conversions from g CO2 m-2 h-1 and µmol m-2 s-1 to mg CO2-C m-2 h-1 using gas-law based formulas; biomass adjustments applied to fluxes based on measured above-ground biomass.
  - Throughfall adjustments: plot-level rainfall derived by applying percent-change from throughfall to site rainfall; gaps excluded or infilled with year-average reductions.
  - Pin-point biomass: conversion tables (Table 6) linking pin hits to biomass (g m-2) by species; species-specific calibration used to convert to biomass estimates.
- Data quality and limitations:
  - Legacy data: some data processing steps not documented to current best practices; documentation available in supporting RTFs and data sheets.
  - Data gaps and inconsistencies: occasional data loss due to instrument/field issues; some years have incomplete replicates; throughfall data may be excluded if measurements compromised.
  - Instrument changes: multiple generations of sensors and measurement devices; explicit conversion/formula details provided for cross-era comparability.
- Metadata and referencing:
  - Comprehensive dataset-specific documentation available (supporting documents referenced with each dataset).
  - Appendix materials include site layout and quadrat layout for reproducibility.

## Data governance, storage, and sharing recommendations

- Metadata and provenance:
  - Maintain detailed dataset-level metadata including sensor types, data cadence, units, calibration notes, and data provenance.
  - Record instrumentation changes, data processing steps, and any data quality flags or exclusions.
- Accessibility and sharing:
  - Ensure on-site data documentation is mirrored in a centralized data repository (preferably EIDC or CEH Bangor archives).
  - Provide clear access contacts (Sabine Reinsch, Bridget Emmett) and update links for dataset availability.
- interoperability and standards:
  - Preserve consistent units and provide crosswalks for legacy data (e.g., conversions between g CO2 m-2 h-1 and mg CO2-C m-2 h-1; µmol m-2 s-1 to mg CO2-C m-2 h-1).
  - Include detailed methodology for each dataset (sampling frequency, measurement method, QA QC steps) to enable re-use across studies.
- Data limitations disclosure:
  - Explicitly document data gaps (missing years, site-level vs plot-level disparities), legacy data caveats, and any infilling practices.
- Next steps for stewardship:
  - Update and harmonize all data processing notes; ensure all datasets have complete, machine-readable metadata; consider digital object identifiers (DOIs) for datasets and version control.

## Appendix and references

- Appendices include:
  - Appendix 1: Site layout
  - Appendix 2: Quadrat layout and plot quadrats
  - Appendix 3: Plot layout with measurement areas
- Contact points for data access and details: Sabine Reinsch and Bridget Emmett (CEH Bangor); primary dataset contacts per dataset documentation.