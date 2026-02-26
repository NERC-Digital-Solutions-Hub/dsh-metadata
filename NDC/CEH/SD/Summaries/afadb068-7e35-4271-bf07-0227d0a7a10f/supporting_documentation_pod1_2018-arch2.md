# Ozone flux dataset POD 1 IAM for grassland (semi-natural vegetation) in 2018 – UK and USA

## Overview
- Documents a dataset of ozone flux POD1 IAM values for grassland in 2018 for the UK and USA.
- Derived from the EMEP-WRF global model (v4.45) driven by 2018 meteorology; emissions based on IIASA ECLIPSE v6a GAINS for 2015.
- Ozone stomatal uptake calculated with the DO3SE model embedded in EMEP; outputs POD values (mmol m-2) accumulated over a growing-season window.
- Data produced as a 1° x 1° gridded shapefile with 5 attributes, intended for environmental monitoring and impact assessment.

## Methods and data sources
- Models and data:
  - EMEP-WRF global model (v4.45) using 1° x 1° grid, 21 vertical layers, driven by hourly 3D meteorology from WRF v4.2.2.
  - Nudging every six hours with GFS-FNL data; global domain; 2018 period.
  - Emissions from IIASA ECLIPSE v6a GAINS (2015).
- Ozone uptake calculation:
  - DO3SE model for stomatal ozone flux; inputs include hourly ozone, temperature, vapor pressure deficit, irradiance, and soil moisture.
  - Vegetation-specific parameterisations (e.g., gmax) required; POD values output as PODyIAM or POD1IAM depending on method.
  - IAM flux models for large-scale modelling; POD1IAM used for perennial grasslands in this dataset.
- Time period:
  - Primary dataset sums daily POD1IAM over a 90-day grassland growing season (mid-April to mid-July) for 2018, UK and USA.
  - Guidance allows selecting a 3-month accumulation within April 1 to September 30 to maximize flux or reflect local seasonality.
- Parameterisation:
  - Parameter values for semi-natural vegetation (grasslands) referenced from CLRTAP Mapping Manual (2017); includes season length, leaf/phenology factors, VPD thresholds, canopy height, and other vegetation-specific inputs.
- Output:
  - POD1IAM values for sunlit leaves at the top of the canopy; units are mmol m-2; spatial reference in decimal degrees (WGS 84).

## Data structure and units
- Shapefile with gridded data at 1° x 1° resolution.
- Attributes (5 fields):
  - FID: Unique grid cell identifier.
  - Lon: Longitude of grid center (decimal degrees).
  - Lat: Latitude of grid center (decimal degrees).
  - NAME: Country (USA or UK).
  - POD1: Accumulated POD1IAM for grassland growing season in 2018 (mmol m-2) per grid cell.

## Quality control and validation
- Model outputs undergo QA/QC prior to use; validation described in Mills et al. (2018) with additional supplementary figures.
- Model performance shown via comparison of modelled vs. observed daily max ozone at Global Atmosphere Watch (GAW) sites, demonstrating capture of spatial/temporal variation.
- Stomatal uptake validation: strong correlation (r^2 = 0.63) between a proxy for growing-season stomatal conductance (AET/PET) and model-estimated POD3IAM divided by the 7-hour mean ozone value, indicating the DO3SE uptake estimates are reasonable.

## Background and usage
- Ozone flux data enable impact assessments on crops and vegetation (yield, biomass, flower number) using response functions from the CLRTAP Modelling and Mapping Manual (2017).
- For grasslands, dose-response relationships are derived from pooled experimental data; POD1IAM values feed into these relationships to estimate potential losses.
- Ozone critical levels have been established for grasslands using POD-based flux metrics, enabling risk assessment for semi-natural vegetation dominated by temperate perennial grasses.
- References and resources:
  - CLRTAP 2017; Emberson et al. 2000; Hayes et al. 2021; Mills et al. 2018; Simpson et al. 2012; Vieno et al. 2016.
  - CLRTAP Mapping Manual and CLRTAP vegetation monitoring resources.

## Practical implications for environment monitoring
- Provides a standardized, QA-validated dataset for evaluating ozone flux to grasslands at continental scales (UK and USA) during 2018.
- Supports monitoring of air-quality policy impacts on semi-natural vegetation and informs risk assessments and potential yield/biomass changes.
- The 1° grid facilitates integration with other environmental monitoring datasets and spatial analyses.

## Useful context and references
- Data sources and model descriptions:
  - EMEP-WRF model (Vieno et al., 2016; Mills et al., 2018; Simpson et al., 2012).
  - DO3SE stomatal ozone flux model (Emberson et al., 2000).
  - CLRTAP Modelling and Mapping Manual (CLRTAP, 2017).
- Validation and supporting analyses:
  - Mills et al. (2018): model validation against GAW observations.
  - Hayes et al. (2021): ozone critical levels for perennial grasslands.
  - Complements to CLRTAP utility in agricultural and ecological impact assessments.