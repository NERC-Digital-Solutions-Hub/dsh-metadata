# LIDAR QUALITY CONTROL REPORT PROJECT PM_1478

- Purpose: Processing and quality assessment of LIDAR data for Devon and Cornwall as part of the South West TELLUS Project to produce DSM and DTM; automated processing with ground-truth validation.
- Stakeholders: British Antarctic Survey (data capture), Environment Agency (processing assistance), Centre for Ecology and Hydrology (ground truth references), GIS/Geomatics team.
- Key outcome: High-quality DSM/DTM products with documented processing workflow and quality metrics; data delivered in multiple formats along with the LAS point cloud.

## Overview and Scope
- Automated processing aimed at producing DSM (surface including above-ground objects) and DTM (bare earth) with minimal manual intervention.
- Ground truth comparisons conducted to evaluate height accuracy and inform data quality conclusions.
- Study area: Devon and Cornwall; timeframe and context tied to the South West TELLUS project.

## Data Processing and Standards
- Processing approach:
  - Terrascan used on 1 km x 1 km blocks with standard 1 m resolution classification macros to separate ground vs surface objects.
  - A secondary DTM retained ground points on steep slopes for coastal cliff definition.
  - ArcView integration with modified Environment Agency scripts; mosaic of overlapping 4x4 km blocks with 50 m overlap.
  - Automated no-data gap filling in the DTM; no manual editing performed (resulting in potential artifacts).
  - Automatic cliff retrieval: cliffs within 100 m of the OS mean sea level line merged back into the DTM when there was a 0.50 m difference with the secondary DTM.
  - Overlapping blocks combined into regular 5x5 km tiles; blocks feathered smoothly; exports in ESRI Binary Grid, ESRI ASCII Grid, and geo-referenced JPEG.
  - Final integration in an ArcGIS GeoDatabase to produce seamless DTM and DSM with hill-shading.
- Data formats and content:
  - 5x5 km tiles for DSM/DTM in multiple raster formats; LAS point cloud supplied with classifications (ground vs surface objects; additional classes by distance to nearest ground point).
  - Metadata-like details captured through processing steps and file naming (OS grid reference).

## Ground Control, Validation, and Provenance
- Validation approach:
  - DSM/DTM compared to 74 random GPS ground truth sites; Appendix A shows coverage; Appendix B shows ground-truth comparison.
  - Reported RMSE for average comparison: 0.095 m (within project target).
  - Validation indicates high quality despite large processing blocks and long baselines; caveats apply to vegetation-free, low-slope areas where accuracy is best characterized.
- Key findings:
  - Accuracy within ±10 cm in validated areas, well within the stated project accuracy of ±25 cm.
  - Limitations acknowledged: vegetation can obscure true ground, leading to false ground surfaces; automated filtering may leave large buildings/bridges or remove features that more intensive filtering would retain.

## Data Delivery and Access
- Delivered products:
  - DTM and DSM as 5x5 km tiles in ASCII Grid, ESRI Binary Grid, and quick-look JPEGs per Ordnance Survey tile.
  - LAS point cloud re-supplied for full data traceability.
- Documentation and usability:
  - ASCII Grid headers documented (ncols, nrows, xll/xllcorner, yll/yllcorner, cellsize, nodata_value).
  - LAS point cloud includes classifications to support downstream analysis.
  - Outputs designed for transfer between applications and integration into GIS workflows.

## Data Quality, Limitations, and Considerations for Data Stewards
- Quality assessment:
  - Ground truth RMSE within 15 cm specification; average RMSE 9.5 cm supports data quality claim.
  - Overall quality good in non-vegetated, low-slope areas; performance may degrade in areas with vegetation canopy, complex terrain, or artifacts from automated processing.
- Limitations and caveats:
  - No manual editing means possible residual artifacts (unremoved large structures, residual vegetation effects, or cliff definitions may be imperfect).
  - Leaf-on conditions during data capture limit penetration through vegetation, potentially affecting true ground elevations under canopy.
  - Cliff detection relies on merging with secondary DTM; potential edge cases near coastlines or where thresholds are exceeded.
- Governance and reproducibility:
  - Clear documentation of processing steps, block-based workflow, and merging strategy supports traceability and reproducibility.
  - Data products are delivered with explicit file formats and grid references, facilitating interoperability with common GIS tools.

## Appendices (Referenced)
- Appendix A: Ground Stations & Coverage Plot.
- Appendix B: Ground Truth Comparison results.