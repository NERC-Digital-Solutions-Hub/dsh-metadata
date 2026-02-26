# Leaf litter decomposition of Welsh upland rivers in response to organic matter addition

## Overview
- A BACI (before-after-control-impact) study across multiple streams with an upstream reference zone and a downstream experimental zone to test leaf litter decomposition under added organic matter.
- Experimental arrangement includes a short separation between reference and experimental zones to ensure independence.
- Before period (T1): 61–65 days (Nov 2012–Jan 2013) with no manipulation; after period (T2): 57–62 days (Jan–Mar 2013) where leaf litter was added to the experimental zone.
- Leaf litter supplementation used one-tonne bags containing oak, birch, and alder, distributed proportionally to experimental zone area; additional 630 kg wet weight added after two storm-flow events during T2.
- Sampling objective: quantify leaf litter decomposition through changes in leaf mass in fine and coarse mesh litter bags.

## Experimental design
- Each stream divided into:
  - Upstream reference (control)
  - Downstream experimental (treatment)
- Zones similar in length and habitat structure; ~20–50 m between zones for independence
- Time periods:
  - T0: initial setup
  - T1: before manipulation (no difference between zones)
  - T2: after manipulation (leaf litter addition in experimental zone)

## Data collection methods
- Litter bags:
  - Fine mesh and coarse mesh bags used to track decomposition.
  - Half of bags removed at the end of T1; new bags deployed to measure decomposition during T2.
  - Bags labeled as T1 (initial) and T2 (end of experiment); some bags left in place for ~18 weeks (T18) for comparison.
- Sample handling:
  - On collection, bags preserved in 70% ethanol and transported to the lab.
  - In the lab: leaf material rinsed (250 µm sieve), air-dried, and macroinvertebrates separated.
- Analytical approach:
  - 1 g subsample combusted at 500°C to estimate ash-free dry mass (AFDM).
  - Documentation references standard methods (Benfield 2006, Methods in Stream Ecology).

## Data structure and contents
- Leaf litter decomposition data stored as flatbed CSV with 10 columns:
  - site
  - landuse
  - region
  - reach
  - t0
  - t1
  - t2
  - days
  - time
  - replicate
  - fine.percent.remaining
  - coarse.percent.remaining
  - fine.precent.loss.day-1
  - coarse.precent.loss.day-1
- Measurements reflect percentage of leaf mass remaining in fine and coarse mesh bags, plus decomposition rate estimates.
- Supporting site metadata (DURESS_CU_site_description.csv) include:
  - Site_code, Name, Eastings, Northings
  - Grid, Latitude, Longitude, Elevation
  - Survey campaign (WAWS-Wye survey, Plynlimon catchment, etc.)
  - Catchment information

## Spatial data and GIS readiness
- Site coordinates provided in British National Grid and WGS84 (Latitude/Longitude), enabling map-based visualization.
- Data structure supports linking decomposition results to precise locations and catchment contexts.
- Potential GIS uses:
  - Map experimental vs. control zones across streams.
  - Visualize spatial patterns of decomposition rates and litter remaining by site.
  - Overlay with land-use, catchment characteristics, and hydrology for spatial analyses.
  - Temporal analysis by aligning T0, T1, T2 dates with map layers.

## Supporting documentation and metadata
- Site description file details each sampling site with precise coordinates and catchment information.
- References to standard methods and data cataloging (CEH Data Catalogue) for traceability.
- Some links may be subject to change; data references indicate where to locate supporting material.

## Data considerations for GIS implementation
- Data reside in multiple sources (decomposition dataset and site metadata) requiring careful joins on site/reach identifiers.
- Consistent site coding and harmonization between litter data and site description are essential.
- Measurements include a mix of percentages and rates; unit consistency and clear handling of “percent remaining” versus “percent loss per day” are important for visualization and analysis.
- Potential data quality considerations include date formats, minor typographical inconsistencies (e.g., “precent”), and ensuring accurate mapping of before/after designations.