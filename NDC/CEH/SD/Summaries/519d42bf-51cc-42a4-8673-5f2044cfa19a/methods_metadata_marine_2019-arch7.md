# Methods, metadata and summary for marine monitoring at Akrotiri and Dhekelia between April 2017 and September 2018

## Overview
- Marine monitoring conducted April 2017–September 2018 as part of Defra Darwin Initiative Plus Project DPLUS056.
- Aim: assess native and non-native marine species in the Sovereign Base Area of Akrotiri and Dhekelia.
- Organisations: University of Cyprus (UCY) and volunteer divers from the Western Sovereign Base Area Sub Aqua Club.
- Data products are organized into two CSV files containing spatially referenced observations.

## Study design and scope
- Location: in front of the Sub-aqua club at the RAF base, Akrotiri; baseline survey also conducted in Dhekelia.
- Sampling regime: seasonal field campaigns.
- Focus: marine invasive species and benthic (algae and invertebrate) assemblages across different habitats (seagrass beds and rocky areas).

## Methods
- Underwater Visual Census (UVC) to record marine invasive species.
- Transect layout:
  - One transect of 85 m total length randomly placed, covering available habitats.
  - Three replicate transects: 25 m each with 5 m gaps between them.
- Fish assessments:
  - Strip transects: 25 m long by 5 m wide (divers record species observed within 2.5 m on each side per 25 m transect).
  - Data captured: species, observed abundance (ACFOR scale), and numeric abundance.
- Benthic sampling (algae and invertebrates):
  - Point intercept photo transects along all three 25 m transects.
  - On-transect quadrats: 20 cm x 20 cm PVC quadrats placed every 1 m.
  - Photography via GoPro with lighting; species and abundance recorded from photos.
  
## Data products and data schema
- akrotiri_marine_2017_2019
  - Content: sampling site location and fish species abundance.
  - Key fields: Date, Site_code, Site_full_name, Lat, Lon, Species, Species_common, Taxonomic_group, Abundance (ACFOR), Abundance_num, Method.
- akrotiri_marine_quadrats_2017_2018
  - Content: sampling site location and quadrat-based benthic species abundance.
  - Key fields: Date, Site_code, Site_full_name, Lat, Lon, Species, Taxonomic_group, Species_Cov_%, Method.
- Data capture fields:
  - Date (sampling date)
  - Site_code / Site_full_name (site identifiers)
  - Lat / Lon (decimal degrees)
  - Species / Taxonomic_group
  - Abundance / Abundance_num (fish)
  - Species_Cov_% (percent cover for quadrats)
  - Method (recording method: diving, snorkelling)

## Spatial information
- Spatial references: latitude and longitude provided in decimal degrees for each observation.
- Granularity: transect-level and 1 m interval quadrat sampling along each transect (spatially explicit data suitable for GIS mapping and analysis).

## Data quality, provenance and workflow
- Quality assurance: equipment and protocols developed by UCY staff; methods presented to volunteer divers.
- Data handling: all incoming data reviewed and digitised by UCY staff.
- Primary contacts: Monica Demetriou (demetriou.monica@ucy.ac.cy).

## Project context and access
- Project: Defra Darwin Initiative Plus Project DPLUS056.
- Access format: CSV data files described above, ready for import into GIS and other data-analysis workflows.