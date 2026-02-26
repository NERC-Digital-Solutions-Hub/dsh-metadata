# Nitrous oxide emission factors of mineral fertilisers in the UK and Ireland: experimental data for the period (1998 - 2019)

## Overview
- 集: 38 experimental sites across the UK and Ireland, yielding 641 N2O emission factor (EF) estimates from field measurements.
- Purpose: to enable a Bayesian analysis of EF differences by fertiliser type and field management, and to establish prior distributions for future EF work.
- Output intended for reuse: dataset of EF events for UK and Ireland fertiliser applications, supporting cross-study comparison and Bayesian modeling.

## Data and design
- Fertiliser types analyzed: ammonium nitrate (AN), calcium ammonium nitrate (CAN), and urea.
- Inhibitors considered: Dicyandiamide (DCD), MIP (a polymer product), NBTP (urease inhibitor); EF records include treatments with inhibitors (e.g., DCD or NBTP).
- Measurement methods: flux chamber most commonly used; one study used eddy covariance.
- Temporal scope: data collected 1998–2019; EF calculations include post-application fluxes, with 25-day post-application EFs calculated from raw data (AEDA) using a log-normal Bayesian approach.
- Data sources: EF data extracted from published studies and from the Agricultural and Environmental Data Archive (AEDA).

## Data collection and sources
- Data collection approaches:
  - i) Extracted from published studies explicitly measuring N2O EF after fertiliser application.
  - ii) Raw data from AEDA used to compute EFs for 25 days after application.
- Literature search:
  - Keywords included N2O, emission factor, mineral fertiliser, nitrification inhibitors, nitrogen use efficiency, agriculture, greenhouse gas, etc.
- AEDA data sources:
  - Multiple InveN2Ory datasets (fertiliser experiments, manure experiments) across sites in Bedfordshire, Devon, Ceredigion, County Down, Warwickshire, Dumfries, East Lothian, etc.
  - Datasets published by Freshwater Biological Association; DOIs provided for each dataset.
- Representative studies cited (examples): Abdalla 2009; Baggs 2003; Bell 2015; Cardenas 2019; Cowan 2019a/2019b; Dobbie & Smith 2003; Harty 2016; Hinton 2015; Jones 2005; Misselbrook 2014; Roche 2016; Skiba 2013; Smith 2012.

## Data structure and units
- File name: Farm_Flux_and_Soil.
- Core fields (12 total):
  - Year = Location: experiment year and country/region (England, Ireland, Northern Ireland, Scotland, Wales).
  - Year = Country: broader location definition.
  - Fertiliser: AN, CAN, or Urea.
  - Inhib: inhibitor type (DCD, MIP, NBTP, or NA for none).
  - Amount applied: kilograms of nitrogen (Kg N).
  - Applications: number of fertiliser applications during the experiment.
  - Mean_N_app: average mass of N applied per event.
  - Field_manage: Arable or Grass.
  - Crop_Type: crop grown during the experiment.
  - Meas. Method: measurement method (Manual chamber or Edy covariance).
  - EF: emission factor as a percent of total N applied.
  - Reference: source of the data.
- EF unit: percent of total nitrogen applied.
- Additional data notes: EF events include both directly published EF measurements and AEDA-recalculated EF data.

## Data sources (references and dataset provenance)
- Published studies (examples): Abdalla et al. 2009; Baggs et al. 2003; Bell et al. 2015; Cowan et al. 2019/2020; Dobbie & Smith 2003; Harty et al. 2016; Hinton et al. 2015; Jones et al. 2005; Misselbrook et al. 2014; Roche et al. 2016; Skiba et al. 2013; Smith et al. 2012; plus others listed in Table and references.
- AEDA data sources: multiple InveN2Ory datasets (fertiliser and manure experiments) across UK sites; each dataset with versioning and publisher attribution (Freshwater Biological Association) and DOIs.

## Data products and reuse opportunities
- Primary data product: a harmonised dataset of N2O EF events (641 events) suitable for cross-study analyses and Bayesian prior construction.
- Potential data products for end users:
  - Self-serve analytics on EF by fertiliser type, inhibitor use, field management, region, and measurement method.
  - Bayesian EF modeling pipelines to derive prior distributions for future EF studies.
  - Dashboards summarising EF distributions, treatment effects (e.g., CAN vs. AN, urea vs. AN, inhibitor effects), and temporal patterns post-application.
- Data integration opportunities:
  - Combine across studies with varying formats and measurement methodologies; apply quality assurance and standardisation to enable robust meta-analysis.
  - Use AEDA-derived data to extend the temporal window and improve estimates of cumulative fluxes.

## Quality, challenges, and considerations
- Challenges highlighted:
  - Patchy data across wide geographic and temporal ranges.
  - Heterogeneity in data formats and measurement methods across studies.
  - Difficulty in communicating and promoting outputs for wider reuse.
- Data quality considerations:
  - Verification of data sources (published articles and AEDA datasets).
  - Standardisation of EF calculations (e.g., 25-day post-application EF via log-normal Bayesian method).
  - Clear documentation of inhibitors and treatment conditions to support reproducibility.
- Suggested improvements for data management:
  - Better data creation and sharing to facilitate broader reuse.
  - Adoption of consistent data schemas and metadata to reduce format fragmentation.