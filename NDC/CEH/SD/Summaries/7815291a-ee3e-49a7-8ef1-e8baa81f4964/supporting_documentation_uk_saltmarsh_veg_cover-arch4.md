# Saltmarsh vegetation composition data produced from 460 quadrats across 33 UK saltmarshes, 2018 - 2021.

- Overview
  - A data resource describing UK saltmarsh vegetation composition from 460 quadrats across 33 saltmarshes collected between 2018 and 2021.
  - Key metrics include plant species coverage, mean plant height, species richness, and Shannon-Wiener diversity.

- Content and structure
  - Primary dataset: UK_saltmarsh_veg_cover.csv.
  - Variables/parameters included:
    - Marsh_ID, Site_ID, Marsh Type (Natural, Historic Breach, Managed Realignment)
    - Nation (England, Scotland, Wales)
    - Latitude and Longitude (decimal degrees, WGS84)
    - X_Easting, Y_Northing, Elevation_above_OD_m
    - Survey_Date
    - Mean_Plant_Height_cm, Plant_Height_SD
    - Plant_species_richness, Plant_S-W_diversity (Shannon-Wiener Index)
    - 'Plant Species' (percentage cover for 58 species)
    - Plant_total_cover (overall plant cover %)
  - Site-level and habitat descriptors accompany geographic data (e.g., marsh type, nation, and location coordinates).
  - Data collection methodology:
    - 1 x 1 m quadrats surveyed along transects perpendicular to the coastline to capture all marsh zones.
    - Within-quadrat estimation of species cover by eye; plant height measured at 10 random points per quadrat.
    - Species richness per quadrat and Shannon-Wiener diversity calculated as described in referenced literature.
  - Calibration and quality:
    - Calibration by expert judgement for plant coverage assessments.
    - Two team members conducted surveys independently to validate observations; combined results reported.
    - Some data quality/control details marked NA (e.g., statistical treatment and explicit QA procedures).

- Geographic and temporal coverage
  - Location: United Kingdom (England, Scotland, Wales) across 33 saltmarsh sites with varied marsh types.
  - Spatial data: Includes latitude/longitude (WGS84) and projected coordinates (X Easting, Y Northing) plus elevation.
  - Survey period: 2018–2021.

- Data formats and accessibility
  - File format: .csv.
  - Descriptive metadata available for each field (e.g., variable descriptions and formats).
  - Site metadata covers marsh type, nation, and coordinate details to support spatial analyses and reproducibility.

- Data use and context
  - Related research and references:
    - Ford et al. 2019: Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type.
    - Pielou 1966: Shannon-Wiener diversity formula used for calculating plant diversity.
  - Potential applications for data leaders:
    - Informing green/blue data assets related to coastal vegetation, ecosystem services, and carbon stock assessments.
    - Supporting analyses of spatial patterns in vegetation structure and diversity across UK saltmarshes.
    - Integrating with broader data systems to enhance understanding of habitat quality and carbon storage potential.

- Data governance considerations
  - Metadata-rich dataset with explicit field definitions and sampling design.
  - Data quality notes indicate independent surveys and expert calibration, but some quality-control details are not specified (NA for certain procedures).
  Spatial and temporal metadata enable discoverability and reproducibility across UK sites and time periods.
  Licensing, access rights, and data usage terms are not stated; practitioners should verify permissions before reuse.