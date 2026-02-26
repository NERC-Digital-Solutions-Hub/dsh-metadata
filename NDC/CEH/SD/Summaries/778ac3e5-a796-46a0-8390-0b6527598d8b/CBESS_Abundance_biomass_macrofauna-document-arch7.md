# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) mobile macrofaunal abundance, biomass and species richness from Fyke netting in mudflat habitats.

## Overview
- Purpose: Provides map-ready data on mobile macrofauna abundance, biomass, and species richness from fyke netting in mudflat habitats for CBESS.
- Geography: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Habitat context: Mudflats with varying sediment types and tidal exposure between Essex estuarine sites and Morecambe Bay sites.
- Timeframe: Winter and Summer 2013 as part of a general field campaign.
- Responsible staff: Mark Emmerson.
- Data format: Excel workbook; NA cells indicate no data.

## Data content and methods
- Observed metrics:
  - Abundance: number of individuals per fyke net deployment.
  - Biomass: total catch wet weight (grams) per species per fyke net deployment.
  - Species richness: number of species caught per fyke net deployment.
- Sampling method:
  - Five double-hoop fyke nets (mesh size 22 mm knot-to-knot, 8 m leader, 0.5 m hoop).
  - Nets deployed perpendicular to shore at the outer edge of each quadrat.
  - Deployment spans two executive tidal cycles; catches processed the following day.
- Spatial and temporal sampling:
  - Quadrats across each site; quadrat numbers 1–22.
  - Seasons: Winter (W) and Summer (S).
- Sites and habitats:
  - Essex: AH, FW, TM (Mudflat, MF).
  - Morecambe Bay: CS, WS, WP (Mudflat, MF).
- Included species (examples of fields):
  - Abundance fields: Carcinus maenas_A, Clupea harengus_A, Crangon crangon_A, Anguilla anguilla_A, Pollachius virens_A, Dicentrarchus labrax_A, Pomatoschistus sp_A, Asterias rubens_A, etc.
  - Biomass fields: Platichthys flesus_B, Carcinus maenas_B, Clupea harengus_B, Crangon crangon_B, Anguilla anguilla_B, Pollachius virens_B, Dicentrarchus labrax_B, Pomatoschistus sp_B, etc.
  - Species richness field: Species Richness (per fyke net).
- Data validation: All values double-checked against field/lab notebooks after digitization.

## Data structure and formats
- Main file format: Excel workbook.
- Key fields and organization:
  - Row Number: sorting index (numeric).
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: AH, FW, TM (Essex); CS, WS, WP (Morecambe).
  - Habitat: Mudflat (MF).
  - Quadrat Number: 1–22 (numeric).
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
  - Pardo field: present but not populated (value ".").
  - Species-specific fields: abundance (_A) and biomass (_B) per fyke net deployment for listed species.
- Data quality indicators:
  - NA cells indicate no data.
  - Values are per fyke net deployment.

## GIS usage considerations
- Spatial resolution: Per-quadrat observations, enabling fine-scale mapping within each site.
- Temporal slices: Separate layers or attributes for Winter and Summer 2013 data.
- Cross-site comparability: Essex vs. Morecambe Bay differences in sediment and tidal ranges should be accounted for in analyses.
- Data integration: Combines per-species abundance and biomass with species richness, suitable for heatmaps, choropleth maps, and species distribution visualizations.
- Handling notes:
  - Many species have separate abundance (A) and biomass (B) fields; ensure proper aggregation if summarizing by site or season.
  - Some fields and metadata (e.g., Pardo) may be empty; interpret as not applicable.

## Access, contact, and limitations
- Primary contact: Mark Emmerson.
- Limitations:
  - Focused on larger mobile macrofauna captured by fyke nets; may not represent smaller organisms or other sampling methods.
  - Data limited to Winter and Summer 2013 campaigns; may not reflect longer-term trends.