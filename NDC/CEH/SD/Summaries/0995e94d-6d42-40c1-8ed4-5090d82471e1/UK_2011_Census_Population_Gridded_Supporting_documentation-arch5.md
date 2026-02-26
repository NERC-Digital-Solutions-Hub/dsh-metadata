# UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015

## Aim
- Create a consistent 1 km x 1 km gridded population product for the UK by combining 2011 Census Output Areas with Land Cover Map 2015 land-use classes (Urban, Suburban) to enable spatially homogeneous population distribution analyses.
- Distinguish residential and workday populations, aligned to the British National Grid datum.

## Provenance and collection methods
- Data sources:
  - 2011 Census population data for Output Areas (OA) from the Office for National Statistics (ONS).
  - Land Cover Map 2015 (vector data) from CEH.
  - OA geography data for England & Wales, Northern Ireland, and Scotland.
- Mapping rationale:
  - Census 2011 provides population counts by OA; LCM 2015 provides land-use context to distribute population within OA polygons to a uniform 1 km grid.
- Data formats and outputs:
  - Outputs include ESRI Shapefiles, CSV summaries, and ASCII Grid rasters (1 km resolution) for residential and workday populations.

## Processing workflow (data handling and reproducibility)
- Tools used:
  - Data processing with FME Desktop 2016; visualisations in ArcGIS for Desktop 10.1.
- Stepwise processing:
  - Step 1: Aggregate Census 2011 OA populations to OA geographies; generate quality-control CSV.
  - Step 2: Extract Urban and Suburban land-use polygons from LCM 2015 (PARCEL_ID, BH, BHSUB).
  - Step 3: Clip land-use polygons to OA geographies; compute clipped areas and store in CSV for area-share calculations.
  - Step 4: Merge population data with clipped land-use parcels; distribute population to land-use classes using relative area shares within each spatial unit; perform area-weighted distribution at both OA and 1 km grid levels.
  - Step 5: Assign equal weight to all Land Use types in the final aggregation step to reflect potential density differences.
  - Step 6: Clip the resulting population to a 1 km grid (OSGB grid) and scale totals to preserve the overall UK Census 2011 total; round results and store as shapefile and ASCII raster.
- Quality assurance:
  - Visual inspection and summary statistics at each step; workflow is documented with annotated workbenches to ensure transparency and reproducibility.

## Calibration, quality control, and limitations
- Consistency checks:
  - Compare intermediate totals with official 2011 Census totals; address inconsistencies due to boundary clipping and land-use date differences.
- Calibration outcomes:
  - Final 1 km gridded population totals are scaled to match the UK Census 2011 total (63,185,612) with a scaling factor applied before rounding.
  - Reported discrepancies: overall 0.47% difference due to land-use data timing; residential vs workday totals differ by 0.107% but are scaled to the same total.
- Accuracy notes:
  - Final residential and workday totals align with Census totals within 0.0012% and 0.0005% respectively after scaling and rounding.
- Data limitations:
  - Land Cover Map 2015 may not capture residential growth that occurred after 2011, leading to potential underestimation in new residential areas.
  - Some mismatches arise from merging administrative-boundary data with land-use polygons.

## Data structure, content, and units
- Data records:
  - Each grid cell has a unique grid ID (TEXT), grid row and column (INTEGER), and population (INTEGER).
- Outputs:
  - Shapefiles and ASCII Raster grids containing residential and workday population values per 1 km cell.

## Access, citation, and reuse
- Citation:
  - Reis, S.; Liska, T.; Steinle, S.; Carnell, E.; Leaver, D.; Roberts, E.; Vieno, M.; Beck, R.; Dragosits, U. (2017). UK Gridded Population 2011 based on Census 2011 and Land Cover Map 2015. NERC Environmental Information Data Centre. https://doi.org/10.5285/0995e94d-6d42-40c18ed4-5090d82471e1
- Accessibility:
  - Data made available through the NERC Environmental Information Data Centre (EIDC) with implemented provenance and versioning for reuse.

## Governance and metadata considerations for Data Stewards
- Documentation and reproducibility:
  - Full FME-based workflow with step-by-step processing documented; enables audit trails and future re-running with updated inputs.
- Metadata and standards:
  - Clear specification of inputs, processing steps, coordinate systems (OSGB references), and output formats (Shapefile, CSV, ASCII Grid) to support discoverability and interoperability.
- Updates and maintenance:
  - Processed outputs scale to census totals; when inputs or land-cover data are updated, re-runable workflows should be maintained to ensure consistency with new census totals and updated land-cover classifications.
- Data quality governance:
  - Regular QA at each processing step; explicit calibration to census totals; transparency about limitations due to data vintage and boundary mismatches.