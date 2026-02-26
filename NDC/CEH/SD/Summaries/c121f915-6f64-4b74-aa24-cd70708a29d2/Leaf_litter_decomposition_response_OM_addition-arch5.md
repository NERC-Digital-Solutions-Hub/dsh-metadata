# Leaf litter decomposition of Welsh upland rivers in response to organic matter addition

## Objective and dataset scope
- Reports a BACI (before-after-control-impact) study to assess leaf litter decomposition in Welsh upland rivers.
- Involves upstream reference (control) and downstream experimental (treatment) zones across multiple streams.
- Aims to capture decomposition dynamics under added organic matter (leaf litter) over defined before (T1) and after (T2) periods, with Jan 2013 marking the start of manipulation.

## Experimental design
- Each stream split into:
  - Upstream reference zone (control)
  - Downstream experimental zone (manipulated)
- Separation: 20–50 m between zones to ensure independence.
- Periods:
  - Before period (T1): 61–65 days, Nov 2012–Jan 2013; no manipulation, both zones treated similarly.
  - After period (T2): 57–62 days, Jan–Mar 2013; experimental zone received leaf litter additions.
- Leaf litter addition:
  - One tonne bags containing deciduous leaves (oak, birch, alder) added proportionally to experimental zone area.
  - Vegetation net bags maintained at ~1.7 kg/m2 (wet weight) in experimental zones; additional 630 kg of leaf litter added on 12 Feb and 5 Mar 2013 after storm events.
- Timepoints:
  - T0: initial placement
  - T1: start of leaf addition to experimental reach
  - T2: end of experiment

## Sampling, collection, and preservation methods
- Litter bags:
  - Collected and replaced in both reference and experimental zones at T1 and T2 for decomposition measurement.
  - Sampling labels: T1 and T2 for different bag sets; remaining bags labeled T18 (left ~18 weeks) and T2 (end of experiment).
- Handling on site:
  - Bags preserved in 70% ethanol in labeled containers and transported to the lab.
- Laboratory processing:
  - Leaf material rinsed through a 250 µm sieve to remove sediments.
  - Air-dried to constant mass; macroinvertebrates separated from contents.
  - Subsampled leaves (1 g) combusted at 500°C to estimate ash-free dry mass (AFDM).

## Analytical methods
- AFDM estimation follows standard methods (Benfield 2006, Methods in Stream Ecology).
- Data representation focuses on:
  - Percentage of leaf mass remaining in fine and coarse mesh bags.
  - Decomposition rates (percent mass loss per day) for fine and coarse bags.

## Data structure and recorded variables
- Data format: flatbed comma-separated values (CSV).
- Leaf litter decomposition data columns (illustrative, as listed in the document):
  - site
  - Code of the sampling site
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
- Note: The document references 10 columns but lists more than 10 field headings; the dataset includes site, location, timing, replication, and both fine and coarse bag mass retention and loss rates.

## Supporting metadata and site description
- Supporting file: DURESS_CU_site_description.csv
  - Fields include: Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey campaign, and catchment information.
- Site metadata facilitates georeferencing and integration with other datasets (catchment, land-use, grid references).

## Data provenance, references, and accessibility
- Data collection and processing align with standard stream ecology protocols; reference method cited: Benfield (2006).
- Meaningful for data discovery and reuse via CEH Data Catalogue Records; links may be updated over time, and the EIDC cannot guarantee link persistence.
- Data lineage supports reproducibility: on-site preservation, lab processing steps, and measurement of AFDM enable traceable mass-loss results.

## Data governance and quality considerations for Data Stewards
- Ensure metadata completeness: capture sampling zone definitions, dates, and replication details for each stream.
- Metadata alignment: verify site codes, land-use classifications, region naming, and reach designations to support cross-dataset interoperability.
- Standardization: confirm column naming and unit consistency (percent remaining, loss per day) across datasets and future updates.
- Provenance and versioning: maintain clear records of T1 vs T2 bag sets, replacement events, and any additional litter additions after storm events.
- Accessibility: link data to the supporting site description file and reference materials; monitor and update data catalogue entries as needed.
- Quality control: account for potential variability in bag degradation rates due to environmental conditions (storm events, hydrology) and ensure transparent documentation of any data gaps or anomalies.