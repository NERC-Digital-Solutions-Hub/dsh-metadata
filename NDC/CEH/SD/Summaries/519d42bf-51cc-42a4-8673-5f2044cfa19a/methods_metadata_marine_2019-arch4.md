# Methods, metadata and summary for marine monitoring at Akrotiri and Dhekelia between April 2017 and September 2018

## Overview
- Project purpose: Defra Darwin Initiative Plus Project DPLUS056 to assess current and future invasive alien species (IAS) in Cyprus and establish baseline data on native and non-native marine species in the Sovereign Base Area of Akrotiri and Dhekelia.
- Organisers: University of Cyprus (UCY) and volunteer divers from the Western Sovereign Base Area Sub Aqua Club.
- Timeframe: Sampling conducted from April 2017 to September 2018, with baseline survey in Dhekelia.

## Methods and study area
- Primary method: Underwater Visual Census (UVC) to record marine invasive species.
- Location: In front of the Sub-aqua club at the RAF base, Akrotiri.
- Seasonal sampling: Conducted on multiple dates throughout the year.

## Sampling design and procedures
- Transects (habitat coverage): On each sampling date, an 85 m total transect area was randomly placed; three replicate 25 m transects were surveyed with 5 m gaps between them.
- Fish assessments: Strip transects of 25 m length by 5 m width (25 x 5 m2). Divers recorded fish species and estimated abundances within 2.5 m on each side of the transect as they swam along the 25 m line.
- Benthic assessments: Point intercept photo transects along all three 25 m replicate transects. A 20 x 20 cm quadrat was placed every 1 m along the transects, equipped with an underwater camera (GoPro) and lighting; photos were taken at each 1 m point to record species and abundance from the imagery.
- Additional baseline: Separate baseline survey conducted in Dhekelia to complement Akrotiri data.

## Metadata and data structure
- Data files:
  - akrotiri_marine_2017_2019: contains sampling site location and fish species abundance data.
  - akrotiri_marine_quadrats_2017_2018: contains sampling site location and benthic (algae and invertebrates) species abundance data.
- Data columns (Akrotiri fish dataset):
  - Date (sampling date)
  - Site_code (site short code)
  - Site_full_name (site full name)
  - Lat (latitude, decimal degrees)
  - Lon (longitude, decimal degrees)
  - Species (recorded species)
  - Species_common (common name)
  - Taxonomic_group (taxonomic category)
  - Abundance (ACFOR scale)
  - Abundance_num (ACFOR scale numbers)
  - Method (recording method: diving, snorkelling)
- Data columns (Akrotiri quadrats dataset):
  - Date, Site_code, Site_full_name, Lat, Lon, Species, Taxonomic_group
  - Species_Cov_% (species percentage cover)
  - Method (recording method: diving, snorkelling)

## Data quality and stewardship
- Quality assurance/quality control (QA/QC): All equipment and protocols developed by experienced UCY staff; data collection methods demonstrated to volunteer divers.
- Data processing: All incoming data reviewed and digitised by UCY staff.
- Data provenance: Data collected by UCY researchers with support from volunteer divers; explicit documentation of methods and site metadata.

## Data availability and accessibility
- Data are organized into clearly defined CSV files with structured metadata describing dates, locations, taxa, abundances, and methods, enabling reproducibility and cross-site comparison.

## Implications for data leaders
- Governance and standards: The project demonstrates clear data ownership, metadata structure, and QA/QC processes essential for reliable data ecosystems.
- Metadata clarity: Explicit column definitions and sampling protocols support discoverability and re-use by policy colleagues and external partners.
- Data integration prospects: Two complementary datasets (fish abundance and benthic cover) enable integrated analyses of community changes and IAS baselines.
- Accessibility and reuse: Standardized formats (CSV) and documented methods facilitate sharing with wider networks and future monitoring programs.
- Data gaps and extension: Baseline data in Akrotiri with a supplementary Dhekelia site highlight the importance of scalable, repeatable sampling to address spatial gaps and temporal dynamics.