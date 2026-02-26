# UK gridded population at 1 km resolution for 2021

- Purpose and scope
  - Creates a spatially homogeneous population distribution product at 1 km x 1 km resolution for the UK, suitable for environmental health monitoring and policy evaluation.
  - Combines 2021 UK Census population data (2022 for Scotland) at Output Area (OA) or Data Zone (DZ) level with Land Cover Map 2021 land-use classes (urban/suburban) to distribute population within a consistent 1 km grid on the British National Grid (OSGB36).

- Data sources
  - Residential population estimates by OA/DZ:
    - England & Wales: mid-2021/mid-2022 small-area population estimates
    - Northern Ireland: geographical database for 2021
    - Scotland: 2022 OA data
  - Land Cover Map 2021 (LCM2021) for Great Britain and Northern Ireland (25 m resolution)
  - Geographic boundaries for OA/DZ:
    - England & Wales OA boundaries
    - Scotland OA boundaries
    - Northern Ireland Data Zones

- Experimental design
  - Purpose-driven combination of OA/DZ population estimates with urban/suburban land-cover mask to improve spatial allocation within a 1 km grid.
  - Maintains population totals from official Census data while achieving finer spatial resolution for analysis of environmental determinants.

- Processing workflow (six key steps)
  - Step 1: Create a 1 × 1 km target grid across the UK in OSGB36 (EPSG 27700).
  - Step 2: Download LCM2021 at 10 × 10 m resolution and generate an urban/suburban mask to indicate residential areas.
  - Step 3: Spatially intersect OA/DZ boundaries with the 1 km grid; reproject Northern Ireland OA/DZs to the target grid as needed.
  - Step 4: For OA/DZs spanning multiple 1 km cells, intersect with the 10 m urban/suburban mask, aggregate within the 1 km grid, and compute weighting fractions (urban/suburban coverage) per OA/DZ.
  - Step 5: Distribute OA/DZ populations to 1 km grid cells using the computed weightings, then aggregate to produce final per-cell population counts.
  - Step 6: Validate by comparing the sum of the raster to official Census totals to ensure consistency.

- Quality control and reproducibility
  - Totals checked at each processing step to ensure consistency with official 2021/2022 Census totals.
  - All processing implemented in R (v4.4.1) using terra and sf packages; code is annotated for transparency and reproducibility.

- Data structure and outputs
  - Output format: GeoTIFF (.tif) where each cell value represents population per square kilometer (persons per km²).
  - Final totals (UK): England 56,490,284; Wales 3,107,463; Scotland 5,440,284; Northern Ireland 1,903,168; UK total 66,941,199 for 2021.

- Description and applicability
  - The dataset provides a 1 km gridded representation of UK population aligned with Census totals, designed to support analyses of environmental health determinants, spatial variability, and policy evaluation.
  - Based on OSGB36 and integrates national census boundaries with land-cover-derived urban/suburban constraints to distribute populations within high-density vs. rural areas.

- Considerations for monitoring frameworks
  - Enables consistent, openly traceable population inputs for environmental health monitoring and policy decision-making.
  - Highlights data governance and data sharing considerations (transparent methodology, QA steps, and reproducible pipeline) relevant to monitoring work.
  - Addresses typical challenges in monitoring data: data availability and quality, metadata clarity, cross-jurisdictional integration, and clear communication of complex spatial outputs.