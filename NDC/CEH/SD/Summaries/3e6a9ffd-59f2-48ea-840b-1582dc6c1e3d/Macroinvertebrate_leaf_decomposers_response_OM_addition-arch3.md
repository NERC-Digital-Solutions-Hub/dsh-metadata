# Macroinvertebrate leaf decomposers of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates how leaf litter addition affects macroinvertebrate leaf decomposers in Welsh upland streams.
- Uses a BACI (before-after-control-impact) design across eight streams to compare upstream reference (control) zones with downstream experimental zones.

## Experimental design and intervention
- Each stream has:
  - Upstream reference (control) zone
  - Downstream experimental (manipulated) zone
  - Approximately 20–50 m separation to maintain independence
- Timeline:
  - Before period (T1): 61–65 days from Nov 2012 to Jan 2013 with no manipulation; both zones treated equally
  - After period (T2): 57–62 days from Jan to Mar 2013 with leaf litter addition in the experimental zone
- Organic matter addition:
  - One-tonne bags of deciduous leaves (oak, birch, alder) added to the experimental zone proportionally to area
  - Vegetable nets used to maintain minimum wet weight of 1.7 kg m^-2
  - Additional leaf litter (630 kg wet weight) added on 12 Feb and 5 Mar 2013 after storm events
- Litter bag design:
  - Nylon mesh bags (10 x 15 cm) with apertures of 500 µm (fine) and 5 mm (coarse) to control invertebrate colonization
  - Each bag contained ~5 g air-dried leaves
  - 48 replicate bags per stream (24 reference, 24 experimental; 24 fine, 24 coarse), totaling across 8 streams
  - Bags fixed to poles and covered with cobbles; submerged under low flow

## Sampling, collection, and processing
- Collection points:
  - End of before period (T1): half of the bags removed (6 fine and 6 coarse per zone per stream) and 6 new bags added to measure after-manipulation decomposition (T2)
  - End of after period (T2): remaining bags from T0 and bags added at start of T2 collected
  - Labels: T1-A through T2-A, with replicates A–F
- On-site preservation and lab processing:
  - Litter bags preserved in 70% ethanol on-site
  - Transported to lab; material rinsed through 250 µm sieve; dried to constant mass
  - Macroinvertebrates identified to species where possible; some taxa identified at genus, family, or coarse levels (e.g., Chironomidae, Oligochaeta)
  - Identification primarily via microscopy
- Measured values:
  - Invertebrate abundance per taxon (species-level when possible)

## Data structure and metadata
- Primary data: Bag data with 10 columns
  - site_code, region, date, time (before/after), landuse, reach (experimental or control), Replicate, BagMesh, taxon_name, abundance
- Supporting data:
  - Site description file (DURESS_CU_site_description.csv) containing
    - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
    - Survey/Catchment information and campaign context
- Taxonomic resolution:
  - Species-level where possible; otherwise genus, family, or coarse levels

## Data quality and governance considerations
- Calibration steps: None reported
- Quality control: None described
- Data processing and transformation: Not explicitly detailed beyond standard lab processing
- Metadata availability:
  - Site coordinates and catchment information available via site description file
  - Clear labeling of sampling periods and replication scheme to support reproducibility
- Data accessibility:
  - Data structure and accompanying site metadata provided; potential barriers if metadata are incomplete or not openly shared beyond provided files

## Relevance for monitoring frameworks
- Demonstrates a robust BACI approach to detect ecological responses to controlled organic matter inputs
- Provides a detailed data architecture for ecological monitoring, including:
  - Clear temporal phases (before/after) and spatial design (reference vs. experimental zones)
  - Replication strategy and standardized sampling via mesh litter bags
  - Transparent data fields enabling downstream quality checks, trend analyses, and policy-relevant assessments of ecosystem functioning (leaf litter decomposition and macroinvertebrate communities)
- Highlights practical considerations for data stewardship in monitoring programs:
  - Importance of metadata (location, land use, reach type, sampling dates)
  - Need for clear documentation of sample processing (preservation, sieve size, taxonomic resolution)
  - Potential need for explicit quality control steps to ensure data reliability for policy evaluation and future decision-making