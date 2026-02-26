# Beech tree ring data from hot and dry European distribution edges, 2019

## Overview
- Purpose: Use the relationship between European Beech tree growth and environmental factors, including climate, to monitor and forecast drought-related declines in forest growth across Europe.
- Focus: Inter-annual growth measured via dendroecology (ring width).

## Data Collection and Sampling
- Sites: 12 European Beech sites across Bulgaria, Albania, Kosovo, and Spain.
- Timing: Sampling conducted in late 2019.
- Rationale: New sites lie at lower elevations to better represent hot and dry climatic conditions at the distribution edges.
- Metadata: A site_meta.csv file contains metadata for the 12 sites, including latitude, longitude, elevation, and the nearest town or village.

## Sampling Details per Site
- Trees: At least 15 standard canopy-level trees per site; two cores collected per tree.
- Processing: Cores air-dried in a shaded, ventilated space; mounted on carriers; sanded through progressively finer grits (80, 120, 300, 600, 1200).
- Imaging: Cores scanned to 2400 PPI images for CDendro measurements with 0.01 mm precision.
- Validation: Cross-dating performed virtually and statistically; COFECH used to control cross-dating quality.

## Data Files and Structure
- Files: 12 measurement files, named by site ID, containing ring width measurements for each core by year.
- Units and resolution: Measurements in millimeters (mm) with a resolution of 0.01 mm.
- Layout: First column is the year; subsequent columns contain ring width measurements for each core.
- Core identifiers: Tree cores labeled with a combination of site ID and tree ID; two cores per tree labeled with 'a' and 'b'.
- Missing data: 'NA' indicates no value for a given year.

## Metadata and Documentation
- Site metadata (site_meta.csv) includes location and site-specific information to facilitate discovery and provenance tracking.
- Data adhere to standard dendroecology practices (dendrochronology measurements, cross-dating quality control).

## Processing, Quality Control, and Provenance
- Processing workflow: Standard dendrology procedures applied to prepare cores; imaging and digital measurement for precise ring width data.
- Quality control: Cross-dating quality verified using COFECH software.
- Provenance: Data originate from multiple field sites with explicit site and tree-level identifiers, enabling traceability from measurement to site.

## Data Access, Sharing, and Usage
- Data components: 12 site-specific measurement files and a site_meta.csv providing contextual metadata.
- Potential uses: Climate-growth relationship analyses, drought monitoring and forecasting, regional synthesis of beech growth under hot/dry edge conditions.
- Sharing considerations: Clear labeling of site IDs, tree IDs, and core labels supports interoperability and reuse across datasets and platforms.

## Governance and Stewardship Considerations
- Data governance alignment: Metadata completeness, standardized measurement units and resolutions, and explicit provenance support data governance and discoverability.
- Maintenance needs: Documentation of processing steps, updates to site metadata as needed, and ongoing alignment with EBTRN-related datasets to address climatic gaps.

## Challenges and Considerations for Data Stewards
- Ensuring consistent metadata across sites (locations, elevations, and nearest settlements).
- Maintaining consistent data formats and units across all site files.
- Managing potential data gaps (NA values) and ensuring transparent data quality notes accompany releases.
- Facilitating future updates to include additional sites or extended time series while preserving interoperability.