# Nitrous oxide emission factors of mineral fertilisers in the UK and Ireland: experimental data for the period (1998 - 2019)

## Overview
- Compiles 641 emission factor (EF) estimates from 38 experimental sites across the UK and Ireland, derived from field measurements.
- Data cover fertiliser types: ammonium nitrate (AN), calcium ammonium nitrate (CAN), and urea; with and without inhibitors (DCD, NBTP, MIP).
- Designed to support a Bayesian analysis of EF differences by fertiliser type and field management; usable to establish prior distributions for future EF work.
- Most data collected via flux chamber methods; one study used eddy covariance.

## Data sources and scope
- Data collection from:
  - Published studies (explicit N2O EF measurements after mineral fertiliser application).
  - Raw data from the Agricultural and Environmental Data Archive (AEDA).
- Time frame: EF data spanning 1998–2019.
- Geographic scope: United Kingdom and Ireland (England, Scotland, Wales, Northern Ireland, and Republic of Ireland).
- Purpose: To provide a comprehensive dataset for statistical (Bayesian) analysis of N2O emissions related to fertiliser type and field management.

## Data structure and content
- Main dataset file: Farm_Flux_and_Soil
- Key fields (examples):
  - Year experiment was carried out: Location (UK or Ireland; subnational region)
  - Location: Country/region (England, Ireland, Northern Ireland, Scotland, Wales)
  - Fertiliser: AN, CAN, or Urea
  - Inhibitors: DCD, MIP, NBTP, or NA (none); combinations where applicable
  - Amount applied: kilograms of N
  - Applications: number of fertiliser applications
  - Mean_N_app: average mass of N per fertiliser event
  - Field_manage: Arable or Grass
  - Crop_Type: Type of crop grown
  - Meas. Method: Flux measurement method (Manual chamber or eddy covariance)
  - EF: Emission factor (% of total N applied)
  - Reference: Source of data
- EF event distribution:
  - AN: 293 events
  - CAN: 63 events
  - Urea: 118 events
  - AN with DCD (and related) and urea with DCD/NBTP: 38 and 129 events respectively
- Data are designed to support cross-study comparability through consistent variable definitions, with multiple studies contributing to a single harmonised EF dataset.

## Data processing and analysis
- For raw AEDA data, EF calculations were performed for 25 days after fertiliser application using a log-normal Bayesian approach (accounts for log-normal spatial and temporal distribution of N2O fluxes).
- The dataset supports Bayesian analyses and the estimation of cumulative fluxes, providing a basis for priors in future EF work.

## Data accessibility and metadata
- AEDA data sources include multiple Fertiliser experimental sites (Bedfordshire, Devon, Ceredigion, County Down, Warwickshire, Dumfries, East Lothian, etc.) with versioned datasets.
- References list key studies and datasets used to assemble the EF database (e.g., Abdalla 2009; Bell 2015; Cowan et al. 2019a/b; Smith 2012; Misselbrook 2014; and others).
- The dataset emphasizes transparent provenance, linking EF events to primary studies and to the InveN2Ory/AEDA platform sources for raw data.

## GIS relevance and potential uses
- Spatially explicit: EF events linked to field locations across the UK and Ireland enable map-based visualization of EF by fertiliser type, inhibitor use, and field management.
- Temporal and management insights: Compare EF across years, regions, and management practices (arable vs. grass, crop types).
- GIS-friendly outputs: Data structure supports integration into GIS workflows for choropleth or symbol maps showing EF magnitudes by site, fertiliser type, or inhibitor treatment.
- Baseline for priors: Useful as a historical prior dataset for Bayesian EF modelling in spatial analyses of N2O emissions.

## Limitations and considerations for GIS work
- Heterogeneity: Data come from many studies with varying measurement methods and study designs; harmonisation required for robust GIS analyses.
- Resolution: Site-level data may lack precise coordinates in summary metadata; some site identifiers are location names rather than exact coordinates.
- Inhibitor treatments and fertiliser formulations vary in scope and frequency; careful stratification is needed when mapping by treatment.
- Temporal coverage spans 1998–2019; cross-temporal comparisons should account for methodological changes and site-specific practices.

## Reproducibility and references
- Core dataset structure and EF calculations are anchored in published literature and the InveN2Ory/AEDA data platform.
- Key methodological references include Levy et al. (2017) and Cowan et al. (2019/2020) for log-normal Bayesian EF estimation and Bayesian analysis of EF factors.
- Representative sources listed for data provenance include Abdalla et al. (2009), Bell et al. (2015, 2017), Cardenas et al. (2017–2019), Cowan et al. (2019a/b, 2020), Dobbie & Smith (2003), Misselbrook et al. (2014), Smith et al. (2012), Skiba et al. (2013), and others.