# Saltmarsh vegetation composition data produced from 460 quadrats across 33 UK saltmarshes, 2018 - 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE); Funding: NERC (NE/R010846/1).
- Team: researchers from University of Glasgow, St Andrews, York, Bangor, UK CEH, and Scottish Association of Marine Science.
- Data Resource ID: UK_saltmarsh_veg_cover.csv; Description: Saltmarsh vegetation composition data from 460 quadrats across 33 UK saltmarshes (2018–2021).
- Geographic and temporal scope: across the UK with sites around Scotland’s coastline; observations collected from 2018 to 2021.
- Data types: vegetation species coverage, plant height, species richness, and plant diversity metrics; site-level and quadrat-level measurements.
- File format: CSV with detailed field descriptions and metadata.

## Dataset contents and variables
- Quadrat design and observations:
  - 460 quadrats, each 1x1 m, sampled along transects perpendicular to the coastline to capture all marsh zones.
  - For each quadrat: annual survey data including date, location, and environmental descriptors.
- Spatial identifiers and location data:
  - Marsh_ID, Site_ID, Marsh_Type (Natural, Historic Breach, Managed Realignment), Nation (England, Scotland, Wales).
  - Latitude (decimal degrees), Longitude (decimal degrees), X_Easting, Y_Northing (UK grid), Elevation above OD (m).
  - Survey_Date (date of survey; format noted as Number in the dataset).
- Vegetation measurements (per quadrat):
  - Mean_Plant_Height_cm and Plant_Height_SD (height measured at 10 random points per quadrat).
  - Plant_species_richness (number of species per quadrat).
  - Plant_S-W_diversity (Shannon-Wiener Index; diversity accounting for richness and evenness).
  - Plant_Species (percent cover of 58 different species; grouped data per species).
  - Plant_total_cover (total reported plant coverage %).
- Location-specific context:
  - Marsh_Type and Nation descriptions to compare vegetation across natural vs. managed/realigned sites and across UK nations.
- Data detail descriptors (examples of fields):
  - Marsh_ID, Site_ID, Marsh_Type, Nation, Latitude_Dec_Degree, Longitude_Dec_Degree, X_Easting, Y_Northing, Elevation_above_OD_m, Survey_Date, Mean_Plant_Height_cm, Plant_Height_SD, Plant_species_richness, Plant_S-W_diversity, Plant_Species (58 species coverage), Plant_total_cover.

## Methods and data quality
- Procedures:
  - Vegetation coverage estimated by eye within each quadrat.
  - Plant height measured at 10 random points per quadrat; mean and standard deviation calculated.
  - Species richness per quadrat; diversity calculated using Shannon-Wiener Index (H = -Σ pi log pi).
  - Calibration used expert judgement; two team members conducted surveys independently, with combined results reported.
- Quality and checks:
  - Data checking procedures are not explicitly described (NA for data checking in the dataset description).
- Format and accessibility:
  - Primary data file: UK_saltmarsh_veg_cover.csv; accompanies detailed metadata describing each field’s meaning and unit.
  - Field-level descriptions present for location, vegetation metrics, and survey metadata.

## Context and potential use cases
- Purpose: provide a robust, large-scale snapshot of saltmarsh vegetation composition and structure across multiple UK sites to support analyses of habitat condition and carbon stock potential.
- Link to broader work: related to regional or national efforts on coastal carbon storage; aligns with approaches that use simple vegetation and soil observations to predict carbon stocks (as referenced by Ford et al. 2019).
- Analytical opportunities for analysts:
  - Explore correlations between vegetation metrics ( richness, diversity, average height, species cover) and marsh type, location, or environmental context.
  - Develop predictive models of carbon stock or habitat quality using plant community structure as predictors.
  - Compare vegetation structure across Natural vs. breached/realigned marshes and across nations (England, Scotland, Wales).
  - Integrate with additional soil or sediment data to enhance carbon stock predictions or habitat assessments.

## Limitations and considerations
- Data checks are not fully documented; interpret quality with awareness of potential measurement subjectivity in eye-based cover estimates.
- Spatial scope emphasizes Scottish coastline representations; broader UK generalization should consider site-specific variations.
- Temporal coverage spans 2018–2021; may not capture longer-term trends or inter-annual variability beyond this window.

## References
- Ford, H., Garbutt, A., Duggan-Edwards, M., Harvey, R., Ladd, C., and Skov, M.W. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type. Biogeosciences, 16(2), 425-436.
- Pielou, E.C. (1966). Shannon's formula as a measure of specific diversity: its use and misuse. The American Naturalist, 100(914), 463-465.