# Soil Core Sample Dataset Variables and Descriptions

## Overview
- A dataset of soil core samples with treatment and site metadata, supporting analysis of soil chemistry, physics, and moisture status.
- Includes field-level details (site, depth, replicate, time of sampling) and treatment information (biochar amendment, wetted treatment).
- Provides chemical and physical properties before incubation, enabling spatial and temporal comparisons via GIS visualizations.

## Data Schema at a Glance
- Identification and context
  - soilcorenumber: Unique identifier for each soil core/sample.
  - site: Field site where the sample was collected.
  - depth: Depth of the soil sample from the soil surface.
  - replicate: Replicate number for the same treatment within a site.
  - timesample: Time point at which the sample was taken.
  - biocharamendment: Whether the sample was amended with biochar (yes/no or similar indicator).
  - wettedtreatment: Whether the sample was periodically wetted to a high water content (yes/no or similar indicator).
- Chemical properties
  - pH.water: Soil pH measured in water at a 1:2.5 ratio.
  - total.C.percent: Total carbon content as a percentage.
  - total.N.percent: Total nitrogen content as a percentage.
  - CN ratio: Ratio of total carbon to total nitrogen.
  - extract.nh4-n.mgkg: Extractable ammonium (NH4+) in mg/kg.
  - extract.no3-n.mgkg: Extractable nitrate (NO3−) in mg/kg after incubation starts.
- Physical properties
  - drysoilweightg: Dry soil weight of the core in grams.
  - gravwatercontproportion.before: Gravimetric water content as a proportion before incubation.
  - bulkdensitygcm3.before: Bulk density before incubation (g/cm³).
  - particledensitygcm3: Particle density of the soil (g/cm³).
  - totalporosityproportionbefore: Total porosity before incubation, calculated as 1 - (bulk density / particle density).
  - wfpsproportionbefore: Water filled pore space before incubation (derived from gravimetric water content, bulk density, and porosity).

## Spatial and Temporal Dimensions
- Spatial: Each record tied to a specific site and depth, enabling spatial mapping and vertical stratification analyses.
- Temporal: Timesample field allows tracking changes across sampling events or incubation stages.
- Experimental context: Replicate and treatment fields support comparative GIS analyses across treatments and replicates.

## GIS Applications and Visualizations
- Map-based representation of soil chemical/physical properties by site and depth.
- 3D or cross-sectional visualizations to show vertical gradients (depth) and spatial patterns (site + replicate).
- Quick derivations in GIS (where needed) for:
  - Derived fields: CN ratio, porosity, and WFPS where appropriate.
  - Aggregations by site, treatment, or depth interval for policy or client-facing dashboards.
- Suitable for temporal comparisons across timesample, to illustrate changes over incubation or treatment periods.

## Data Quality and Preparation Notes
- Units/scales to verify for consistency:
  - pH is measured at a 1:2.5 soil-to-solution ratio.
  - Carbons and nitrogen are expressed as percentages; nutrient species are in mg/kg.
  - Densities in g/cm³; porosity and WFPS as proportions.
- Ensure consistent handling of inputs across sites to avoid misalignment of depth references or treatment labels.
- Abide by the dataset’s definitions for before-incubation measurements; interpret any “before” suffix as baseline values.

## Access and Integration Considerations
- Integrate with GIS workstreams by linking soilcorenumber to spatial coordinates (if available) and to site boundaries.
- Maintain clear provenance for biochar amendment and wetted treatment as categorical fields for filtering and visualization.
- Manage large datasets by segmenting into manageable chunks (e.g., by site or depth ranges) for performance in GIS platforms.