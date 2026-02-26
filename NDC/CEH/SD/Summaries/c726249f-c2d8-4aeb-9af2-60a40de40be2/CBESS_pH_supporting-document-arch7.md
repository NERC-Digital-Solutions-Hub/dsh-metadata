# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil pH on salt marsh sites at Morecambe Bay and Essex

## Overview
- A dataset of soil pH measurements from saltmarsh sites in Essex and Morecambe Bay, collected as part of CBESS.
- pH measured from 10 g soil sampled from the top 5 cm within 1 m x 1 m quadrats.

## Spatial coverage and sampling design
- Locations and sites
  - Essex (E): Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay (M): Cartmel Sands (CS), Warton Sands (WS)
  - Additional site reference: West Plain (WP) within Morecambe region
- Coordinates
  - Essex: AH 51°47'N, 0°52'E; FW 51°49'N, 0°58'E; TM 51°41'N, 0°56'E
  - Morecambe Bay: CS 54°10'N, 3°00'W; WS 54°08'N, 2°48'W
- Habitat types
  - Mudflat (MF)
  - Saltmarsh (SM)
- Grazing and vegetation context ( descriptively noted for site contrasts)
  - Essex: hare-grazed; AH and FW heavily grazed by Brent geese
  - Morecambe Bay: intensive sheep grazing; pink-footed geese grazed in winter; West Plain lightly grazed
- Quadrat structure and sampling scale
  - Quadrat Number: 1 to 22 per sampling unit
  - Scale categories for spatial resolution: A=1 m, B=1–10 m, C=10–100 m, D=100 m to upper limit

## Measurements and methods
- Variable measured: pH
- Sampling and lab procedure
  - Soil: 10 g fresh mass
  - Dilution: 25 ml deionised water, 1:2.5 dilution
  - Mixing: shaken ~30 minutes
  - Measurement: pH with Jenway 4320 pH/electrical conductivity probe
  - pH values adjusted for ambient temperature
- Monitoring period
  - General field campaign: Winter and Summer 2013
  - Essex winter samples collected during an additional window: 2–6 March 2013
- Calibration and quality
  - Calibration procedures: None specified
  - Data checking procedures (quality control): Mentioned, but details not provided

## Data structure and access
- Data format: Excel workbook
- Dataset fields
  - Row Number: numeric, original input order
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe CS, WS, WP; Essex AH, FW, TM
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A=1 m; B=1–10 m; C=10–100 m; D=100 m to upper limit
  - pH: numeric, pH value
  - pH adjusted for ambient temperature

## Temporal coverage
- Winter and Summer 2013 sampling campaigns
- Essex winter samples collected 2–6 March 2013

## Considerations for GIS use
- Spatially explicit pH data across multiple saltmarsh sites and quadrats, suitable for:
  - Creating pH maps by site, habitat, season, or grazing context
  - Integrating with other GIS layers (inundation frequency, vegetation, management)
  - Analyzing spatial patterns at multiple scales via the scale codes (A–D)
- Data integration notes
  - Site coordinates enable mapping at point level; quadrat-level data supports fine-grained mapping within sites
  - Field methodology and lack of explicit calibration details should be considered when assessing measurement uncertainty

## Summary of limitations
- Calibration procedures are not described
- Quality control and data checking processes are referenced but not detailed
- Some contextual variables (e.g., grazing regime specifics, inundation data) are described qualitatively rather than quantitatively in this metadata

## Potential outputs for GIS specialists
- pH choropleth by quadrat within saltmarsh sites
- Temporal comparisons by season (Winter vs. Summer)
- Habitat-based pH comparisons (Mudflat vs. Saltmarsh)
- Spatial relationships with grazing regimes and site characteristics
- Integration with other CBESS datasets for ecosystem service and biodiversity analyses