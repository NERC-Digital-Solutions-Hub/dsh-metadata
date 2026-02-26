# UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015

## Aim and scope
- Creates a 1 km x 1 km gridded population product for the UK by combining 2011 Census population data (at Output Area level) with Land Cover Map 2015 land-use classifications (Urban and Suburban).
- Produces both residential and workday population grids, aligned to the British National Grid (OSGB36/OSGB63) and delivered as ASCII grid files (and shapefiles for some steps).
- Designed to provide a spatially homogeneous population distribution for analyses requiring consistent grid cells rather than irregular administrative units.

## Data sources
- Census 2011 population data for Output Areas (England, Wales, Northern Ireland, Scotland) supplied by the Office for National Statistics (ONS).
- Land Cover Map 2015 (vector) data from CEH.
- Output Area geography extents for England & Wales, Northern Ireland, and Scotland.
- Final format includes unique grid reference ID, grid row/column, and population values.

## Data processing workflow
- Step 1: Aggregate Census 2011 population data from Output Areas to OA geography shapefiles; generate CSV for quality control.
- Step 2: Extract Urban and Suburban land-use classes from Land Cover Map 2015 (vector data).
- Step 3: Clip land-use polygons to Output Area geographies, calculate area shares for subsequent population distribution.
- Step 4: Merge clipped land-use polygons with population data; distribute population within each OA by relative area shares across land-use classes, propagating to 1 km grid cells.
- Step 5: Apply equal weighting across land-use types; assess potential density differences; proceed to 1 km grid aggregation.
- Step 6: Clip the aggregated polygons to a 1 km grid (British National Grid). Calculate grid cell areas, assign populations, scale to conserve total UK Census 2011 population, round values, and output final shapefile, ASCII raster, and CSV.

## Calibration, consistency, and limitations
- Total population is checked against official 2011 census totals at each processing step; discrepancies arise from boundary clipping and land-use data dating (LCM 2015 vs. 2011 census).
- Overall discrepancy with Census totals is 0.47%; a final scaling factor is computed as the ratio of official total to produced total UK population and applied before rounding.
- Residential vs. workday totals differ by 0.107%; the same scaling applied to both maintains overall consistency.
- Resulting dataset matches UK Census 2011 totals within 0.0012% (residential) and 0.0005% (workday).

## Output and data structure
- Outputs include:
  - ASCII Grid (.asc) for residential and workday populations.
  - Shapefile and CSV formats for accompanying data.
  - Each record contains a unique grid_ID (TEXT), grid row (INTEGER), grid column (INTEGER), and population (INTEGER).
- Processing workflow is documented and reproducible; visual QC and summary statistics performed at each step.

## Quality control and reproducibility
- Visual inspections and statistical summaries conducted after each processing step.
- FME workflow used (with ARCGIS for desktop visuals); workflows are annotated to ensure transparency and reproducibility.
- Calibration notes acknowledge data-age differences and include documented scaling to maintain consistency with census totals.

## Accessibility and citation
- Dataset cited as: Reis, S.; Liska, T.; Steinle, S.; Carnell, E.; Leaver, D.; Roberts, E.; Vieno, M.; Beck, R.; Dragosits, U. (2017). UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/0995e94d-6d42-40c18ed4-5090d82471e1

## Relevance for data leadership and data systems
- Demonstrates a cohesive data system approach:
  - Integrates official census data with land-use information to create a consistent, scalable grid product.
  - Includes data lineage, multi-stage processing, and rigorous quality checks to ensure reliability.
  - Addresses data accessibility and discoverability via standardized formats (ASCII grids, shapefiles, CSVs) and clear metadata.
  - Provides a method to maintain alignment with authoritative totals through calibration and scaling, ensuring trust and applicability for policy and analytical work.