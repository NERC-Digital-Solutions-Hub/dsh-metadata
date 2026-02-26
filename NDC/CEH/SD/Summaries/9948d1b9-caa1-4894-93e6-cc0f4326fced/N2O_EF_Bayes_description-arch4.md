# Nitrous oxide emission factors of mineral fertilisers in the UK and Ireland: experimental data for the period (1998 - 2019)

## Overview
- Compilation of 641 nitrous oxide (N2O) emission factor (EF) estimates from 38 experimental sites in the UK and Ireland (1998–2019).
- EF estimates cover ammonium nitrate (AN), calcium ammonium nitrate (CAN), and urea, including treatments with nitrification inhibitors (DCD) and/or urease inhibitors (NBTP, MIP).
- Data collected mainly via flux chamber methods; one study used eddy covariance.
- Intended to support a Bayesian analysis of EF differences by fertiliser type and field management, and to inform prior distributions for future EF work.

## Data scope and purpose
- Purpose: to quantify N2O emission factors associated with mineral fertilisers and to enable Bayesian estimation of EF distributions.
- Coverage: UK and Ireland, across multiple sites, fertiliser forms, inhibitors, and management practices.
- Outputs: EF values expressed as a percentage of total nitrogen applied.

## Data collection and methods
- Data sources:
  - Published studies explicitly measuring N2O after mineral fertiliser application.
  - Raw data from the Agricultural and Environmental Data Archive (AEDA), recalculated for 25 days post-application using a log-normal Bayesian approach.
- Particle of methods:
  - Flux chamber measurements (majority) with one eddy covariance study.
  - Log-normal distribution used to account for temporal and spatial variability in N2O fluxes after fertiliser events.
- Literature search: papers published after January 1998 and before April 2019, with keywords related to N2O, fertilisers, inhibitors, and related topics.
- AEDA datasets linked to multiple fertiliser experiments across sites and years.

## Data structure and metadata
- File name referenced: Farm_Flux_and_Soil.
- Key fields (12 core variables):
  - Year = Location (country/region: UK or Ireland; subregions England, Ireland, Northern Ireland, Scotland, Wales)
  - Year = Fertiliser type (AN, CAN, Urea)
  - Year = Inhibitor type (DCD, MIP, NBTP, or NA for none)
  - Year = Amount applied (kg N)
  - Year = Applications (number of fertiliser applications)
  - Mean_N_app (average mass of N per fertiliser event)
  - Field_manage (Arable or Grass)
  - Crop_Type
  - Meas. Method (Manual chamber or eddy covariance)
  - EF (Emission factor as % of total N applied)
  - Reference (source of data)
- Data structure supports linking EF events to specific sites, fertilisers, inhibitors, and measurement approaches.

## Data sources and provenance
- Published studies contributing EF events (examples include Abdalla 2009; Baggs 2003; Bell 2015; Cardenas 2019; Cowan et al. 2019a/2019b; Dobbie & Smith 2003; Harty 2016; Hinton 2015; Jones 2005; Misselbrook 2014; Roche 2016; Skiba 2013; Smith et al. 2012; and others).
- AEDA (Agricultural Greenhouse Gas Inventory Research Platform InveN2Ory) datasets as raw data sources, with multiple fertiliser and site deployments (e.g., Bedfordshire, Devon, Ceredigion, County Down, Warwickshire, Dumfries, East Lothian).
- References include a broad set of journals and reports focused on N2O emissions from fertilised soils, nitrification inhibitors, and fertiliser formulations.

## Data quality, limitations, and considerations
- Heterogeneity in data sources (different measurement methods, sites, soils, management practices) introduces variability in EF estimates.
- Presence of inhibitors (DCD, NBTP, MIP) and varying fertiliser formulations adds complexity to cross-study comparisons.
- Data gaps and granularity issues may exist due to scattered data sources and inconsistent metadata across studies.
- The log-normal, time-upscaled approach addresses temporal variability but requires careful interpretation when aggregating across studies.

## Reuse, governance, and implications for data strategy
- The dataset demonstrates end-to-end data handling: collection from multiple sources, harmonisation into a common structure, and preparation for Bayesian analysis.
- Provenance and metadata are explicit, enabling reproducibility and traceability of EF estimates.
- For data leaders, this example highlights:
  - The value of pooling disparate data sources to create robust prior distributions for modelling.
  - The importance of standardized metadata (e.g., site, fertiliser type, inhibitors, measurement method) to enable discoverability and reuse.
  - The need to maintain clear data lineage (publications, AEDA datasets) and to document data transformation steps (e.g., recalculation to 25 days post-application, log-normal upscaling).
  - The benefit of aligning data assets with broader community resources and methods (Bayesian EF estimation) to support cross-organisational learning and policy-relevant analysis.