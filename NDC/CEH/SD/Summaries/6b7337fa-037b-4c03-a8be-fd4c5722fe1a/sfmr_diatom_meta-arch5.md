# Diatom data: Short working title: Diatom data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Purpose: Monitor diatom response to wildfire by comparing restored vs unrestored sites along the South Fork McKenzie River (SFMR), Oregon.
- Geographic context: Latitude 44.17, Longitude -122.30.
- Data type: Monitoring data with diatom genus counts and associated periphyton metrics; contextual site and environmental metadata.

## Data and Content
- Study design: Data from 23 sites across two collection periods (Feb 2022 and Sep 2021) following the Holiday Farm Fire (Sept 2020); sites include both restored and unrestored reaches.
  - February 2022: 10 sites (5 restored, 5 unrestored)
  - September 2021: 13 sites (7 restored, 6 unrestored)
- Data files:
  - SFMR_Diatom_Data: main data file with site- and sample-level metadata and diatom genus counts.
  - A separate file describing key column names for SFMR_Diatom_Data.
- Core variables:
  - Status (restored/unrestored), date.coll, year, habitat (e.g., pool, riffle, off-channel), Season, transect, site.id
  - AI (autotrophic index), mean.depth (cm), mean.velocity (m/s)
  - rock1/rock2/rock3.area.cm2 (rock surface area in cm2)
  - Diatom genera counts identified to genus level (e.g., Tabellaria, Epithemia, Fragilaria, Hannaea, Melosira, Navicula, Achnanthes, Reimeria, Cyclotella, Cymbella, Frustulia, Synedra, Rhopalodia, Eunotia, Pinnularia, Rhicosphenia, Amphora, Caloneis, Surirella, Asterionella, etc.)
  - Transect-specific geographic data: leftLon/leftLat, rightLon/rightLat (endpoints of each transect)
- Measurements and biology:
  - AI = organic mass per cm2 in periphyton divided by chlorophyll a per cm2 in periphyton
  - mean.depth (cm) and mean.velocity (m/s) for each sample
  - Diatoms counted to a minimum robust threshold (≥500 valves per sample)

## Collection Methodology
- Periphyton sampling: Scrubbed from five randomly selected cobbles per location using a toothbrush; cobbles rinsed and composited into a single sample, then split into three subsamples.
- Subsampling: One subsample preserved in 37% formalin for diatom analysis; two unpreserved subsamples analyzed for chlorophyll a (Chl a) and ash-free dry mass (AFDM).
- Diatom analysis: At least 500 diatom valves counted per sample; genera identified using standard laboratory techniques.
- Laboratory standards and references: Methods follow Baird, Eaton & Rice (2017) and Kelly et al. (1998) for diatom sampling and analysis.

## Dataset Structure and Metadata
- Main dataset: SFMR_Diatom_Data includes a mix of site-level metadata, transect details, environmental measures, and genus-level diatom counts.
- Metadata capture: Includes collection dates, year, habitat type, season, transect identifiers, site IDs, and sampling coordinates for traceability and reproducibility.
- Units and clarity: Explicit units for depth (cm) and velocity (m/s); rock area in cm2; AI as a ratio-based metric.

## Quality Assurance and Documentation
- QA/QC: Diatom sampling and counting conducted using standard procedures; minimum robust sample size of ≥500 valves per sample to ensure data reliability.
- Documentation: Dataset structure and column descriptions provided; explicit notes on treatment (restored vs unrestored) and data provenance to facilitate reuse and replication.

## Data Governance and Reuse Considerations
- Governance considerations:
  - Clear delineation of data collection periods, restoration status, and site-level metadata supports governance of dataset variants across time.
  - Comprehensive metadata and standardized measurement units aid interoperability and discovery in data portals.
- Potential reuse considerations:
  - Post-fire context and restoration status enable comparative analyses of periphyton response to wildfire and restoration efforts.
  - Genus-level diatom data allow ecological assessments while acknowledging taxonomic resolution constraints.
  - Ensure alignment of dates, transects, and site IDs when merging with other SFMR datasets or temporal analyses.

## Challenges and Opportunities for Data Stewards
- Challenges:
  - Integrating data across multiple years and sites with restoration status differences.
  - Maintaining consistent metadata quality across sites and time points; potential gaps in coordinate or transect alignment.
  - Managing a large number of diatom genera and ensuring accurate genus-level identifications.
- Opportunities:
  - Establishing a publishing mindset for reusable datasets by documenting methods, QA/QC, and provenance.
  - Facilitating data discovery through standardized metadata and clear file descriptions.
  - Supporting governance by providing traceable, high-quality data suitable for sharing to portals and networks.