# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) mobile macrofaunal abundance, biomass and species richness from Fyke netting in mudflat habitats.

## Overview
- Dataset documenting abundance, biomass, and species richness of larger mobile macrofauna collected via fyke nets in Essex and Morecambe Bay mudflats.
- Collected during Winter and Summer 2013 as part of a general field campaign.
- Focuses on per-quadrat catches using fyke nets to assess community structure and biomass.

## Location and sites
- Essex
  - Abbotts Hall (AH): 51.7833 N, 0.8667 E
  - Fingringhoe Wick (FW): 51.8167 N, 0.9667 E
  - Tillingham Marshes (TM): 51.6833 N, 0.9333 E
- Morecambe Bay
  - Cartmel Sands (CS): 54.1667 N, -3.0 W
  - Warton Sands (WS): 54.1333 N, -2.8 W
  - West Plain (WP): 54.15 N, -2.9667 W
- Habitat context
  - Essex mudflats: cohesive clays, mud and silt.
  - Morecambe mudflats: coarse, mobile sediments; sites more exposed with larger tidal ranges.

## Sampling and methods
- Equipment and design
  - Five double hoop fyke nets (mesh 22 mm knot-to-knot, 8 m leader, 0.5 m hoops).
  - Deployed perpendicular to shore at the outer edge of each quadrat.
  - Observations collected over two successive tidal cycles; catches processed the following day.
- Observed variables
  - Abundance: total number of individuals per fyke net deployment.
  - Biomass: total catch wet weight (g), calculated per species.
  - Species richness: number of species caught per deployment.
- Survey timing
  - Winter (W) and Summer (S) seasons within Winter and Summer 2013 field campaigns.

## Data structure and content
- Data format
  - Excel workbook; NA cells indicate missing data.
  - All values double-checked against field/lab notebooks after digitization.
- Dataset fields (highlights)
  - Row Number: sortable index (numeric).
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe CS/WS/WP; Essex AH/FW/TM.
  - Habitat: Mudflat (MF).
  - Quadrat Number: 1–22.
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
  - Species-specific data
    - Abundance fields (A) for multiple species (e.g., Carcinus maenas_A, Clupea harengus_A, Crangon crangon_A, Anguilla anguilla_A, Pollachius virens_A, Dicentrarchus labrax_A, Pomatoschistus sp_A, Asterias rubens_A).
    - Biomass fields (B) for corresponding species (e.g., Platichthys flesus_B, Carcinus maenas_B, Clupea harengus_B, Crangon crangon_B, Anguilla anguilla_B, Pollachius virens_B, Dicentrarchus labrax_B, Pomatoschistus sp_B).
  - Notes
    - Some fields indicate whether the value represents abundance (A) or biomass (B) per fyke net deployment; biomass values are in g (wet weight).

## Data quality and provenance
- Responsible staff: Mark Emmerson.
- Quality control: All values double checked against field and laboratory notebooks after digitization.

## Access and usage considerations
- Availability
  - Data provided as an Excel workbook with per-quadrat, per-season measurements across six sites.
- Metadata and discoverability
  - Rich site descriptions and coordinates enable cross-site comparisons and integration with broader CBESS datasets.
- Practical notes for use
  - Data combines abundance and biomass metrics alongside species richness, suitable for cross-site community analyses and ecosystem service assessments.
  - Differences in habitat and tidal exposure between Essex and Morecambe Bay should be considered when aggregating results.
  - Missing values are explicitly indicated as NA, requiring careful handling in analyses.