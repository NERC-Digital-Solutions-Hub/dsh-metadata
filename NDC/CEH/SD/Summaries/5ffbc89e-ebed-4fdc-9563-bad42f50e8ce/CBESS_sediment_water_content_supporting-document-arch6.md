# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment water content in saltmarsh and mudflat habitats

## Overview
- Dataset measuring percentage water content in the surface sediment (top 2 mm).
- Based on CBESS field campaigns conducted in winter and summer 2013.
- Collected by Jack Maunder.
- Five replicates per 1x1 m quadrat across two habitat types (saltmarsh and mudflat).

## Locations and habitats
- Essex sites (saltmarsh and mudflat):
  - Abbotts Hall (AH): 51°47′N, 0°52′E
  - Fingringhoe Wick (FW): 51°49′N, 0°58′E
  - Tillingham Marshes (TM): 51°41′N, 0°56′E
- Morecambe Bay sites (saltmarsh and mudflat):
  - Cartmel Sands (CS): 54°10′N, 3°00′W
  - Warton Sands (WS): 54°08′N, 2°48′W
  - West Plain (WP): 54°09′N, 2°58′W
- Habitat contrasts:
  - Saltmarsh sites include contrasting soil types (Essex clay vs. Morecambe sandy soils) and differing inundation, creek structure, and vegetation.
  - Mudflat sites differ by sediment type (Essex cohesive clays; Morecambe coarse, mobile sediments).

## Sampling design and procedures
- Sampling periods: Winter and Summer 2013; no repeat sampling planned.
- Quadrat layout: 22 randomly allocated 1x1 m quadrats per site, spanning four spatial scales:
  - A: 1 quadrat only
  - B: 3 quadrats at 1–10 m apart
  - C: 6 quadrats at 10–100 m apart
  - D: 12 quadrats at 100–1000 m apart (site maximum)
- Sampling method:
  - Surface 2 mm sediment sampled with a contact corer.
  - Samples flash-frozen in liquid nitrogen and stored below -80°C.
  - Wet and dry weights measured after drying (to calculate water content).
  - Quadrats selected randomly using R (2014).
- Replication: Five replicates per quadrat.

## Data collection, formats, and structure
- File format: Comma separated values (.csv).
- Key fields per observation:
  - Row Number: numeric order
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe – CS, WS, WP; Essex – AH, FW, TM
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100–1000 m)
  - Percentage Water Content: average value for the quadrat
  - StDev: standard deviation of water content within quadrat
  - Other information: NA indicates missing data due to inaccessible quadrat; Not Applicable otherwise
- Dataset field descriptions mirror the above structure.
- Header/Description alignment consistent with the dataset’s metadata.

## Quality, context, and usage notes
- Data quality checks involve recording readings into spreadsheets; no explicit mention of additional QC beyond this.
- Designed to enable cross-site and cross-habitat comparisons of surface sediment water content, supporting analyses of coastal biodiversity and ecosystem services.
- Provides a structured, self-contained record suitable for re-use and meta-analysis, with explicit spatial scale and seasonal context.