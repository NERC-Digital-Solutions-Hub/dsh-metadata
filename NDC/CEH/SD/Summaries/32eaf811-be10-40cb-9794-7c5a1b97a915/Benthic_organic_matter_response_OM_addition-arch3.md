# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates how benthic organic matter (BOM) in Welsh upland rivers responds to added leaf litter using a controlled BACI design.
- Aims to inform environmental health monitoring by linking organic matter inputs to BOM stocks, informing management decisions in catchments.

## Experimental design
- BACI (before-after-control-impact) setup with each stream split into:
  - Upstream reference (control) zone
  - Downstream experimental (manipulated) zone
- Independent zones separated by 20–50 meters to ensure independence; similar habitat structure across zones.
- Time phases:
  - T1 (before): 61–65 days, Nov 2012 to Jan 2013; no manipulation, equal treatment of zones
  - T2 (after): 57–62 days, Jan–Mar/Apr 2013; experimental zone receives leaf litter addition
- Leaf litter addition:
  - One-tonne bags of oak, birch, and alder leaves proportionally distributed to the experimental zone
  - Vegetable net bags used to maintain minimum wet weight (1.7 kg m^-2); materials deployed above the experimental zone
  - Additional leaf litter (630 kg wet weight) added after two large storm-flow events (12 Feb and 5 Mar 2013)

## Sampling regime
- Six random BOM samples collected per stream across five collection months: January, February, March, April, May 2013
- Sampling method: Surber net (0.1 m^2, 330 µm mesh, 10 cm depth)
- On-site preservation in 70% IMS; lab processing included rinsing, separating macroinvertebrates, drying, and weighing BOM to 0.01 g

## Laboratory processing and analytical methods
- BOM processing:
  - Macroinvertebrates removed; remaining material dried and weighed
  - Subset samples combusted at 550°C for 5 hours to determine ash-free organic matter
- Units recorded: grams of organic matter (coarse and fine particulate)

## Data structure and variables
- Data format: flatbed CSV files
- Core BOM dataset columns (10 total):
  - site_code (sampling site)
  - landuse (basin land-use)
  - region (stream basin)
  - time (Before/After manipulation)
  - month (collection month)
  - reach (Experimental or Control)
  - replicate (replicate code)
  - surber_area (area of Surber sampler in m^2)
  - cpom (coarse particulate organic matter, g)
  - fpom (fine particulate organic matter, g)
- Supporting dataset: site_description.csv with site metadata (Site_code, name, coordinates, grid reference, elevation, catchment, survey campaigns)

## Quality control and metadata
- Calibration steps: None documented
- Quality control: None documented
- Metadata availability:
  - Detailed sampling and site metadata provided in separate site_description file
  - Data structure and measurement methods clearly described to facilitate reuse

## Temporal and geographic scope
- Timeframe: November 2012 to May 2013 (with specific manipulation in January 2013 and ongoing leaf litter addition during T2)
- Geography: Welsh upland river catchments; field sampling via Surber nets in multiple reaches per stream

## Relevance for monitoring frameworks
- Demonstrates a rigorous monitored manipulation (BACI) to assess ecosystem response to organic matter inputs.
- Highlights the importance of:
  - Clear experimental controls and independence between study zones
  - Standardized sampling methods and transparent data structures
  - Thorough documentation of metadata (site, habitat, sampling campaign)
- Points to practical data governance needs:
  - Availability of raw data and accompanying metadata for transparency and reproducibility
  - Awareness of potential data quality gaps (no QA steps recorded) when integrating into policy-relevant dashboards or reports
  - The need for consistent data sharing practices and open data standards to support wider policy analysis

## Limitations and considerations for use
- No explicit quality control or calibration steps reported; data users should consider this in interpretation.
- Metadata completeness beyond the site description is not detailed; users may need to assess full data provenance and processing steps.
- The study focuses on BOM response to leaf litter addition over a limited temporal window; extrapolation to long-term policy scenarios should be cautious.