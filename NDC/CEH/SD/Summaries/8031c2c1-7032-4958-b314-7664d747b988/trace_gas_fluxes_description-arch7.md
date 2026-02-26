# Hampshire Avon: trace gas fluxes from experimentally manipulated plots in three sub-catchments

## Overview
- Near-continuous greenhouse gas flux measurements using SkyLine2D on lysimeters in unimproved pastures across three sub-catchments with chalk, clay, and greensand geologies in the Hampshire Avon catchment.
- Fluxes include CO2 (with CH4 and N2O included where applicable) measured via automated chamber methods.

## Datasets and Files (Part One)
- gasflux_chalk.csv
  - From: 04Aug2015; To: not specified
  - Description: CO2, CH4 and N2O fluxes from lysimeters
  - Location: OS Grid Reference ST 85862 38261
- gasflux_clay.csv
  - From: 04Mar2015; To: 04Aug2015
  - Description: CO2, CH4 and N2O fluxes from lysimeters
  - Location: OS Grid Reference ST 92218 27263
- gasflux_greensand.csv
  - From: not specified; To: 01Sep2015
  - Description: CO2 and CH4 fluxes from lysimeters (N2O not listed)
  - Location: OS Grid Reference SU 09720 57896
- Depositor and contact
  - Depositor: James Stockdale
  - Contact: james.stockdale@york.ac.uk

## Dataset Structure (Part Two)
- All three CSV files share the same format and variables (specific field names not listed in this summary).

## Methods and Quality Control (Part Three)
- Measurement approach
  - Near-continuous measurements using a novel SkyLine2D suspended mobile platform with a non-steady-state chamber.
  - Sequential, automated measurements of all plots at each site.
  - Lysimeters contain intact soil-vegetation monoliths from unimproved pastures across three geologies.
- Instruments and flux calculations
  - CO2: Infra-red gas analyser (Li-Cor Li-Cor 8100, model 8100); software Li-Cor v2.0.0
  - CH4: Campaign-mode measurements with Fast Greenhouse Gas Analyzer (FGGA, model 907-0010)
  - N2O: Campaign-mode measurements with Isotopic N2O Analyzer (INA, model 914-0027)
  - Flux measurement protocol: chamber closure for 180 seconds (extended to 300 seconds in campaign-mode)
  - Flux calculation and quality control
    - CO2: fluxes calculated with Li-Cor software; post-flux QC to remove poorly fitted slopes (r^2 < 0.7) or highly variable fluxes (CV > 50%) not near zero (between -0.5 and 0.5 µmol CO2 m^-2 s^-1)
    - CH4 and N2O: fluxes calculated by linear regression and quality-controlled similarly to CO2
- Data context
  - Measurements conducted on lysimeters containing soil-vegetation monoliths from three underlying geologies
  - Temporal scope spans 2015 data across the three site datasets

## GIS Relevance and Usage
- Spatial data points are defined by OS Grid References, enabling precise mapping in OSGB36 and easy overlay with geology, catchment boundaries, and other GIS layers.
- Suitable for creating point-based flux maps, time-series visualizations, or aggregations by geology or site.
- When integrating, ensure consistent data quality filtering (r^2, CV, flux thresholds) and harmonize temporal coverage across sites.

## Access and Contact
- Depositor: James Stockdale
- Contact: james.stockdale@york.ac.uk
- Datasets are named by site (chalk, clay, greensand) and include explicit flux types per file.