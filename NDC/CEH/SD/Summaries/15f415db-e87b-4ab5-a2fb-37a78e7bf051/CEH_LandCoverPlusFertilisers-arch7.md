# CEH Land Cover plus: Fertilisers 2010-2015 (England)

- Purpose and scope
  - Provides map-based, spatially explicit estimates of predicted average annual application rates of three inorganic fertilisers (N, P, K) for England from 2010–2015, with associated uncertainty, at 1 km x 1 km resolution.
  - Enables exploration of agrochemical environmental impacts for farmers and policymakers, and supports analyses such as nutrient fate, GHG emissions, eutrophication indicators, crop yield potential, and policy development.

- Data content
  - Two-band raster maps per fertiliser (N, P, K): 
    - Band 1: Predicted average annual application rate (kg/km^2)
    - Band 2: Uncertainty (%)
  - Coverage: England (1 km grid)
  - Derived from Defra BSFP data, spatially interpolated and linked to crop typology.

- Spatial and temporal coverage
  - Temporal: 2010–2015
  - Spatial: England, 1 km grid, aligned with CEH Land Cover plus: Crops map (2015–2017 average)

- Data collection and preprocessing
  - Raw data: Defra BSFP surveys (voluntary participation; approx. 3,696 georeferenced farms per year) with coordinates, crop types, soil, farm IDs.
  - Records with zero rates excluded due to data validity and spatial predictability concerns.
  - Fertiliser rates (kg/ha) converted to total application per 1 km cell by integrating crop areas.

- Analytical methods
  - Interpolation: Ordinary Kriging (OK) chosen for performance, agricultural data suitability, and ability to produce a variance surface for uncertainty estimation.
  - Supporting data: Crop typology from CEH Land Cover plus: Crops (based on Sentinel data; 2 million fields across Great Britain).
  - Process: 
    - Interpolate fertiliser application rates by crop group and fertiliser at 1 km grid cell.
    - Multiply interpolated rates by crop area to obtain total application per crop; sum across crops to obtain total fertiliser application per cell (kg/km^2).
  - ArcGIS-based workflow with default OK parameters; a variable search radius using 12 input points applied for each cell.

- Data structure and formats
  - Two-band TIFF rasters for each fertiliser (N, P, K), covering England at 1 km resolution.
  - File naming (examples): fertiliser_n_prediction_uncertainty, fertiliser_p_prediction_uncertainty, fertiliser_k_prediction_uncertainty.
  - Band definitions:
    - Band 1: Predicted average annual fertiliser application rates (kg/km^2)
    - Band 2: Uncertainty estimates associated with the predicted rates (%)
  - Uncertainty calculation: U = 2 * sqrt(V) / P × 100, where V is kriging variance and P is predicted value (95.5% confidence level).

- Quality assurance and uncertainty
  - Uncertainty surfaces produced per crop typology and fertiliser, aggregated to a single per-fertiliser surface.
  - Uncertainty expressed as a percentage of the predicted value; acknowledges potential lack of independence between crops.
  - Validation relies on kriging variance; zero-rate exclusions acknowledged as a limitation.

- Access, citation, and reuse
  - Data accessible via the Environmental Information Data Centre: https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051
  - Mandatory citation: Osório, B.; Redhead, J.W.; Jarvis, S.G.; May, L.; Pywell, R.F. (2019). CEH Land Cover plus: Fertilisers 2010-2015 (England). NERC Environmental Information Data Centre. https://doi.org/10.5285/15f415db-e87b-4ab5-a2fb-37a78e7bf051

- Applications for GIS workflows
  - Integration with other environmental layers (soil, land cover, crop types) for hotspot identification and spatial risk assessment.
  - Use in modelling nutrient fate, runoff, and pollutant transport; linking to crop growth models and yield optimization.
  - Support for policy analysis and catchment-level management to reduce pollution and improve water quality.

- Acknowledgements
  - Supported by NERC national capability funding to CEH and the ASSIST project; BSFP data acknowledged for access.