# Methods, metadata and summary for marine monitoring at Akrotiri and Dhekelia between April 2017 and September 2018

## Overview
- Project under Defra Darwin Initiative Plus Project DPLUS056: Assessment and monitoring of current and future IAS in Cyprus to establish baseline data on native and non-native marine species in the Sovereign Base Area of Akrotiri and Dhekelia.
- Conducted by the University of Cyprus with volunteer divers from the Western Sovereign Base Area Sub Aqua Club.
- Aims to monitor marine invasive species using standardized sampling and metadata to support data discovery and reuse.

## Study design and field methods
- Underwater Visual Census (UVC) used to record marine invasive species.
- Seasonal sampling conducted in front of the Sub-aqua club at Akrotiri RAF base.
- Transect setup: 85 m total length, three 25 m replicate transects with 5 m gaps, covering habitats such as seagrass beds and rocky areas where possible.
- Fish assessments: Strip transects (25 m x 5 m) with divers recording species and abundances within 2.5 m on each side of the transect.
- Benthic species recording: Point-intercept photo transects along all three 25 m transects; a 20x20 cm quadrat placed every 1 m along the transect, photographed with a GoPro.
- Baseline survey conducted in Dhekelia in addition to Akrotiri.

## Data and metadata structure
- Data collected are organized into two CSV files:
  - akrotiri_marine_2017_2019: sampling site location and fish species abundance.
  - akrotiri_marine_quadrats_2017_2018: sampling site location and quadrat species abundance (benthic, algae, invertebrates).
- Data fields and structure:
  - akrotiri_marine_2017_2019:
    - Date (sampling date), Site_code (short code), Site_full_name (site name), Lat, Lon (decimal degrees), Species, Species_common (common name), Taxonomic_group, Abundance (ACFOR scale), Abundance_num (ACFOR numeric), Method (recording method: diving, snorkelling).
  - akrotiri_marine_quadrats_2017_2018:
    - Date, Site_code, Site_full_name, Lat, Lon, Species, Taxonomic_group, Species_Cov_% (percent cover), Method (recording method).
- Data type and units:
  - Abundance uses ACFOR scale with corresponding numeric values.
  - Spatial coordinates provided in decimal degrees.
  - Quadrat data provide percent cover for benthic species.
- Documentation is embedded in the file descriptions and field definitions to support interpretation and reuse.

## Data quality, provenance and governance
- Quality control/assurance performed by experienced University of Cyprus staff.
  - Equipment and protocols developed by UCY.
  - All incoming data reviewed and digitised by UCY staff.
  - Methods presented to volunteer divers to ensure consistency.
- Provenance: data collection methods, field procedures, and data digitisation processes are documented and controlled by UCY, ensuring traceability from field collection to digital records.

## Scope, timing and location
- Temporal coverage: April 2017 to September 2018 for Akrotiri; baseline survey in Dhekelia included.
- Spatial scope: Akrotiri area (in front of the Sub-aqua club, RAF Akrotiri) with supplementary baseline data from Dhekelia.
- Data capture targets: presence and abundance of marine invasive/native species, including both fish and benthic communities.