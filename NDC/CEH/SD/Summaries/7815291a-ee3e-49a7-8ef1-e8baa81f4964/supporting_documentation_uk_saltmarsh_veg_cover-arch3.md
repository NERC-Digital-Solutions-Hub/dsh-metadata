# Saltmarsh vegetation composition data produced from 460 quadrats across 33 UK saltmarshes, 2018 - 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: Natural Environment Research Council (NERC) NE/R010846/1
- Lead staff: Craig Smeaton
- Research team: Cai J.T. Ladd; Lucy C. Miller; Lucy McMahon; Glenn M. Havelock; Angus Garbutt; Martin W. Skov; William E.N. Austin; (affiliations with University of Glasgow, St Andrews, York, Bangor, UK CEH, SAMS)
- Purpose: Provide a dataset of saltmarsh vegetation composition to support monitoring, evaluation of environmental health, and informing policy decisions on carbon storage and habitat condition.

## What the data contains
- Coverage: Saltmarsh vegetation data from 460 quadrats across 33 UK saltmarshes
- Timeframe: Surveys conducted 2018–2021
- File format: CSV (UK_saltmarsh_veg_cover.csv)
- Key variables and metrics:
  - Spatial identifiers: Marsh_ID, Site_ID
  - Location: Latitude/Longitude (WGS84), X_Easting, Y_Northing, Elevation above datum (m)
  - Marsh characteristics: Marsh_Type (Natural, Historic Breach, Managed Realignment), Nation (England, Scotland, Wales)
  - Survey details: Survey_Date
  - Plant measurements: Mean_Plant_Height_cm, Plant_Height_SD
  - Biodiversity metrics: Plant_species_richness, Plant_S-W_diversity (Shannon-Wiener Index)
  - Vegetation composition: Plant_Species (percent cover per species; 58 species reported), Plant_total_cover
- Sampling design and observations:
  - Quadrat layout: 1 x 1 m quadrats surveyed along transects perpendicular to the coastline to capture all marsh zones
  - Measurements: percentage cover estimated by eye per species; height measured at 10 random points per quadrat
  - Derived metrics: mean height and its standard deviation per quadrat; species richness per quadrat; Shannon-Wiener index for diversity
- Data quality and calibration:
  - Calibration: expert judgement used for species coverage; two team members conducted surveys independently; combined results reported
  - Data quality checks: not specifically documented (quality control field NA)

## Data collection and processing details
- Procedures:
  - Field observations conducted in 1 m2 quadrats; covers all marsh zones via transects
  - Species coverage estimated by eye; mean plant height derived from 10 measurements per quadrat
  - Diversity calculated using Shannon-Wiener formula
- Metadata and lineage:
  - Comprehensive spatial and environmental metadata included (coordinates, elevation, marsh type, nation)
  - References for methods and diversity calculation: Ford et al. 2019; Pielou 1966

## Relevance for monitoring frameworks
- Provides tangible, quantifiable indicators of environmental health:
  - Vegetation composition and structure (height, total cover)
  - Biodiversity dimensions (species richness, Shannon-Wiener diversity)
- Spatially explicit baseline across multiple UK saltmarshes enables:
  - Monitoring changes over time and space
  - Linking vegetation metrics to carbon stock estimates and habitat quality
- Data governance and data sharing:
  - Metadata-enriched dataset with clear provenance
  - Highlights governance considerations: metadata completeness, standardization, and data sharing barriers that can affect timely use
- Practical alignment to policy needs:
  - Supports indicators for carbon storage potential and habitat condition
  - Facilitates evidence-based decision-making for marsh management (e.g., natural marshes vs. managed realignment sites)

## Data provenance and references
- Ford, H.; Garbutt, A.; Duggan-Edwards, M.; Harvey, R.; Ladd, C.; Skov, M.W. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type. Biogeosciences, 16(2), 425-436.
- Pielou, E.C. (1966). Shannon's formula as a measure of specific diversity: its use and misuse. American Naturalist, 100(914), 463-465.