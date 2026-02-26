# Leaf litter decomposition of Welsh upland rivers in response to organic matter addition

## Overview
- Study investigates how leaf litter decomposition responds to added organic matter in Welsh upland rivers.
- Uses a before-after-control-impact (BACI) design across streams with upstream reference and downstream experimental zones.
- Periods:
  - Before period (T0/T1): 61–65 days with no manipulation; both zones treated equally.
  - After period (T2): 57–62 days during which the experimental zone received leaf litter additions to simulate natural senescence and abscission.
- Leaf litter sources: oak, birch, and alder; bags placed in the experimental zone to track decomposition under increased organic matter input.
- Measurements focus on the percentage of leaf mass remaining in fine and coarse mesh bags, and decomposition rates.

## Experimental Design
- Each stream divided into:
  - Upstream reference (control) zone
  - Downstream experimental zone
- Independent arrangement ensured by a 20–50 m gap between zones.
- Leaf litter additions:
  - One tonne bags distributed proportionally by experimental zone area.
  - Vegetative nets maintained to ensure a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Additional 630 kg (wet weight) of leaf litter added on 12 February 2013 and 5 March 2013 after two storm events.
- Time markers:
  - T0: initial placement of leaf bags
  - T1: start of the after period with leaf addition
  - T2: end of the experimental period

## Sampling & Collection Methods
- At the end of the before period (T1):
  - Half of the litter bags (6 fine + 6 coarse per pole) removed from both reference and experimental zones.
  - 6 new fine mesh and 6 new coarse mesh bags added to each pole for measuring decomposition during T2.
- At the end of the after period (T2):
  - Remaining half of bags from T0 and bags added at T2 removed.
  - Those from T0 designated as T18 (left ~18 weeks) and those from T2 as T2.
- On-site processing:
  - Litter bags preserved in 70% ethanol in labelled polystyrene bags.
  - In the lab: leaf material rinsed through 250 µm sieve, air-dried to constant mass; macroinvertebrates separated.
  
## Analytical Methods
- Mass loss measurement:
  - Leaves rinsed, subsampled (1 g) and combusted at 500°C to estimate ash-free dry mass (AFDM).
  - Method aligned with Benfield (Methods in Stream Ecology, 2006).
- Output units:
  - Percentage of leaf mass remaining in fine and coarse mesh bags.
- References and data provenance notes:
  - CEH Data Catalogue referenced for links to sources; links may not be permanent.

## Data Structure & Variables
- Data files: flatbed CSVs.
- Leaf litter decomposition dataset includes 10 columns:
  - site, Code of the sampling site, landuse (stream basin), region (basin land-use), reach (experimental or control), t0 (date bags placed), t1 (date of leaf addition to the experimental reach), t2 (end date), days (length of experiment), time (Before or After manipulation), replicate (replicate code), fine.percent.remaining, coarse.percent.remaining, fine.precent.loss.day-1, coarse.precent.loss.day-1.
- Endpoints:
  - Fine and coarse mesh bag data as percentages remaining.
  - Decomposition rates expressed as percent loss per day for each mesh type.

## Supporting Data / Metadata
- DURESS_CU_site_description.csv:
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey campaign (e.g., WAWS-Welsh Acid Water Survey), Catchment information.
- Provides site-level context (coordinates, catchment, campaign) to enable spatial linkage and metadata enrichment.

## Potential Analyses & Considerations for Analysts
- BACI framework enables assessment of causal effects of organic matter addition on leaf litter decomposition by comparing before/after changes between reference and experimental zones.
- Compare decomposition rates (fine vs coarse mesh) to understand size-class dependent effects of added organic matter.
- Cross-stream variation by region, landuse, and reach type can be explored using hierarchical models.
- Temporal dynamics: use t0, t1, t2 and days to model decomposition trajectories and rate changes over the manipulation period.
- Data quality and integration considerations:
  - Zone independence relies on a 20–50 m separation; ensure proper stratification by stream.
  - Storm-event additions and timing may influence decomposition beyond the deliberate additions; account for this in models.
  - Data completeness and consistency across sites (replicates) are essential for robust inference.
- Metadata linkage:
  - Utilize site_description metadata to incorporate spatial controls and environmental covariates (e.g., elevation, coordinates) in analyses.