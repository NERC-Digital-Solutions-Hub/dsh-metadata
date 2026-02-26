# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal abundance in mudflat and saltmarsh habitats.

## Overview
- Dataset of macrofaunal abundance (individuals per m^2) across mudflat and saltmarsh habitats.
- 6 sites over 2 locations (Essex and Morecambe Bay), sampled in winter and summer 2013.
- 3 replicates per habitat per quadrat, totaling 22 quadrats across 4 spatial scales.
- Part of the CBESS field campaign; data checked for quality and consistency.

## Study Design and Sampling
- Sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West plain).
- Habitats: Mudflat (MF) and Saltmarsh (SM).
- Temporal coverage: Winter (W) and Summer (S) 2013.
- Sampling intensity: 3 cylindrical cores per quadrat (10 cm depth, 10 cm diameter) across 22 quadrats.
- Spatial scales: Four scales (A = 1 m; B = 1–10 m; C = 10–100 m; D = 100 m to upper limit).

## Locations, Habitats, and Site Details
- Essex saltmarsh: contrasting clay soils; More frequent inundation and distinct vegetation structure compared to Morecambe.
- Morecambe Bay saltmarsh: sandy soils; different inundation patterns and creek structures.
- Mudflats: Essex dominated by cohesive clays; Morecambe by coarse, mobile sediments.

## Data Collection and Processing
- Observation process: 3 cores per quadrat, fixed in 4% buffered formalin, sieved through 0.5 mm, preserved in 70% IMS.
- Identification: species level (or appropriate taxon) using stereo microscopy; counted to obtain abundance data.
- Conversion: counts multiplied by 127.323955 and rounded to the nearest whole number to yield abundance per m^2.
- Quality control: data entered independently by two people; cross-checked against CBESS_macrofauna_biomass.csv; species names validated against WoRMS.

## Data Structure and Variables
- Primary format: CSV (.csv).
- Core fields (Row/Meta): 
  - Row Number, Season (Winter W / Summer S), Location (Morecambe M / Essex E), Site (CS, WS, WP, AH, FW, TM), Habitat (Mudflat MF / Saltmarsh SM), Quadrat Number (1–22), Scale (A/B/C/D), Replicate (C/D and related codes), Measurement Type (Maf = Macrofauna / Abundance).
- Taxa data: extensive list of taxa with numeric Abundance values (per quadrat), including numerous annelids, molluscs, crustaceans, and related debris indicators (Annelid debris, Mollusc debris, Crustacea debris).
- Example taxa: Arenicola marina, Hediste diversicolor, Glycera alba, Nephtys hombergii, Mya arenaria, Crangon crangon, Gammarus spp., plus many others.
- Debris indicators: separate columns for major debris categories (Annelid, Mollusc, Crustacea debris).

## Spatial and GIS-Relevance
- Rich, spatially explicit dataset suitable for map-based analyses of species distribution across habitats and scales.
- Multi-site, multi-habitat design enables comparative GIS analyses of habitat-specific assemblages and environmental gradients.
- Precise site coordinates provided for Essex and Morecambe Bay locations.

## Data Quality, Provenance, and Related Resources
- Data provenance linked to the CBESS field campaign (2013); included cross-check against biomass data file.
- Taxonomic validation against World Register of Marine Species (WoRMS).
- No planned repeats noted for sampling; dataset designed for wide-format, multi-taxa abundance analysis.