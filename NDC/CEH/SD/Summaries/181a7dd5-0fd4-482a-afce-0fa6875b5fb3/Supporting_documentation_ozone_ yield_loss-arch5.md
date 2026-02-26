# Modelled average percentage yield loss due to ozone damage for four global staple crops (2010-2012)

## Overview
- Global dataset estimating average yield loss (percent) due to ozone for maize, rice, soybean, and wheat during 2010–2012.
- Based on the EMEP MSC-W chemical transport model output of ozone uptake (POD3IAM) and dose–response relationships.
- Outputs are four 1° by 1° GIS shapefiles (one per crop), enabling spatial analysis of ozone-related yield impacts at a global scale.
- Data suitable for integration into data portals and for informing governance around data discovery, sharing, and reuse.

## Data collection and generation (methodology)
- Grid construction and input data
  - Created a 1° by 1° grid; used FAO GAEZ crop production data (year 2000) at 0.0833° resolution, separated irrigated vs non-irrigated production.
  - For each grid cell, total production was summed; 2010–2012 average production estimated using a conversion factor from FAO national data (based on 1999–2001 vs 2010–2012 differences).
  - Only grid cells with >500 tonnes production included; cells classified as irrigated if >75% of production was irrigated.
  - Each grid cell assigned hemisphere (North/South) and climate zone using the ES DAC/JRC climate zone layer.
- Growing period and classification
  - For each hemisphere/climate zone, defined a 90-day growing period per crop using USDA/FAO-derived schedules (Table 1 in supplementary information).
- Ozone exposure and yield-loss calculation
  - Wheat-based dose-response: used POD3IAM (phytotoxic ozone dose above 3 nmol m−2 s−1) with a reference POD3IAM = 0.1 mmol m−2 to represent pre-industrial levels.
  - Yield loss equation for wheat: Percent Yield Loss = (POD3IAM − 0.1) × 0.64.
  - For maize, rice, and soybean: applied the wheat-based yield loss, then scaled by each crop’s relative ozone sensitivity (ratio of their M7 slope to the wheat M7 slope).
  - M7 (7-hour mean ozone, ppb) response functions used to derive crop-specific sensitivities (slopes provided in study figures).
- Final data assembly
  - For each grid cell, calculated crop-specific yield loss and added to the corresponding 1° grid.
  - Stored results as GIS shapefiles, one per crop.

## Data structure and format
- Four yield-loss GIS shapefiles (one for each crop: maize, rice, soybean, wheat).
- Each shapefile is gridded at 1° by 1° resolution with five attribute columns:
  - ID: unique grid cell identifier
  - Zone: climate zone for the grid cell
  - Long_Lat: center coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South (for Cool temperate)
  - Yield loss: average percentage yield loss (2010–2012) per grid cell
- Climate/hemisphere classifications and production thresholds used to filter grid cells as described above.

## Quality assurance and validation
- Model validation (EMEP MSC-W) described in Mills et al. 2018b; comparison against Global Atmosphere Watch (GAW) data showed good spatial/temporal alignment.
- Key validation metrics:
  - Dmax and M7 against GAW observations for 2012: r2 values 0.88–0.93 with low scatter.
  - Stomatal uptake proxy (AET/PET vs. POD3IAM/M7) showed a strong relationship (r2 ≈ 0.63).
- Quality notes:
  - Global-scale application uses a wheat-based flux–response as a proxy for other crops due to limited crop-specific flux data.
  - Acknowledges uncertainties, especially for maize (limited cultivar data) and for regions with multiple or non-standard growing seasons.
  - Recommends a species-specific flux approach when new experimental data become available.

## Limitations and considerations for data governance
- Cross-crop flux relationships are not crop-specific for maize, rice, and soybean; results rely on relative sensitivity to wheat (potentially impacting accuracy in some regions or climates).
- Data reflect the most important growing period per crop per climate/hemisphere; multi-season regions may not be fully captured.
- Uncertainties are discussed in detail in supplementary materials (T1) of Mills et al. 2018a; users should consult these for caveats and methodological nuances.
- Only publicly described inputs and methodologies are provided; ongoing updates or refinements would require access to updated experimental data and revalidation.

## Provenance, reuse, and data stewardship
- Data products rely on:
  - EMEP MSC-W chemical transport model (version 4.16)
  - CLRTAP modeling framework and dose–response methodology
  - FAO GAEZ crop production data
  - ES DAC/JRC climate zone raster
  - GAW observational datasets for validation
- References for methodological details and model validation:
  - Mills et al. (2018a) Global Change Biology: Closing the global ozone yield gap
  - Mills et al. (2018b) Global Change Biology: Ozone pollution and global wheat production
- Practical guidance for data stewards:
  - Maintain metadata documenting input data sources, processing steps, climate-zone mappings, and the 90-day growing period definitions.
  - Clearly disclose assumptions (e.g., wheat-based flux proxy for other crops) and known limitations.
  - Ensure data is stored with versioning, and made accessible via appropriate geomarked portals; provide per-crop shapefiles to support discovery and reuse.
  - Note the potential need for updates as species-specific flux data become available.

## References and related documentation
- Mills, G., et al. (2018a). Closing the global ozone yield gap: Quantification and co-benefits for multi-stress tolerance. Global Change Biology, 24, 4869–4893. doi:10.1111/gcb.14381
- Mills, G., et al. (2018b). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology, 24, 3560–3574. doi:10.1111/gcb.14157
- Supplementary Information (T1) for evaluation of the approach used for spatial analysis of multiple stresses on crop yield.