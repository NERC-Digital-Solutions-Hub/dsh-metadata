# Supporting documentation

## Overview
- Dataset of hemispherical canopy photographs for estimating leaf area index (LAI) at plot level.
- Context: Nordeste project in northeast Brazil (Caatinga biome), a dry region with irregular rainfall and droughts; aims to address neglected biodiversity and ecosystem-function research and to understand plant, soil, and climate relationships.
- LAI estimation via indirect canopy transmittance analysis from hemispherical photos; photos processed to obtain plot-level LAI values.

## Data content and scope
- Sampling design: two sets of plots/sites
  - 12 plots (sites) corresponding to Fig. 1A, each with about 36 photos.
  - 14 plots (sites) corresponding to Fig. 1B, each with about 50 photos.
- Total data: 1132 photos totaling approximately 2607.8 MB (all in JPG format).
- Location and plot identifiers: multiple sites across Brazil (e.g., states PI, PB, MG, BA) with unique codes (e.g., BTI_01, CGR_01, CJU_01, etc.) and associated coordinates.
- Photo metadata: includes plot name, coordinates (latitude/longitude), number of photos per site, file size, and date.
- Temporal span: photos taken between March 2017 and August 2019; some MOR plots have two dates (2017 and 2018) but there are date labeling inconsistencies (e.g., MOR photos: two dates, but JPGs mislabeled as 2017).

## Methods and data collection
- Equipment: Nikon D100 camera with a Sigma 4.5 mm F2.8 fisheye lens.
- Sampling protocol: under overcast conditions
  - In intersections of four subplots: one photo per intersection (for the Nordeste plots) resulting in 36 photos per plot for 12 plots.
  - For other sites: one photo at the center of each subplot.
- Field setup: photos taken with the camera top facing north, at approximately 1 meter height.
- Scope of each photo: designed to capture canopy structure representative of the whole plot; depending on vegetation height, imagery may include canopies up to 20 meters away from the camera.
- LAI estimation: derived indirectly from canopy transmittance analyses of hemispherical images, yielding a representative plot-level LAI rather than subplot-level values.

## Data quality, limitations, and caveats
- Data quality considerations
  - Some photos suffered trigger failures or were rejected due to rapid changes in sky conditions.
  - Variation in sampling coverage: some plots had fewer than the maximum planned photos due to camera issues or weather.
  - Processing considerations: LAI represents the whole-plot value and may be influenced by vegetation height and canopy structure within the image radius.
- Temporal labeling issues
  - MOR plots show two dates (2017 and 2018), but JPEG date metadata can be incorrect, with some 2017 dates mislabeled.
- Scale and standardization challenges
  - The dataset is designed for plot-level LAI, not subplot-specific values; cross-plot comparisons require consistent processing and careful interpretation of canopy cover and distance from the camera.
- Data management notes
  - Emphasis on tracking data sources and providing metadata to support discoverability and reuse.

## Contextual relevance and potential analyses
- Enables analyses of LAI variation across Caatinga plots in relation to:
  - Soil properties, climate factors, and drought dynamics.
  - Biomass, phenology, carbon allocation and storage, biodiversity, and ecosystem functioning.
  - Remote sensing and ecological-modeling studies linking ground-based LAI with larger-scale vegetation dynamics.
- Data provenance and metadata structure support reproducibility and integration with other datasets in thematic biodiversity and ecosystem-function research.

## Practical considerations for analysts
- When using the dataset, account for:
  - Possible date mislabeling in MOR plots and ensure date validation where temporal analyses are sensitive.
  - Plot-level nature of LAI estimates; be cautious about extrapolating to subplots.
  - The potential need for harmonizing plot coordinates and ensuring consistent spatial references across plots for cross-site comparisons.