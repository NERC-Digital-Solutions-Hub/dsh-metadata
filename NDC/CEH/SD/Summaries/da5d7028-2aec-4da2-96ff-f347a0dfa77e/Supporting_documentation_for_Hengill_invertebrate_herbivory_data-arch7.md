# Invertebrate herbivory data across a natural soil temperature gradient in Iceland from May-July 2017

## Overview
- Dataset of environmental data, vegetation cover, and community- and species-level invertebrate herbivory.
- Collected May–July 2017 across 14 experimental plots in the Hengill geothermal valley, Iceland.
- Plots span a soil temperature gradient (roughly 5–35 °C on average) within a 1 km² area, with similar soil moisture, pH, nitrate, ammonium, and phosphate.
- Aimed at understanding how soil temperature, plant phenology, and vegetation composition influence invertebrate herbivory.

## Sampling regime and study area
- 14 plots (66–210 m² each) within 1 km² area; chosen to distribute focal plant species across the temperature gradient and to maximize within-plot temperature variation.
- Focal plant species for herbivory assessments: Cardamine pratensis, Cerastium fontanum, Viola palustris.
- Species-level sampling: 30 individuals per species marked in each of 10 plots (stratified random sampling across temperature range).
- Community-level sampling: five 50 × 50 cm quadrats per plot in eight plots capturing the full temperature gradient.
- Temperature measurements: recorded at 12 cm depth at five points per community-level quadrat and near each marked individual.
- Soil moisture: measured in each community quadrat.
- Soil chemistry: five cores per quadrat for pH and nutrients (nitrate, ammonium, phosphate) using standard extraction and colorimetric methods.
- Vegetation phenology: weekly assessment of development stage for each marked plant.
- Vegetation cover: percentage cover of functional groups (bryophytes, forbs, graminoids, lichens, litter, bare ground) estimated in quadrats.
- Herbivory assessments: leaf-level and plant-level damage tracked over time; community-level assessment conducted once (mid-June); species-level assessments every two weeks from late May to early July.

## Data collection and variables (five CSV files)
- cardamine.csv and cerastium.csv (species-level data)
  - Common columns: time, date, plot
  - Additional columns: ID (unique plant), temp (soil temp at 12 cm near plant), phenology, damage (binary herbivory indicator), length, stems, leaves, leaves_damaged, pc_leaves_damaged, overall_damage, flowering, num_flowers
- viola.csv (species-level data; similar columns to the above with pc_leaves_damaged and flowering as columns 9 and 10)
- cover.csv (vegetation cover around individuals)
  - Columns: ID, species (Latin name), temp, moss, lichens, graminoids, forbs, litter, bare_ground, flowering
- herbivory.csv (community-level herbivory and quadrat context)
  - Columns: herbivory (proportion of plants with damage in quadrat), moss/lichens/graminoids/forbs/litter/bare_ground covers, temp (average soil temp in quadrat), pH, moisture, nitrate, ammonium, phosphate
- All files include the first three shared columns: time, date, plot; additional file-specific columns align to the study’s sampling scheme
- Data are linked by time-point, plot, and, where applicable, individual IDs for integration in analyses

## Spatial and temporal structure
- Spatial: 14 plots within Hengill valley; quadrats nested within plots; temperature gradient represented across plots and within-plot microhabitats.
- Temporal: multiple sampling time-points May–July 2017 (species-level surveys every two weeks; community-level survey mid-June; ongoing phenology and damage tracking throughout the period).

## Data structure and usefulness for GIS
- Data are provided as five comma-separated value files with explicit column order and descriptions.
- Plot-level coding is referenced to Warner et al. (2021), enabling cross-referencing to plot locations and gradient context.
- Suitable for GIS workflows to:
  - Map plots and quadrats along the soil temperature gradient.
  - Join time-series plant-level and quadrat-level data by ID, time, and plot.
  - Visualize spatial patterns of herbivory relative to temperature, soil moisture, and nutrient status.
  - Create derived layers (e.g., temperature surfaces, vegetation cover classes, phenology stages) and link to herbivory metrics.

## Potential GIS applications and integration notes
- Create spatial representations of:
  - Temperature gradients across plots and micro-sites (12 cm depth measurements).
  - Species distribution and phenotype across the gradient.
  - Community-level herbivory hotspots and their relation to soil chemistry and moisture.
  - Temporal changes in herbivory and phenology across time-points.
- Data integration:
  - Link by time, plot, and ID to generate comprehensive GIS-ready datasets.
  - Use plot codes and references ( Warner et al. 2021 ) to align with existing spatial layers and metadata.
- Considerations:
  - Ensure consistent handling of time formats and time-points across files.
  - Validate plot and ID mappings to avoid misalignment when joining datasets.
  - Be mindful of the measurement depth (soil temp at 12 cm) when creating spatial temperature surfaces.

## References
- Blakemore, L., Searle, P. & Daly, B. (1987). Methods for chemical analysis of soils.
- Egnér, H., Riem, H. & Domingo, W.R. (1960). Chemical methods for soil nutrient extraction.
- O'Gorman et al. (2012). Impacts of warming on aquatic communities.
- Peet, R.K. et al. (1998). Vegetation recording method.
- Robinson et al. (2018). Soil temperature effects on plant and invertebrate communities.
- Turcotte et al. (2014). Percentage leaf herbivory.
- Valdés et al. (2019). Phenotypic and genotypic responses to warming.
- Warner et al. (2021). Impacts of soil temperature, phenology, and plant community composition on invertebrate herbivory.