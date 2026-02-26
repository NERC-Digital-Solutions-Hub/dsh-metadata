# Overview of data

- This document describes a dataset that compiles results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, titled "The role of lateral exchange in the seaward flux of C, N and P."
- The dataset focuses on oxygen (O2) flux measurements in rivers of the Hampshire Avon catchment, at both the benthic (streambed) and water column levels.

## Dataset contents and accompanying files

- One dataset accompanies this overview: O2fluxes_Avon.CSV.
- Measurements include benthic O2 fluxes (via aquatic eddy covariance, AEC) and water-column O2 fluxes (incubations with 100 mL bottles and optical O2 sensors).
- Four field campaigns span spring 2013, summer 2013, autumn 2013, and winter 2014.
- Sites cover six tributaries: CE1 (River Ebble), GA2 (River Avon), GN1 (River Nadder), CW2 (River Wylye), AS1 (tributary of the Sem), AS2 (River Sem). CE1 was not sampled in winter; GA2 autumn/winter data were omitted due to quality issues.
- The campaigns collected data across various depths and conditions, with measurements including daytime and nighttime benthic fluxes, water-column fluxes, and PAR (photosynthetically active radiation) metrics.

## Methods and data processing

- Benthic fluxes: measured using aquatic eddy covariance (AEC); processing follows Attard et al. (2014) and Rovelli et al. (2015).
- Water-column fluxes: obtained from 24 h incubations with optical O2 sensors; standard reporting includes daytime and nighttime rates.
- PAR data and daylight duration are included to contextualize flux measurements.
- The document references multiple foundational studies for methodology (e.g., Berg et al. 2003; Attard et al. 2014; Rovelli et al. 2015, 2016; Rovelli et al., submitted).

## Data structure and variables

- Column headers in the dataset:
  - Campaign
  - Site
  - Depth
  - Day flux (b) [mmol/m2/h] +/- SE
  - Night flux (b) [mmol/m2/h] +/- SE
  - Total PAR (b) [mol/m2/d]
  - Daylight (b) [h]
  - Day flux (w) [µmol/L/h]
  - Night flux (w) [µmol/L/h]
  - Total PAR (w) [mol/m2/d]
  - Daylight (w) [h]
- Notes:
  - Values marked as nd indicate missing data due to technical issues or sampling contamination.
  - Some data (e.g., GA2 autumn/winter) were omitted due to not meeting quality requirements.
  - Day/Night flux values have data counts indicated in parentheses; some rate values may be below detection (<0.1 µmol/L/h) for water-column measurements.

## Temporal and spatial coverage

- Campaign timings:
  - Spring 2013: 23/04 – 09/05/2013
  - Summer 2013: 31/07 – 16/08/2013
  - Autumn 2013: 29/10 – 11/11/2013
  - Winter 2014: 28/01 – 09/02/2014
- Spatial scope: six tributaries within the Hampshire River Avon catchment, with site-specific coordinates provided for each site.

## Data quality, limitations, and governance

- Some datasets were omitted due to quality concerns (e.g., GA2 autumn/winter; CE1 winter sampling canceled due to flooding).
- Missing data are explicitly marked as nd; issues may arise from technical problems or contamination.
- Metadata includes site depth (from flow transects) and PAR-based daylight definitions to support reproducibility and re-use.
- Provenance and licensing are tied to the NERC Macronutrients project and associated publications; related datasets and methods are described in Rovelli et al. (submitted) and linked references.

## Provenance and references

- Primary project: NERC Macronutrients consortium, led by Prof. Mark Trimmer (Queen Mary University of London).
- Key methodological references:
  - Berg et al. 2003
  - Attard et al. 2014
  - Rovelli et al. 2015
  - Rovelli et al. 2016 (data on flow velocity transects)
- Related works:
  - Rovelli et al., 2016; Reach-scale river metabolism across contrasting sub-catchment geologies (submitted)
- Data access and citation:
  - Data are archived with NERC Environmental Information Data Centre.
  - Dataset DOI reference: https://doi.org/10.5285/16df35a9-90ab-4273-8b6c-5ef3648ec76d (as provided in accompanying materials). Additional datasets and descriptions appear in Rovelli et al. (submitted).