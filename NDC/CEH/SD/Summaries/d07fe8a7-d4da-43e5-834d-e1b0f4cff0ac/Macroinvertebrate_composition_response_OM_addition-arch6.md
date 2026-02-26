# Macroinvertebrate composition of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates how macroinvertebrate communities respond to organic matter addition (leaf litter) in Welsh upland rivers using a BACI design.
- Compares upstream reference (control) and downstream experimental (treatment) zones within each stream.

## Experimental design
- BACI structure: each stream has an upstream reference zone and a downstream experimental zone, separated by 20–50 m to maintain independence.
- Time periods:
  - Before period (T1): 61–65 days, early Nov 2012 to early Jan 2013. January samples are included in the before period.
  - After period (T2): 57–62 days, early Jan 2013 to March 2013. February–April samples are included in this period.
- Leaf litter manipulation (T2):
  - One tonne bags containing deciduous leaves (oak, birch, alder) distributed proportionally by experimental zone area.
  - Vegetation litter bags maintained to a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Additional leaf litter (630 kg wet weight) added on 12 Feb 2013 and 5 Mar 2013 after two storm-flow events.

## Sampling regime and collection methods
- Sampling: six random macroinvertebrate samples per reach, on five occasions (January, February, March, April, May 2013).
- Method: Surber net sampler (0.1 m^2, 330 µm mesh, 10 cm depth).
- Preservation: on-site in 70% IMS; in lab, rinsed, macroinvertebrates separated from debris, preserved in 70% IMS.
- Taxonomy and measurements:
  - Identification to species level when possible; otherwise genus, family, or coarse level.
  - Size measurements (Size1 and Size2) in millimeters; taxon-specific body measurements recorded with a note in Comment indicating head width or body length.

## Data structure and files
- Surber data: flatbed CSV with 11 columns:
  - site_code, region, month, time (Before/After), landuse, reach (Experimental or Control), replicate, taxon_name, Size1, Size2, Comment.
- Site description: DURESS_CU_site_description.csv (10 columns):
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.

## Data quality and considerations
- Calibration: None documented.
- Quality control: No explicit QC steps described.
- Taxonomic resolution may vary by specimen; data include both species-level identifications and higher-level designations where species-level ID was not possible.

## How this data can be used (data support perspective)
- Create biodiversity metrics:
  - Taxa richness, abundance per site, period, and treatment.
  - Size distribution analyses using Size1 and Size2.
- Analyze community responses:
  - BACI-style comparisons of upstream (control) vs downstream (experimental) across Before and After periods.
  - Multivariate analyses (ordination) to assess shifts in community composition due to leaf litter addition.
- Data integration and products:
  - Link Surber data with site metadata (geography, catchment) using site_code.
  - Generate dashboards or reports that enable end-users to explore changes over time and between zones.
- Practical data cleaning and preparation:
  - Ensure consistent taxon naming across records.
  - Handle missing Size1/Size2 values and interpret measurements via the Comment field (head width vs body length).
  - Validate linkage between Surber records and corresponding site descriptions for spatial analyses.