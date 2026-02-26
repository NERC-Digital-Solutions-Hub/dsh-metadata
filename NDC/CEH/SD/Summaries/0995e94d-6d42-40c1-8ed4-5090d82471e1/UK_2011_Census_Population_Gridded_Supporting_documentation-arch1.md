# UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015

- A 1 km × 1 km gridded population dataset for the United Kingdom, combining 2011 Census population data on Output Areas with Land Cover Map 2015 land-use classes (Urban/Suburban) to produce a consistent spatial distribution.
- Distinguishes residential and workday populations; final products are provided in ASCII grid, shapefile, and CSV formats.

## Data sources

- Population data: Office for National Statistics (Census 2011) at Output Area geography.
- Land data: Land Cover Map 2015 (vector data) for land-use classification.
- Geography extents: Output Area boundaries for England & Wales, Northern Ireland, and Scotland.
- Grid reference: British National Grid (OSGB36 datum; final clipping to OSGB63 grid).

## Experimental design / Approach

- Objective: produce a spatially homogeneous population distribution that preserves Census totals and reflects land-use-related density differences.
- Workflow aligns 2011 OA populations with 2015 land-use classes to distribute population to a uniform 1 km grid.
- Separate pipelines for residential and workday populations; results scaled to match official Census totals.

## Collection methods

- Census 2011 population data downloaded as CSV.
- Land Cover Map 2015 vector data obtained from CEH.
- OA geography extents obtained for England & Wales, Northern Ireland, and Scotland.

## Data processing workflow (Steps 1–6)

- STEP 1: Aggregate Census 2011 OA population data (CSV) onto OA geography polygons (ESRI SHAPE) to produce UK-wide OA-level population files.
- STEP 2: Extract Land Cover Map 2015 land-use types Urban and Suburban from vector data.
- STEP 3: Clip land-use polygons to OA geographies, calculate clipped polygon areas, and prepare area-share data for population distribution.
- STEP 4: Merge population with land-use areas, distribute population according to relative area shares, first within clipped OA polygons and then within 1 km grid cells.
- STEP 5: Apply equal weights to all land-use types during final distribution; assess potential density differences before final aggregation to 1 km grid.
- STEP 6: Clip the aggregated polygons to a 1 km × 1 km grid (OSGB63), compute grid-cell areas, scale to conserve total Census 2011 population, round values, and output final shapefile and ASCII grid (separate for residential and workday populations).

## Calibration and quality control

- Consistency checks against official 2011 Census totals at each processing step; acknowledges inevitable discrepancies due to geography, urban/suburban land-use overlap, and updated land-cover data from 2015.
- Final scaling factor applied to ensure the 1 km grid totals match the UK Census 2011 totals (0.47% total discrepancy; 63,185,612 national total used for scaling).
- Residual difference between residential and workday totals is minimal (0.107%); scaling applied uniformly to both.
- Quality control includes visual checks, summary statistics, and reproducible workflow documentation.

## Data structure and formats

- Outputs delivered as ASCII Grid (*.asc) files providing grid reference with residential and workday population values.
- Additional outputs: shapefile and CSV containing population data per grid cell with unique grid_ID, row, and column identifiers.
- Final product preserves total UK 2011 population within tight tolerances (0.0012% residential, 0.0005% workday).

## Data access and provenance

- Dataset citation: Reis, S.; Liska, T.; Steinle, S.; Carnell, E.; Leaver, D.; Roberts, E.; Vieno, M.; Beck, R.; Dragosits, U. (2017). UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/0995e94d-6d42-40c18ed4-5090d82471e1

## Limitations and considerations for analysts

- Land Cover Map 2015 reflects data from before the 2011 census update; new residential areas that emerged after 2015 may be underrepresented.
- Discrepancies arise from combining administrative boundary data with land-use polygons; minor inconsistencies are corrected by scaling but may affect local accuracy.
- The methodology weights all land-use types equally during final distribution, which may influence density estimates in mixed-use cells.
- Outputs are provided in both residential and workday perspectives, enabling analyses tied to different population exposure scenarios but requiring careful interpretation when comparing to other datasets.