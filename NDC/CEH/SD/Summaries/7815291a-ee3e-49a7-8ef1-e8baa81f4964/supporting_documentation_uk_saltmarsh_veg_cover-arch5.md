# Saltmarsh vegetation composition data produced from 460 quadrats across 33 UK saltmarshes, 2018 - 2021

## Overview
- Dataset from the Carbon Storage in Intertidal Environments (C-SIDE) project, funded by NERC.
- Produced by a multi-institution team (University of Glasgow, St Andrews, York, Bangor, UK CEH, etc.).
- Captures vegetation composition across UK saltmarshes collected between 2018 and 2021 (460 quadrats across 33 sites).

## Dataset scope and contents
- Describes saltmarsh vegetation composition, including:
  - Plant species coverage (percent cover) and plant height.
  - Measures of plant species richness and Shannon-Wiener diversity.
- Location data provided for each observation (latitude/longitude in decimal degrees, with X (Easting) and Y (Northing); elevation above ordnance datum).
- Site descriptions indicate sites are within Scotland-typical environmental regions to support comparability.

## Methods and measurements
- Sampling design: 1 x 1 meter quadrats collected along transects perpendicular to the coastline to capture all marsh zones.
- Observations:
  - Plant coverage estimated by eye within each quadrat.
  - Plant height measured at 10 random points per quadrat; mean and standard deviation reported.
  - Plant species richness per quadrat recorded; diversity calculated using the Shannon-Wiener index.
- Calibration and quality control:
  - Expert judgement used to estimate species coverage.
  - Two team members independently conducted surveys; results combined for reporting.
- Data treatment: Statistical treatment indicated as NA; data checking procedures indicated as NA.

## Data structure and metadata
- Data format: CSV (UK_saltmarsh_veg_cover.csv).
- Key variables include:
  - Marsh_ID, Site_ID, Marsh_Type (Natural, Historic Breach, Managed Realignment), Nation (England, Scotland, Wales).
  - Latitude_Dec_Degree, Longitude_Dec_Degree, X_Easting, Y_Northing, Elevation_above_OD_m.
  - Survey_Date; Mean_Plant_Height_cm; Plant_Height_SD; Plant_species_richness; Plant_S-W_diversity.
  - Plant_Species (percentage cover for 58 species); Plant_total_cover.
- Site descriptions indicate all sites are in Scotland to allow comparable data across similar environmental contexts.
- Data resource details align with UK saltmarsh vegetation coverage, with explicit referencing.

## Provenance, governance, and disclosure
- Data produced under the C-SIDE project with clear authoring team and affiliations.
- Dataset includes explicit references for methodologies and diversity calculation:
  - Ford et al. 2019 for large-scale predictions of salt-marsh carbon stock.
  - Pielou 1966 for Shannon-Wiener diversity calculation.
- Data stewardship emphasis:
  - Standardized measurement approaches (1 m quadrats, 1x1 m sampling, transect approach).
  - Geospatial referencing with WGS84 coordinates and Easting/Northing for interoperability.
  - Metadata coverage includes measurement procedures, calibration, and data fields to support discovery and reuse.

## Data quality, limitations, and reuse considerations
- Calibration relies on expert judgement; two observers improve reliability.
- Some quality-control fields are marked NA, indicating limited documented QC steps beyond independent double-surveys.
- Spatial scope is focused on UK saltmarshes (primarily Scotland) for comparability; applicability to other regions should consider environmental differences.
- Data suitable for integration with large-scale saltmarsh carbon stock models and ecological diversity analyses.

## Access, reuse, and references
- Data resource is described as UK_saltmarsh_veg_cover.csv with detailed field descriptions.
- References for methodological context:
  - Ford, H., Garbutt, A., et al. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type. Biogeosciences.
  - Pielou, E.C. (1966). Shannon's formula as a measure of specific diversity.
- The dataset is structured to support discovery, sharing, and potential updates within data portals and catalogues.