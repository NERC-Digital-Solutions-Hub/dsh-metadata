# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal abundance in mudflat and saltmarsh habitats.

## Overview
- Dataset of macrofaunal abundance (individuals per square meter) across mudflat and saltmarsh habitats.
- 6 sites over 2 locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Sampling in winter and summer 2013 with 3 replicates per quadrat across 22 quadrats at 4 spatial scales.
- Staff: Christina Wood and Martin Solan.
- Data are provided as CSV with detailed field and taxa descriptions; abundance values are standardized to per m^2.

## Study design and sampling
- Purpose: quantify macrofaunal abundance in contrasting habitat types and sediment contexts.
- Habitats: Mudflat and Saltmarsh at each site; saltmarsh sites chosen to represent contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation/creek structure.
- Sampling scheme: 3 cylindrical cores per quadrat (10 cm depth, fixed in preservative), processed to identify and count taxa.
- Temporal aspect: two seasonal sampling points (winter and summer 2013); no planned repeat sampling beyond this campaign.

## Locations and habitats
- Essex sites: AH (Abbotts Hall), FW (Fingringhoe Wick), TM (Tillingham Marshes) – predominantly clayey mud/sediments for mudflat; saltmarsh with clay soils.
- Morecambe Bay sites: CS (Cartmel Sands), WS (Warton Sands), WP (West Plain) – mudflat with coarser, mobile sediments; saltmarsh with sandy soils.
- Saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation; mudflat differences: cohesive clays/mud/silt in Essex vs. coarse sediments in Morecambe Bay.

## Data collection and processing
- Field method: 3 cores per quadrat; core area combined to yield abundance estimates.
- Preservation and identification: cores fixed in seawater-based preservative, organisms identified (to species where possible) and stored for counting.
- Data handling: counts converted to abundance per m^2 using a specified conversion factor (127.323955) and rounded to the nearest whole number.
- Data quality: two people independently entered data; cross-checked against CBESS macrofauna biomass dataset; species names checked against World Register of Marine Species (WoRMS).

## Data structure and fields
- Primary format: CSV with a detailed schema (Dataset Field Descriptions).
- Key fields:
  - Row Number (sorting index)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS, WS, WP, AH, FW, TM)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m; B: 1–10 m; D: 100 m+)
  - Replicate (C, D, etc.)
  - Measurement Type (Maf: Macrofauna; others as text)
  - Taxa abundance columns (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., etc.)
  - Debris columns (Annelid/Mollusc/Crustacea debris)
  - Other taxa lists (Crustacea, Copepoda, Nematoda, Nemertea, etc.)
- Units: Abundance per taxa per quadrat (later expressed per m^2 via the conversion factor).

## Quality control and provenance
- Data are quality-checked through dual entry and cross-validation with biomass data.
- Taxonomic checks performed against accepted names in WoRMS.
- Provenance: dataset is part of the CBESS project, with explicit documentation of sampling, processing, and formatting procedures.
- File format: CSV, with standardized field descriptions to support re-use.

## Data format and accessibility
- Primary data format: .csv
- Supplementary materials: comprehensive field descriptions for each column, including season, location, site, habitat, and species-specific abundance data.

## Key variables and units
- Abundance: counts of individuals per taxa per quadrat, converted to abundance per m^2 using a specified multiplier.
- Spatial-temporal granularity: seasonal (winter, summer), site, habitat, quadrat, and replicates.
- Taxonomic scope: documented list of macrofaunal taxa and associated debris categories used for presence/absence notes in debris columns.