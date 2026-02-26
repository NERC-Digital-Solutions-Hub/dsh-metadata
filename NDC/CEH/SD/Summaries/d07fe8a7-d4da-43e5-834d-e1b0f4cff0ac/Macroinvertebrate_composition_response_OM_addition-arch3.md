# Macroinvertebrate composition of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates how macroinvertebrate communities respond to increased organic matter in Welsh upland rivers using a BACI (before-after-control-impact) design.
- Compares an upstream reference zone with a downstream experimental zone within each stream to isolate effects of leaf litter addition.
- Data collection spans before (T1) and after (T2) manipulation periods, with ongoing sampling to track community and body size changes.

## Experimental design details
- Setup: Each stream split into upstream reference and downstream experimental zones; ~20–50 m between zones to ensure independence.
- Timeline:
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated identically.
  - After period (T2): 57–62 days (early Jan 2013 to Mar 2013); experimental zone receives leaf litter additions to simulate increased organic matter.
- Manipulation:
  - One tonne bags of deciduous leaves (oak, birch, alder) distributed proportionally to experimental zone area.
  - Vegetable nets used to maintain minimum wet weight (1.7 kg/m2) in experimental zones.
  - Leaf packs fixed in place; additional 630 kg (wet weight) of leaf litter added on Feb 12 and Mar 5 after storm events.
  - Goal: maintain loose leaf litter throughout the experimental stretch.
  
## Sampling and collection methods
- Invertebrate sampling: Surber net (0.1 m2, 330 µm mesh, 10 cm depth); six random samples per reach on five occasions (January–May 2013).
- Preservation: On-site storage in 70% IMS; laboratory processing includes rinsing through a 350 µm sieve and preservation in 70% IMS.
- Taxonomy: Identification to species level where possible; otherwise genus, family, or coarse levels.
- Morphometrics: Body measurements (Size1 and Size2) in mm; record head width or body length; accompanying comments indicate measurement type.
  
## Data and metadata
- Data structure: Flat CSV files with 11 columns.
  - Key columns: site_code, region, month, time (Before/After), landuse, reach (Experimental or Control), replicate, taxon_name, Size1, Size2, and size-related comments.
- Supporting site data: Site description CSV with 10 columns including site_code, name, coordinates (Eastings/Northings, Latitude/Longitude), elevation, grid reference, survey campaign, and catchment information.
- Calibration and quality control:
  - No explicit calibration steps reported.
  - No formal quality control procedures documented.

## Relevance for monitoring and governance (for monitoring framework authors)
- Demonstrates a clear BACI design to attribute ecological responses to a specific stressor (organic matter input) while controlling for background variation.
- Highlights the importance of:
  - Defining independent reference and treatment zones and maintaining adequate separation.
  - Consistent, repeatable sampling regimes across time to detect temporal changes.
  - Detailed metadata and data dictionaries (e.g., explicit column definitions and site descriptors) to enable transparent data reuse and governance.
- Data management considerations:
  - Some metadata gaps and the need for robust data governance to ensure metadata completeness, data provenance, and timely data sharing.
  - Potential barriers to data reuse include lack of documented calibration steps and QA procedures.
- Practical constraints and data handling:
  - Resource-intensive field manipulations (leaf litter enrichment) and the need to document deployment specifics for reproducibility.
  - The necessity of standardized units and taxonomic resolution to enable cross-study comparisons and policy-relevant reporting.