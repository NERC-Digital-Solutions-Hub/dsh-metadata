# Croplands_2050.csv

## Overview
- Analyzes how changes in water availability will affect cropland availability in 2050.
- Identifies country-level vulnerabilities by combining projections of water scarcity with current cropland extent.

## Experimental design / aims
- Combine projections of changes in water scarcity with current cropland extent to identify country-level cropland vulnerabilities to water scarcity in 2050.

## Data collection methods
- Global maps of change in annual runoff (%) and water scarcity (1–4 scale) derived from five general circulation models (GCMs); provided by Prof. N. Arnell (University of Reading). Methodology detailed in Arnell et al. 2011.
- Global cropland area maps downloaded from earthstat.org; based on satellite-derived data plus national/state/country statistics; grid: global 5 arc-minute. Details in Monfreda et al. 2008 and Ramankutty et al. 2008.

## Fieldwork / instrumentation
- Desk-based study; only PC computer used.

## Calibration steps / values
- No calibration required; all data were previously published.
- Runoff change represented as percent change from baseline 1960–1990 to 2050.
- Water scarcity scaled from 1 (not water scarce) to 4 (severely water scarce).
- Cropland areas provided on a hectare basis.

## Analytical methods
- Overlay cropland maps with each GCM’s projections of water scarcity and runoff using ArcGIS.
- Vulnerable cropland defined where cropland exists in areas that (i) have declining annual runoff and (ii) are in water-scarce watersheds.
- For each country, the percentage of cropland meeting both criteria is calculated as the vulnerability metric.

## Nature and units of recorded values
- Croplands_2050.csv provides the percentage of a country’s total cropland classified as vulnerable.
- Country names follow the FAOSTAT naming convention.
- Data are averaged across the five GCM models; includes standard deviation.

## Quality control
- Datasets sourced directly from data owners to prevent modification.

## Data structure details
- Country-level estimates averaged across five GCMs; standard deviation reported.

## Additional information for interpretation
- GCMs used: CSIRO Mk3, HADGEM, INMCM4, IPSL-CM5A, MRI-CGCM3.
- References for underlying datasets include Arnell et al. (2011), Gosling & Arnell (2016), Gosling et al. (2010), Monfreda et al. (2008), Ramankutty et al. (2008).