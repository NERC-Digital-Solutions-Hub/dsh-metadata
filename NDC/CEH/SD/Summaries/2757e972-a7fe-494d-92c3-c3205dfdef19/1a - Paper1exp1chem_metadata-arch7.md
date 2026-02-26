# Soil Core Sample Dataset Description

## Overview
- A dataset describing soil core samples with associated treatments (notably biochar amendments) and a range of chemical, physical, and moisture properties.
- Designed for map-based data visualisation and spatial analysis, enabling comparisons across treatments and sampling sites.

## Dataset fields and measurements
- soilcorenumber: Unique identifier for each soil sample/core.
- treatmentfullname: Full name of the soil treatment (biochar and wetted).
- treatmentnamenowet: Full name of the soil treatment (biochar) without the wetted component.
- shorttreatmentname: Shortened treatment identifier.
- biocharamendment: Indicates whether the sample was amended with biochar.
- temperature: Soil temperature of the sample (unit not specified; typically °C).
- pH.water: Soil pH measured in water at a 1:2.5 ratio.
- total.C.percent: Total carbon content as a percentage.
- total.N.percent: Total nitrogen content as a percentage.
- CN ratio: Carbon-to-nitrogen ratio (dimensionless).
- extract.nh4-n.mgkg: Extractable ammonium (NH4-N) in mg/kg.
- extract.no3-n.mgkg: Extractable nitrate (NO3-N) in mg/kg after incubation.
- bulkdens.after.mix.gcm3: Bulk density immediately after mixing (g/cm³).
- bulkdens.fortydays.after.mix.gcm3: Bulk density 40 days after mixing (g/cm³).
- WFPS.field.moist.proportion: Water filled pore space at field-moist conditions (dimensionless proportion), calculated from gravimetric water content, bulk density, and total porosity.
- WFPS.after.wetting.proportion: Water filled pore space immediately after wetting (dimensionless proportion).

## Treatments and data context
- Treatments reflect biochar-related interventions, including combinations with wetting ( wetted ) and separate biochar-only conditions.
- Some fields distinguish between the full treatment name and a shortened variant to support consistent categorization in GIS workflows.

## GIS applications and visualization
- Map-based visualization of soil properties by core site to identify spatial patterns associated with treatments.
- Potential analyses include comparing CN ratio, carbon/nitrogen content, pH, and nutrient availability across amended vs. non-amended sites.
- Can be integrated with site coordinates to produce choropleth or point maps, and to support spatial modeling of treatment effects on soil chemistry and moisture dynamics.

## Data quality, standards, and challenges
- Units are specified for most chemical and physical properties (e.g., mg/kg, g/cm³, percent, dimensionless), but explicit unit confirmation for temperature and any porosity variables may be needed.
- Consistency in treatment naming (treatmentfullname vs treatmentnamenowet vs shorttreatmentname) is important for reliable GIS categorization.
- Data may originate from multiple sources or resolutions, requiring standardization before integration with other spatial datasets.
- Common GIS challenges include handling missing values, aligning sampling locations, and packaging large datasets into manageable chunks for visualization.

## Recommendations for GIS integration
- Validate and harmonize treatment names to ensure consistent category mappings.
- Attach or verify spatial coordinates for each soilcorenumber to enable mapping; store coordinates in a compatible CRS.
- Confirm units for all fields (especially temperature) and apply uniform units across the dataset.
- Abstract or compute derived variables as needed (e.g., porosity if total porosity is available) for WFPS calculations.
- Implement metadata documenting data provenance, collection methods, and processing steps to support reproducibility.
- Consider creating separate layers or attributes for field-moist vs. post-wetting conditions to facilitate dynamic visualizations.