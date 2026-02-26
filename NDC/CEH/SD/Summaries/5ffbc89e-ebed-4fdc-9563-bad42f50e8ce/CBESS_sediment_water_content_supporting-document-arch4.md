# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment water content in saltmarsh and mudflat habitats

## Overview
- Measures percentage water content in the surface sediment (top 2 mm) of saltmarsh and mudflat habitats.
- Timeframe: winter and summer 2013; no planned repeat sampling.
- Replication: five replicates per 1x1 m quadrat; 22 quadrats randomly allocated to each mudflat and saltmarsh site.
- Principal staff: Jack Maunder.
- Regions and sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) representing clay soils; Morecambe Bay (Cartmel Sands, Warton Sands, West Plain) representing sandy soils; sites chosen to capture contrasting sediment types and inundation/vegetation differences.

## Study design and scope
- Comparisons built around contrasting habitats and soil types (Essex vs Morecambe Bay; clay vs sandy soils), with saltmarsh versus mudflat habitats.
- Two broad coastal regions with differing inundation regimes, creek structures, and dominant vegetation to explore variability in sediment water content.
- Part of the CBESS field campaign; data captured in winter and summer 2013; no subsequent resampling planned.

## Location, habitats and site details
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) – represented as mudflat and saltmarsh with cohesive clays/mud/silt.
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) – saltmarsh with sandy sediments; mudflat sediments are coarser/mobile.
- Habitat categories: Mudflat (MF) and Saltmarsh (SM) at each site.

## Sampling design and procedures
- Quadrat allocation: 22 quadrats per mudflat and per saltmarsh site, across four spatial scales:
  - A: 1 quadrat (single)
  - B: 3 quadrats spaced 1–10 m apart
  - C: 6 quadrats spaced 10–100 m apart
  - D: 12 quadrats spaced 100–1000 m apart
- Quadrat locations determined randomly using R (R Development Core Team 2014).
- Sample collection: surface 2 mm sediment sampled with a contact corer; samples flash-frozen with liquid nitrogen and stored below -80°C.
- Sample processing: freeze-dried (Edwards EF4 Modulyo); water content calculated from wet and dry weights.
- Data entry and checks: measurements recorded in spreadsheets; QA included basic data entry checks.

## Variables and data structure
- Primary variable: Percentage water content (average per quadrat; with accompanying standard deviation).
- Quadrats and scales: Quadrat Number; Scale (A–D with corresponding deployment patterns).
- Seasons: Winter (W) and Summer (S).
- Locations: Morecambe (M) and Essex (E) with specific sites listed (AH, FW, TM; CS, WS, WP).
- Site and habitat descriptors: Site name; Habitat (Mudflat MF or Saltmarsh SM).
- Data fields: Include Header, Row Number, Season, Location, Site, Habitat, Quadrat Number, Scale, Percentage Water Content, StDev, Other Information.
- Data formats: CSV files for dataset delivery.
- Data completeness: Some fields may be Not Applicable (NA) or missing where sampling quadrats were inaccessible.

## Data quality, metadata and governance
- Data quality controls: Wet/dry weight measurements used to compute water content; readings entered into spreadsheets.
- Metadata richness: Detailed site descriptions, habitat types, soil contrasts, and sampling scales to support discoverability and reusability.
- Potential data issues: Some repetition and formatting artifacts in the dataset description; NA entries indicating inaccessible quadrats; no explicit statistical treatment beyond basic calculations (no advanced modeling described).

## Access, reuse and stewardship
- File formats: Comma-separated values (.csv).
- Reusability considerations: Well-documented sampling design, site-level and habitat-level context, and per-quadrat measurements with variability (StDev).
- Temporal coverage: 2013 winter and summer only; no repeated measurements planned.
- Stewardship notes: Dataset tied to CBESS field campaigns; clear association with coastal sediment water content across contrasting habitats and soils.