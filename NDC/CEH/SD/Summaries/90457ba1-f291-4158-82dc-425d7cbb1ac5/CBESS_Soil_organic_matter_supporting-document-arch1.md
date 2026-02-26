# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil organic matter content from three soil depths on saltmarsh sites at Morecambe Bay and Essex

## Overview
- Dataset capturing soil organic matter (SOM) content from three depths (0–10 cm, 10–20 cm, 20–30 cm) on saltmarsh sites in Essex and Morecambe Bay.
- SOM measured by loss-on-ignition (LOI) using bulk density samples.
- Field campaign conducted Winter and Summer 2013; Essex winter samples collected 2–6 March 2013 as an additional window.
- Staff: Hilary Ford.
- Sites represent contrasting soil types (Essex: clay; Morecambe Bay: sandy) and differing grazing regimes.

## Locations and site descriptions
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Regional differences:
  - Essex: hare-grazed; heavy grazing by Brent geese at AH and FW.
  - Morecambe Bay: intensive sheep grazing at CS and WS; pink-footed geese grazing in winter; West Plain lightly grazed.
- Coordinates provided for each site (e.g., AH, FW, TM in Essex; CS, WS in Morecambe Bay; WP as West Plain).

## Methods and data collection
- SOM assessed via LOI from bulk density samples.
- Bulk density rings used: 3.1 cm height, 7.5 cm diameter.
- Depths analyzed: 0–10 cm, 10–20 cm, 20–30 cm.
- Samples dried at 105°C for 72 hours; sub-samples dried at 375°C for 16 hours to determine OM percentage.
- Sampling window included both Winter and Summer 2013; Essex winter samples collected in early March 2013.
- File format: Excel workbook; NA cells indicate no data.

## Variables and data structure
- Core variables:
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe – Cartmel Sands (CS), Warton Sands (WS), West Plain (WP); Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
  - OM_10-20: Soil organic matter (%) at one depth interval (as described in metadata; intended to represent SOM across the target depths).
  - OM_20-30: Soil organic matter (%) at another depth interval (likewise described in metadata).
- Data organization notes:
  - Row Number provides original input order.
  - Each observation includes corresponding season, location, site, habitat, and spatial scale indicators.

## Data quality and considerations
- Calibration procedures: Not specified (not provided).
- Quality control: Data described as Excel workbook with explicit handling of missing data (NA).
- Depth-related labeling for OM fields may contain inconsistencies in the metadata; analysts should verify depth mappings during analysis.
- Spatial and temporal scope is limited to six saltmarsh sites in two UK regions and toWinter/Summer 2013 timeframe, with an additional Essex winter window; suitability for broader generalizations may be limited.
- Local grazing regimes and inundation differences present potential confounders when analyzing SOM across sites.

## Uses for analysis and practical applications
- Compare SOM across sites, depths, habitats, and seasons.
- Assess influence of soil type (clay vs. sandy) and grazing intensity on SOM.
- Develop predictive models of SOM as a function of site characteristics, depth, season, and habitat.
- Integrate with other CBESS datasets to study ecosystem services and biodiversity–soil interactions at saltmarsh sites.

## Provenance and access
- Source: CBESS project dataset.
- Principal contact: Hilary Ford.
- File type: Excel workbook with structured fields and explicit metadata on observations.