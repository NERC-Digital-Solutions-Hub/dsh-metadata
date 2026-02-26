# Dry weight root biomass from three soil depths on salt marsh sites at Morecambe Bay and Essex.

## Overview
- Dataset measuring root biomass (kg dry weight per m^2) across three depth intervals: 0–10 cm, 10–20 cm, and 20–30 cm.
- Seasonality: Winter and Summer 2013; for Essex winter samples, an additional window (2–6 March 2013) was sampled.
- No planned repeat sampling.

## Study sites and context
- Regions and sites (six in total):
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Coordinates provided for each site.
- Habitat and soil context:
  - Saltmarsh sites representing two soil types: clay (Essex) and sandy (Morecambe Bay).
  - Essex sites generally hare-grazed; some heavily grazed by Brent geese.
  - Morecambe Bay sites heavily grazed by sheep and geese; West Plain lightly grazed.
- Broad environmental differences included inundation frequency, creek structure, and dominant vegetation.

## Sampling design and data collected
- Site-level sampling framework:
  - Each site rectangle sized approximately 400×500 m to 1000×1000 m, spanning low, mid, and high marsh zones.
  - 22 randomly allocated 1×1 m quadrats per site.
- Spatial scales:
  - Four scales (A–D) to structure quadrat sampling density or extent (details defined in the dataset).
  - Random allocation of quadrats within each site rectangle.
- Variables observed:
  - Root biomass per depth: RB_0-10, RB_10-20, RB_0-30 (the latter is the total for 0–30 cm).
  - Contextual fields include season, location, site, and habitat.

## Methods and processing
- Field sampling:
  - One large sediment core per quadrat: 16 cm diameter, 30 cm depth, including soil, roots, and above-ground vegetation.
  - Roots separated after exposure to water erosion in a recirculating flume.
- Laboratory processing:
  - Roots dried at 60°C for 72 hours and weighed.
  - Biomass values converted to kg DW m^-2 (per quadrat area).
- Location determination:
  - Quadrats randomly allocated within each site; spatial scales implemented using R (R Development Core Team, 2014).

## Data format and metadata
- File format: Comma separated values (.csv).
- Dataset fields include:
  - Season (Winter W / Summer S)
  - Location (Morecambe M / Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Saltmarsh SM / Mudflat MF)
  - Quadrat Number (1–22)
  - Scale (A–D; definitions linked to spatial extent)
  - RB_0-10, RB_10-20, RB_0-30 (kg DW m^-2)
  - Row Number, Header, and other descriptive metadata
- Data quality notes:
  - Data checked by entering scale readings into spreadsheets; outliers assessed.
  - Some data gaps noted due to loss of samples during processing.
- Total root biomass (0–30 cm) is calculated as the sum of 0–10, 10–20, and 20–30 cm depths.

## Quality assurance and accessibility
- Quality control steps included basic data entry checks and outlier review.
- Metadata and dataset field descriptions are provided to support data reuse and discoverability.
- Data are suitable for analyses comparing root biomass across depths, sites, habitats, and grazing regimes, with attention to local-scale variability and potential missing data.

## Potential for analysis
- Compare root biomass across soil types (clay vs. sandy) and regions (Essex vs. Morecambe Bay).
- Examine relationships with grazing intensity, inundation frequency, and vegetation type.
- Assess depth-dependent patterns in root biomass and overall below-ground allocation in saltmarsh ecosystems.
- Consider spatial scale effects by leveraging the A–D sampling framework to explore scale-dependent conclusions.