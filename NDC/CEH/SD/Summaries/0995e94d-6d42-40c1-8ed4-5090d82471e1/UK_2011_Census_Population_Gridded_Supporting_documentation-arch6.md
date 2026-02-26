# UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015

## Purpose and Outputs
- Creates a 1 km × 1 km gridded population dataset for the UK by combining 2011 Census Output Area (OA) population with Land Cover Map 2015 land-use classes (Urban and Suburban).
- Produces both residential and workday population distributions on a uniform grid, aligned to the British National Grid (OSGB36) with final outputs in shapefile and ASCII grid formats.
- Data designed to support spatial analyses requiring homogeneous population distribution and to enable self-service exploration and visualization.

## Data Sources
- Census 2011 OA population data (Office for National Statistics, downloaded as CSV)
- Land Cover Map 2015 vector data (CEH)
- OA geography extents for England & Wales, Northern Ireland, and Scotland

## Methodology (Experimental Design)
- Goal: distribute Census OA populations into a consistent 1 km grid by weighting land-use area shares from LCM 2015.
- Distinguishes residential and workday populations; workday definition follows UK Census: employed residents with workplaces in the area plus non-employed residents.
- Mapping uses OSGB36; equal weighting applied across Land Use types (Urban, Suburban) during distribution.
- Calibration ensures final grid totals align with official 2011 Census totals.

## Processing Workflow (Step-by-Step)
- STEP 1: Aggregate Census 2011 OA population data to OA geography, producing UK-wide population per OA (CSV and shapefile for QC).
- STEP 2: Extract Urban/Suburban land-use parcels from LCM 2015 (PARCEL_ID, BH, BHSUB) (Shapefile).
- STEP 3: Clip land-use parcels to OA geographies; compute clipped polygon areas; output area-share data (CSV and shapefile).
- STEP 4: Merge population and clipped land-use polygons; distribute population based on relative area weights within each spatial unit; perform area-weighting at multiple clipping scales.
- STEP 5: Apply equal weight across land-use types; account for potential density differences when aggregating to 1 km grid.
- STEP 6: Clip to 1 km × 1 km grid (OSGB63), compute per-cell totals; apply a scaling factor to preserve total UK Census 2011 population; round values; outputs include shapefile, ASCII raster, and CSV.

## Calibration and Quality Control
- Totals checked against official 2011 Census figures at each processing step; acknowledges minor inconsistencies due to geography clipping and LCM 2015 date.
- Overall discrepancy with total Census 2011 population is 0.47%, corrected by a final scaling factor (UK total 63,185,612) applied before rounding.
- Residential vs. workday totals differ by 0.107% but use the same scaling factor; final results align with Census totals within 0.0012% (residential) and 0.0005% (workday).
- Quality assurance includes visual checks, summary statistics, and reproducibility documentation of the FME workflow.

## Data Structure and Outputs
- Output formats: ESRI SHAPE, ESRI ASCII GRID (*.asc), and CSV.
- Grid-level data: unique grid_id, row, column, and population (INTEGER for populations; FLOAT during intermediate steps).
- Final products are 1 km grid cells covering the UK, aligned to OSGB36, with both residential and workday population counts.

## Access, Citation, and Reproducibility
- Data cited as: Reis, S.; Liska, T.; Steinle, S.; et al. (2017). UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/0995e94d-6d42-40c18ed4-5090d82471e1
- Processing workflow implemented in FME Desktop 2016; visualizations in ArcGIS for Desktop 10.1; workflow documented for transparency and reproducibility.