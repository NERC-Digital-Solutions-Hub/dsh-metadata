# Soil Core Sample Dataset

## Overview
- A structured dataset of soil core measurements intended for map-based visualizations and spatial analyses.
- Captures sample-level chemical, physical, and treatment-related properties across field sites.

## Key fields (schema at-a-glance)
- soilcorenumber: Unique identifier for each soil core sample.
- site: Field site name where the sample is located (requires join to a spatial layer for mapping).
- biocharamendment: Indicates whether the sample is un-amended or amended with biochar.
- depth: Depth of the soil sample from the soil surface (unit not specified).
- treatmentfullname: Full name of the soil treatment (e.g., biochar and wetted).
- dayfromstart: Day count from the start of measurements.
- date: Date of the soil gas flux analysis.
- pH.water: pH of the soil in water at a 1:2.5 ratio.
- total.C.percent: Total carbon content as a percentage.
- total.N.percent: Total nitrogen content as a percentage.
- CN ratio: Carbon-to-nitrogen ratio.
- extract.nh4-n.mgkg: Extractable ammonium (mg/kg).
- extract.no3-n.mgkg: Extractable nitrate after incubation (mg/kg).
- drysoilweightg: Dry soil weight of the core (grams).
- gravwatercontproportion: Gravimetric water content (proportion).
- bulkdensitygcm3: Soil bulk density (g/cm3).
- bulkdensitygcm3SE: Standard error of the bulk density (g/cm3).

## Spatial considerations for GIS
- Location context: Each sample is tied to a site; to map, join site identifiers to a spatial layer with coordinates.
- Potential for 3D visualization: depth and date/day from start enable depth-based and temporal analyses.
- Visualization options: color/size encodings by pH, total C, bulk density, CN ratio, or nutrient extracts; overlay biochar treatment and dayfromstart.

## Data quality, preparation and standards
- Units: Ensure consistent units across all records (e.g., depth units, mg/kg, g/cm3).
- Missing data: Identify and address gaps in key fields (e.g., depth, date, pH).
- Date format: Normalize date field for temporal analyses.
- Consistency: Align treatment names with a controlled vocabulary; verify integrity of soilcorenumber as a unique key.
- Data integration: Prepare to merge with external spatial datasets (e.g., site polygons, elevation) for richer GIS context.

## Visualization and analysis ideas
- Spatial maps: create per-site maps of pH.water, total.C.percent, total.N.percent, CN ratio, and bulk density.
- Biochar effects: compare samples with and without biochar amendment across sites and depths.
- Depth profiles: visualize how properties vary with depth within samples; aggregate by site or treatment.
- Temporal trends: analyze changes over dayfromstart or date to assess incubation effects on nutrient concentrations.
- Multivariate visuals: combine multiple properties (e.g., pH, C, N) into composite maps or faceted views.

## Data governance and integration notes
- Metadata: Maintain clear field definitions and units in metadata to support end-user interpretation.
- Provenance: Track data source, collection methods, and any transformations applied during cleaning or integration.
- Accessibility: Provide consistent access to the dataset alongside spatial layers to enable GIS workflows.