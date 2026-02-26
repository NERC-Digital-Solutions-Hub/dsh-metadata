# Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)

## Overview
- Supplement to the Turf2Surf WP2 supporting documentation.
- Describes the data structure for plant physiological measurements collected in North Wales and Northwest England across 2013, 2014, and 2016.
- Data are provided in Turf2Surf_Plant_physiological_data.csv and related datasets.

## Dataset structure
- The dataset contains 96 rows.
- It includes 9 additional columns beyond the first 9 base columns.
- Missing values are indicated as NA.
- At sites 5, 7, 14, and 19, leaves were sampled in 2015 for re-analysis of foliar nitrogen and phosphorus content only.

## Shared schema across related datasets
- The following datasets share the first 9 columns:
  - Plant structural measurements (North Wales and Northwest England; 2013 and 2014)
  - Plant aboveground and belowground standing biomass (Conwy catchment; 2013 and 2014)
  - Soil carbon data (Conwy catchment; 2013 and 2014)
  - Soil physical, chemical, and biological measurements (Conwy catchment; 2013 and 2014)
  - Plant aboveground and belowground standing biomass (Conwy catchment; 2013 and 2014)

## Detailed column information (first 9 columns)
- A: Unique Site Number
- B: Habitat
- C: Habitat Description
- D: Site name
- E: Ecosystem Component (plant, soil, or roots)
  - If Plant, column F contains the plant species; otherwise NA
- F: Plant species (or NA for soil/root components)
- G: Plot number (1–4)
- H: Replicate number (used when measurements are not co-located with plots)
- I: Soil depth interval (for soil and roots)

## Additional (nine) data columns
- J: Year (measurement year)
- K: Vcmax — Maximum rate of carboxylation at 25°C (µmol m⁻² s⁻¹)
- L: Jmax — Electron transport capacity at 25°C (µmol m⁻² s⁻¹)
- M: Asat — Photosynthetic rate at saturating irradiance and 400 ppm CO₂ at 25°C (µmol m⁻² s⁻¹)
- N: Leaf mass area (LMA) — leaf mass per leaf area (g m⁻²)
- O: Foliar nitrogen content (%)
- P: Foliar phosphorus content (%)
- Q: Specific leaf area (SLA) (cm² g⁻¹)
- R: Comments (no unit)

## Data quality and interpretation notes
- NA indicates data not available or not performed for a site/component.
- The column structure supports integration with geographic and habitat data for GIS applications (e.g., linking site-level attributes to maps of habitat types, plots, and soil/biological layers).
- The dataset provides year-specific physiological measurements, enabling temporal GIS analyses across 2013, 2014, and 2016.

## Temporal and spatial scope
- Temporal coverage: measurement years 2013, 2014, 2016 (with some 2015 re-analysis for foliar N and P at select sites).
- Spatial scope: North Wales and Northwest England; site-based sampling with plot and replicate identifiers for spatially explicit mapping.

## GIS applicability and usage notes
- Data are structured to facilitate map-based visualisations of plant physiology across sites and habitats.
- First-9-column sharing across multiple related datasets enables efficient joins with habitat, site, and plot layers in GIS workflows.
- Variables such as Vcmax, Jmax, Asat, LMA, foliar N and P, SLA can be used to create thematic layers or model calibrations, aligned with habitat and soil property layers.
- When integrating, consider handling NA values and the specific sites with 2015 foliar re-analysis data.