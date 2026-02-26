# Field sites and microclimate measurements

## Overview
- Field study conducted at six forest reserve stands in the Northern Boreal zone of Sweden, varying in age since last wildfire (47 to 367 years). 
- Sites selected for similar soil types and vegetation (Scots pine, Norway spruce, dwarf shrubs, and feather moss ground cover).
- Microclimate data collected using weather stations measuring air temperature, soil temperature at 1 cm and 5 cm, soil moisture, and surface leaf moisture; stations installed at all sites except GUO.
- Data collection period for microclimate and related measurements: June 2012 to July 2014.

## Sites and Sampling Frame
- Six sites with codes and time-since-fire (as of 2014): NJA (47 years), JAR (53), LAD (136), GUO (183), FET (232), REV (367).
- Site coordinates provided (latitude/longitude). 
- Site-level context includes soil type and vegetation to maintain comparability across sites.

## Data Collected

### Microclimate and Environmental Measurements
- Air temperature, soil temperature (1 cm and 5 cm), soil moisture, and surface leaf moisture recorded at each site (except GUO for some datasets).

### Plant and Soil Sampling
- Post-GHG sampling, gas plots destructively harvested: all above- and below-ground material within gas chamber collars collected, dried (60ºC), and weighed for total biomass.
- Soil core (5 cm diameter, 10 cm depth) collected to assess horizon depths, bulk densities, and total soil C:N.
- Plant cover estimated by species (often >100% cover due to overlapping plants) and grouped into plant functional types (PFTs: shrubs, graminoids, bryophytes) to estimate total cover by type.
- June 2012: six soil cores along transect for inorganic nitrogen (NO3-, NH4+).
- September 2013: four additional cores for soil properties (pH, total phosphorus, loss on ignition for organic matter, microbial PLFA content) in the soil organic horizon.

### Microbial and PLFA Analyses
- Microbial biomass and fungal/bacterial ratios determined via a modified Bligh and Dyer lipid extraction, followed by phospholipid fatty acid (PLFA) analysis.
- PLFA separation into neutral, free fatty acids, and phospholipids; identification of bacterial PLFAs (e.g., 15:0i, 15:0a, 16:0i, etc.) and fungal PLFAs (18:2ω6,9); results expressed as nmol PLFA g dw^-1.

### Forest Floor Greenhouse Gas Fluxes
- Five permanent PVC collars per site used to measure GHG fluxes; installed along transects on a moss mat (P. schreberi).
- Measurements: June 2012 once, Sept 2012, June 2013, July 2014 (total of four campaigns after initial setup).
- GHGs measured: CO2 exchange (ER and NEE) using a portable IR gas analyser with opaque/transparent chambers; NEE combines ER and GPP (negative NEE = net CO2 uptake).
- PAR measured concurrently to derive GPP component of NEE.
- CH4 and N2O measured with a closed static chamber approach; gas samples collected every 10 minutes for 30 minutes, analyzed by GC with detectors appropriate for CH4 and N2O.
- Fluxes converted from ppm to mg CH4-C or mg N2O-N m^-2 h^-1; quality control procedures applied to identify missing data and contamination.

## Data Processing and Analyses

### Statistical Approaches
- Analyses performed in R to assess: (a) relationships among time since fire, site properties, and GHG fluxes; (b) inter-site differences in properties and GHG fluxes; (c) predictors of forest floor GHG emissions.
- Linear regression used to examine trends in soil properties and GHG fluxes with time since fire (data from collars and transects).
- ANOVA used to detect discrete site differences (with Tukey's HSD post-hoc when significant); non-parametric alternatives (Kruskal-Wallis with Dunn’s test) applied when assumptions not met.
- Linear mixed effects (LME) models developed to identify controls on forest floor GHG fluxes:
  - Time since wildfire removed from models as it was not significantly related to soil properties or GHG emissions in this dataset; site used as a discrete factor.
  - Collinearity checks removed one of each highly correlated pair (>70%).
  - Random effects included to account for repeated sampling per plot and heterogeneity among sites.
  - Fixed effects selected via stepwise term deletions and likelihood ratio tests; interaction terms pruned if not significant.
- Two model variants due to GUO lacking a weather station:
  - All Sites model (with all data).
  - Including WS Data model (excluding GUO data to maximize use of weather-station-derived variables).
- Data inputs for models included: mean air temperature (AirTemp1), mean soil moisture, mean leaf moisture, soil horizon depth (DepthOH), C:N in horizon, bulk density (BDOH), final plant biomass, percent moss, percent cover of key species (e.g., Dicranum sp., P. commune), total shrub cover, and cover percentages for various mosses and vascular plants.
- Final model factors reported in context of their fixed effects and significance; emphasis on how vegetation and soil properties predict GHG fluxes.

## Data Quality, Provenance, and Methods Transparency

- Field and laboratory methods referenced to established protocols (e.g., Ward et al. 2013 for GHG measurements; Crossman et al. 2004 for PLFA extraction).
- Detailed descriptions of sample collection, processing (desiccation, biomass drying, soil core handling), and analytical instrumentation (GC setup, detectors) provided to enable reproducibility.
- Data transformations and QA steps (e.g., drift corrections, calibration against standards, identification of atmospheric contamination) documented for GHG data.

## Data Sharing, Standards, and Governance Considerations for Data Stewards

- Datasets span multiple campaigns (2012–2014) and multiple measurement modalities (soil properties, PLFA, biomass, plant cover, GHG fluxes, microclimate).
- Site codes, coordinates, and time-since-fire metadata essential for discoverability and reuse; table-like structures (e.g., Table 1) should be preserved with clear definitions.
- Potential interoperability challenges:
  - GUO lacks a weather station data stream, necessitating separate model configurations and potentially incomplete cross-site comparability.
  - Data derive from both destructive sampling and non-destructive monitoring across several campaigns; versioning and data lineage important.
  - Multiple data types and units (e.g., PLFA nmol g dw^-1, mg CH4-C m^-2 h^-1, mg N2O-N m^-2 h^-1) require a consistent data dictionary and unit conventions.
- Recommendations for data stewardship:
  - Provide a comprehensive metadata schema including site, sampling periods, instruments, calibration details, units, data processing steps, and QC procedures.
  - Preserve raw and processed data with clear versioning and data provenance.
  - Include data dictionaries and controlled vocabularies for site codes, plant functional types, and taxonomic names.
  - Supply analysis scripts or workflows (R code) used for model selection and final analyses to enhance reproducibility.
  - Where data gaps exist (e.g., GUO weather data), document limitations and provide guidance on comparability and potential imputation or exclusion criteria.

## Challenges and Limitations Highlighted
- Incomplete or inconsistent data across sites due to missing weather data at GUO, limiting certain cross-site model comparisons.
- Time-since-fire did not show a consistent relationship with soil properties or GHG fluxes in this dataset, guiding model restructuring (placing site as the discrete factor).
- Collinearity among predictors required careful variable selection to avoid inflated effects.

## Summary of Key Datasets (Implied)
- Site metadata: codes, coordinates, age since last wildfire.
- Microclimate data: air temperature, soil temperature at 1 cm and 5 cm, soil moisture, surface leaf moisture.
- Plant data: biomass, total cover by species and by plant functional type.
- Soil data: horizon depths, bulk density, soil C:N, pH, total phosphorus, loss on ignition, inorganic N (NO3-, NH4+), PLFA profiles (bacterial and fungal markers), soil organic horizon metrics.
- GHG flux data: NEE, ER, GPP, CH4 flux, N2O flux; PAR data for GPP estimation.
- Analytical outputs: PLFA-derived microbial biomass indicators (bacteria/fungi), derived flux measurements with quality control notes.