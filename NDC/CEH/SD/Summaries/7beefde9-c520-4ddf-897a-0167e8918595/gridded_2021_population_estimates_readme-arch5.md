# UK gridded population at 1 km resolution for 2021

- Purpose and governance
  - A 1 km x 1 km gridded population dataset for the UK, integrating Census 2021 (Scotland: 2022) with Land Cover Map 2021 to enable spatially consistent population distribution for environmental and health analyses.
  - Published by the NERC Environmental Information Data Centre (EIDC); suitable for data governance, discovery, and reuse by organizations with large datasets.

- Data lineage and sources
  - Population inputs by Output Areas and Data Zones sourced from official statistics:
    - England & Wales: ONS small-area population estimates mid-2021 to mid-2022
    - Northern Ireland: NISRA geography data for 2021
    - Scotland: 2022 Output Area data
  - Land Cover inputs: Land Cover Map 2021 (Great Britain and Northern Ireland)
  - Geographical boundaries: OA/DZ shapefiles for England & Wales, Scotland, and Northern Ireland
  - All sources are public-facing datasets intended for GIS usage and alignment with census totals

- Experimental design and rationale
  - Goal: provide a spatially homogeneous population distribution beyond administrative boundaries to support environmental health analyses.
  - Strategy: map OA/DZ-level population to a 1 km grid using urban/suburban land-cover as a distribution proxy; preserves total census counts while reflecting land-use variability.
  - Projection and grid: British National Grid (OSGB36; EPSG 27700)

- Data processing workflow (high level)
  - Step 1: Create a national 1 x 1 km target grid (EPSG 27700).
  - Step 2: Build urban/suburban mask from LCM2021 at 10 x 10 m; project Northern Ireland data to the GB grid; create a fraction mask representing urban/suburban coverage within each OA/DZ.
  - Step 3: Spatially intersect each OA/DZ with the 1 x 1 km grid; reproject NI OA/DZs to match the target grid.
  - Step 4: For OA/DZs spanning multiple 1 km cells, distribute population to grid cells using the urban/suburban weight fractions; ensure each OA/DZ has some urban/suburban coverage.
  - Step 5: Merge OA/DZ populations with their weightings and aggregate to 1 km grid cells; reform into a raster format.
  - Step 6: Validate by comparing the raster sum to the official census totals; annotate and ensure reproducibility through documented R code.

- Quality control and validation
  - Totals checked at each step against official 2021/2022 census totals to ensure consistency.
  - Reproducibility emphasized via annotated R code; tools used include Terra and sf packages for spatial processing.
  - Final raster totals align with UK census totals by country (England, Wales, Scotland, Northern Ireland, UK overall).

- Data outputs and structure
  - Output format: GeoTIFF raster
  - Cell value: persons per square kilometer (or grid-cell population density)
  - Resolution: 1 km x 1 km across the United Kingdom
  - Total population in final product (UK): 66,941,199 for 2021

- Details of the data product and scope
  - Combines Census population data at OA/DZ level with Land Cover Map 2021 urban/suburban classes to produce a spatially homogeneous gridded population dataset.
  - Covers England, Wales, Scotland (Census 2022 data for Scotland), and Northern Ireland with consistent UK-wide methodology.

- Reproducibility, transparency, and governance notes
  - Processing implemented in R (version 4.4.1) using terra and sf packages; steps and methodology are documented within the code for transparency.
  - Northern Ireland LCM2021 data reprojected to match Great Britain grid using nearest-neighbor interpolation.
  - Urban/suburban masking approach is central to distribution logic, acknowledging that rural OA/DZs may require more reliance on non-urban areas for population distribution.
  - Dataset is designed for reuse and integration into GIS workflows, with clear linkage to official census totals to support governance and data stewardship responsibilities.

- Access, citation, and usage considerations
  - Dataset citation: Carnell, E.; Tomlinson S.J. and Reis, S. (2025). UK gridded population at 1 km resolution for 2021 based on Census 2021/2022 and Land Cover Map 2021. NERC Environmental Information Data Centre.
  - Data sources are publicly accessible; the product is intended to be discoverable, citable, and updateable as standard within data governance practices.
  - Users should be aware of the methodology’s reliance on urban/suburban land-cover proxies, which may affect small-area accuracy in rural contexts.