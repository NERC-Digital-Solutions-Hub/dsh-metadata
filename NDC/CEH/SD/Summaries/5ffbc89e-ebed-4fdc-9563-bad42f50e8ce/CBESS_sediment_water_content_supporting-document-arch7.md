# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment water content in saltmarsh and mudflat habitats

## Overview
- Measures the percentage water content of the surface sediment (top 2 mm) in saltmarsh and mudflat habitats.
- Campaign: CBESS field campaign, winter and summer 2013.
- Replication: five replicates per quadrat.
- Spatial coverage: two UK regions—Essex (east coast) and Morecambe Bay (northwest coast).
- Sites included:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)

## Locations and habitat context
- Essex and Morecambe Bay saltmarsh sites represent contrasting soil types and inundation/vegetation conditions:
  - Essex saltmarsh: predominantly clay soils.
  - Morecambe saltmarsh: sandy soils.
- Mudflat sites differ between regions:
  - Essex mudflats: cohesive clays, mud, and silt.
  - Morecambe mudflats: coarser, mobile sediments.
- Precise site coordinates provided for each location (latitude/longitude).

## Sampling design and spatial structure
- Quadrat-level sampling:
  - 22 quadrats of 1x1 m per mudflat and per saltmarsh site.
  - Quadrats allocated randomly using R to explore four spatial scales (A–D):
    - A: 1 quadrat
    - B: 3 quadrats at 1–10 m apart
    - C: 6 quadrats at 10–100 m apart
    - D: 12 quadrats at 100–1000 m apart
- Temporal coverage:
  - Winter and Summer 2013 sampling; no planned repeats.
- Data collection at each quadrat:
  - Wet and dry weights used to calculate water content.
  - Sample handling included flash-freezing with liquid nitrogen and storage at -80°C prior to freeze-drying.

## Variables and data structure
- Core variable: Percentage Water Content (per quadrat; average across quadrats within a scale).
- Supporting fields:
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM), Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A–D (sampling intensity/coverage)
  - StDev: Standard deviation of water content within a quadrat group
  - Other information: NA or Not Applicable where data are missing
- Data capture and quality:
  - Data checked by entering scale readings into spreadsheets.
  - No additional statistical treatments beyond calculating water content from wet/dry weights.

## Data formats and accessibility
- File format: Comma-separated values (.csv)
- Dataset field descriptions: include header, row number, season, location, site, habitat, quadrat number, scale, percentage water content, standard deviation, and other information.
- Metadata supports integration with GIS workflows through explicit geographic locations (lat/long) and site classifications (region, habitat, site).

## GIS and practical use
- Suitable for mapping spatial variation in sediment moisture across saltmarsh and mudflat habitats.
- Enables analysis of regional differences (Essex vs. Morecambe Bay), habitat type (saltmarsh vs. mudflat), and scale-dependent patterns due to multi-scale quadrat design.
- Provides two-season temporal snapshots (winter and summer 2013) for comparative analysis, with potential for linking to other CBESS ecological variables.
- Important considerations for GIS:
  - Coordinate system not explicitly specified; coordinates are given in degrees/minutes. Verify CRS when importing to GIS.
  - Data include multiple hierarchical qualifiers (region, site, habitat, scale) to support layered mapping and multi-criteria queries.

## Limitations and considerations
- Sampling period limited to 2013 winter and summer; no longitudinal repeats planned beyond the stated design.
- Some fields in the source text show transcription variants; verify field meanings and coding (e.g., Scale and Site identifiers) against the CSV metadata in practice.
- No additional statistical treatments reported beyond wet/dry weight calculations; further analyses (e.g., spatial statistics) would require explicit QA of coordinates and scale mappings.