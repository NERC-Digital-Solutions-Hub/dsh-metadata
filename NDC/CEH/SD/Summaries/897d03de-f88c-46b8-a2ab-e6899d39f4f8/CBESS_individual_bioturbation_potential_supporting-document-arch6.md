# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) individual bioturbation potential in mudflat and saltmarsh habitats.

## Overview
- Dataset describing individual bioturbation potential (BPi) across mudflat and saltmarsh habitats as part of CBESS.
- Data derived from 6 sites at 2 locations (Essex and Morecambe Bay) and 2 habitats per site, collected in winter and summer 2013.
- Abundance and biomass data per species used to compute BPi per m², enabling comparison of bioturbation potential across habitats, seasons, and locations.

## Sampling design and scope
- Sampling framework: 3 replicates across 22 quadrats per habitat, at 4 spatial scales.
- Habitats: Mudflat and Saltmarsh; saltmarshes represent contrasting soil types (clay in Essex, sandy in Morecambe Bay).
- Sites/Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Seasons: Winter (W) and Summer (S) 2013.
- No planned repeat sampling beyond these campaigns.

## Data collected and key variables
- Primary measurement: Bioturbation potential per individual (BPi) for a list of species, plus aggregate BPc and BPp calculations.
- Abundance and biomass: Counts and weights for each species per replicate; biomass used with abundance to compute BPi.
- Processing to per-area: Abundance and biomass values converted to per square metre using a conversion factor (127.323955).
- Derived metrics:
  - BPi = (sqrt Bi) × Mi × Ri, where Bi = biomass, Mi = mobility, Ri = reworking contribution.
  - BPp (per msquared) = BPi × Ai, where Ai = species abundance per m²; BPc = sum of all BPp per m².
- Species covered (examples): Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, Macoma balthica, Mytilus edulis juveniles, Crangon crangon, Cerastoderma edule, and many others listed in the dataset field descriptions.
- Data are stored and described by per-quadrat observations and species-level BPi/abundance/biomass values.

## Procedures and quality assurance
- Field/lab methods:
  - Collect three cylindrical cores per quadrat (10 cm depth, 10 cm diameter).
  - Fix in 4% buffered formalin in seawater; sieve through 0.5 mm mesh.
  - Identify organisms to species level; count and store in 70% IMS.
  - For biomass, blot and weigh individuals (0.0001 g precision; 0.0001 g default if too light).
  - Convert abundance and biomass to per m² using the specified factor.
- Data handling and QA:
  - Raw data entered by two people and double-checked.
  - Biomass data cross-checked against corresponding abundance data (CBESS_macrofauna_abundance.csv).
  - BPi calculations checked and re-checked.
- Data formats:
  - Primary dataset available in CSV format.
  - Data check flag and NA usage: NA indicates no data for a cell.

## Dataset structure and metadata
- Dataset Field Descriptions include:
  - Row Number, Season (Winter W or Summer S), Location (Morecambe M or Essex E), Site (e.g., AH, FW, TM, CS, WS, WP), Habitat (Mudflat MF or Saltmarsh SM), Quadrat Number (1–22), Scale (A–D representing spatial extents), Measurement Type (BPi), and per-species fields with BPi values and counts.
- Species and measures are listed with both BPi values and counts where applicable.
- File formats: .csv; additional notes indicate original data order and formatting details.
- Data provenance: Staff responsible = Christina Wood and Martin Solan.

## Location, timing, and usage notes
- Locations chosen to contrast sediment types and inundation regimes to capture variability in bioturbation potential across habitats.
- Timeframe: Winter and Summer 2013 field campaigns; no planned repeat sampling beyond this dataset.
- Usage considerations:
  - Conversion factor applied to standardize to per-m² units.
  - NA indicates missing data for a given cell.
  - The dataset supports cross-site, cross-habitat, and seasonal analyses of bioturbation potential.