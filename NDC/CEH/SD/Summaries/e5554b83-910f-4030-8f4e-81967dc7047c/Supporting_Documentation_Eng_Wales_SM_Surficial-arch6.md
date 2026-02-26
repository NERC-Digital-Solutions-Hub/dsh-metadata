# Supporting documentation for data resource Eng_Wales_SM_Surficial.csv

## Overview
- Data resource documenting dry bulk density, loss on ignition (LOI), and organic carbon content for surficial soils (top 10 cm) from 212 samples across 49 saltmarshes in England and Wales.
- Timeframe: sampling conducted January 2018 – December 2019; no repeat sampling planned.
- Study purpose aligned with carbon stock assessment in saltmarshes; part of the C-SIDE project and CarbonQuest citizen science program.
- Variables captured include soil texture, dry bulk density, LOI (organic matter content), and organic carbon content; location data provided in multiple coordinate formats (lat/long WGS84, OSGB grid, easting/northing).

## Data collection and provenance
- Sampling method: soil collected with a 50 ml syringe to a depth of 10 cm.
- GPS and location: locations recorded using various methods (mobile phones, handheld units, RTK); site coordinates provided in multiple formats.
- Sample handling: soils frozen at -20°C until analysis.
- Soil classification: texture categorized as organic, sandy, or not sandy using Ford et al. (2019) methodology; four researchers independently classified texture for QC.
- Laboratory analyses:
  - Dry bulk density calculated from dry mass and sample volume after drying at 60°C for 72 hours.
  - LOI determined by combusting dried milled samples at 450°C for 4 hours.
  - Organic carbon measured with Elemental Analysis (Carlo Erba NA-1500 or equivalent) after acidification to remove carbonates.
- Calibration and QA: elemental analyzer calibrated with Acetanilide; repeated analysis of standard (B2178) across runs; citizen science participants QC’d by salt marsh scientists; GPS coordinates cross-checked against habitat maps and aerial photos.

## Data structure and formats
- Main data format: CSV.
- Data resource description fields include:
  - Saltmarsh_Name, Nation, Year, Lat_dec_deg, Long_dec_deg, Grid_Reference, X_easting, Y_northing.
  - Sampling_Method, Depth_cm.
  - Dry_Bulk_Density_g_cm_3, Soil_Texture, OC_Perc (organic carbon %), LOI_Perc (organic matter %).
- Data resource description table supports multiple observations per site; explicit units and cell formats noted (e.g., Lat/Long in decimal degrees, Grid Reference as text, numeric fields for densities and percentages).

## Quality assurance and validation
- Citizen science entries undergo visual and contextual QC by experienced scientists; GPS coordinates validated against habitat maps and aerial imagery.
- Soil texture classifications obtained independently by four team members to ensure consistent categorization.
- Analytical procedures followed established methodologies with documented calibration and standards to ensure comparability across samples and sites.

## Usage, accessibility, and potential data products
- Data are provided in a structured CSV suitable for integration into dashboards, pivot analyses, or self-serve exploration by end users.
- Rich location data enables geospatial analyses and site-level carbon stock assessments across England and Wales saltmarshes.
- Clear documentation of methods and references supports replication, data reuse, and integration with broader carbon stock models.

## Relevance to data work and potential analyses
- Supports cross-site comparisons of dry bulk density, LOI, and organic carbon content in surficial saltmarsh soils.
- Enables estimation of carbon stocks at the saltmarsh level when combined with area and depth assumptions.
- Open to methodological evaluation and potential meta-analyses with other saltmarsh datasets.

## Notes and references
- Sampling and analytical procedures reference key works:
  - Craft et al. (1991) on LOI and carbon/nitrogen estimation.
  - Dadey et al. (1992) on dry bulk density determination.
  - Ford et al. (2019) large-scale salt-marsh carbon stock predictions.
  - Nieuwenhuize et al. (1994) and Verardo et al. (1990) methodologies for organic carbon analyses.
- No statistical treatment is indicated (NA) in the data description; no repeat sampling planned.