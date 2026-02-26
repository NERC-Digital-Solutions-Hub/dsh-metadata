# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment water content in saltmarsh and mudflat habitats

## Overview
- Dataset measuring surface sediment water content (%), derived from the top 2 mm of sediment.
- Sampling occurred in winter and summer 2013 as part of the CBESS field campaign.
- Five replicates per quadrat were collected and analyzed.
- Locations span Essex and Morecambe Bay to represent contrasting habitats and sediment types.

## Locations and habitats
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) — saltmarsh and mudflat habitats with cohesive clays.
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) — saltmarsh and mudflat habitats with sandy/coarser sediments.
- Site characteristics:
  - Saltmarsh: Essex (clay soils) vs. Morecambe Bay (sandy soils) with broader differences in inundation frequency, creek structure, and vegetation.
  - Mudflats: Essex characterized by cohesive clays, mud and silt; Morecambe by coarse, mobile sediments.

## Study design and sampling approach
- Quadrat layout: 22 randomly allocated 1x1 m quadrats per mudflat and per saltmarsh site to capture spatial heterogeneity.
- Spatial scales (A–D) used to structure sampling density:
  - A: 1 quadrat
  - B: 3 quadrats at 1–10 m apart
  - C: 6 quadrats at 10–100 m apart
  - D: 12 quadrats at 100–1000 m apart
- Quadrat placement and scale allocations determined with R (R Development Core Team 2014).
- Seasonality: Winter (W) and Summer (S) sampling; datasets reflect both seasons.

## Data collected and variables
- Primary variable: Percentage water content of surface sediment.
- Derived statistics per quadrat: 
  - Average percentage water content
  - Standard deviation (StDev) across quadrats within a scale
- Additional fields in the dataset include quadrat identifiers (Row Number, Quadrat Number), site and location descriptors, habitat type, scale, and season.

## Methods and data processing
- Field procedure: Random quadrat selection; surface 2 mm sediment sampled with a contact corer; samples flash-frozen with liquid nitrogen and stored at -80°C.
- Laboratory procedure: Samples dried to determine water content via the difference between wet and dry weights using a freeze dryer.
- Data handling: Wet and dry weights recorded; readings entered into a spreadsheet for quality control.

## Data formats and accessibility
- File format: Comma-separated values (.csv).
- Dataset fields include: Season, Location, Site, Habitat, Quadrant/Quadrat details, Scale, Percentage Water Content, StDev, andNotes on missing data.
- Some entries indicate missing data due to inaccessibility (Not Applicable/NA).

## Temporal coverage and reusability
- Temporal coverage limited to Winter and Summer 2013; no planned repeat sampling within this dataset.
- Designed for integration with other CBESS environmental data to assess environmental health and ecosystem service sustainability over time and across habitats.

## Relevance to environmental monitoring and challenges
- Demonstrates standardized data collection and reporting to enable comparisons across sites and seasons.
- Supports monitoring of coastal sediment water content as an indicator of habitat condition and potential ecosystem service implications.
- Aligns with Analysts Monitoring the Environment goals: verify and standardize data from established sources, present clear outputs (tables, maps, charts), and enable data reuse and accessibility.
- Key challenges addressed or anticipated:
  - Increasing the value of the datasets by enabling data integration with additional environmental layers (e.g., sediment type, inundation patterns, vegetation).
  - Ensuring broad access to underlying data used for final outputs to support scrutiny of environmental health and policy performance.