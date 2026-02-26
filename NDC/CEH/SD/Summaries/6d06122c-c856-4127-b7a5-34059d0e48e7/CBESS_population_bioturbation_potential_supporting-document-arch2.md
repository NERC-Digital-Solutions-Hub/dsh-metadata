# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) population bioturbation potential in mudflat and saltmarsh habitats.

## Purpose and scope
- Document describes a CBESS dataset on population bioturbation potential (BPp) in mudflat and saltmarsh habitats.
- Aims to standardise environmental monitoring outputs and enable scrutiny of ecological health and policy performance over time.
- Study covers 6 sites across 2 locations (Essex and Morecambe Bay) and 2 habitat types (mudflat and saltmarsh), sampled in winter and summer 2013.
- Sampling design includes 3 replicates across 22 quadrats at 4 spatial scales, with two habitat types chosen to contrast sediment soils and inundation/vegetation characteristics.

## Study design and locations
- Locations and coordinates:
  - Essex: Abbotts Hall (AH) 51.783°N, 0.867°E; Fingringhoe Wick (FW) 51.817°N, 0.967°E; Tillingham Marshes (TM) 51.683°N, 0.933°E
  - Morecambe Bay: Cartmel Sands (CS) 54.167°N, 3.000°W; Warton Sands (WS) 54.133°N, 2.800°W
- Habitat contrasts:
  - Saltmarsh: three sites in Essex (clay soils) and three sites in Morecambe Bay (sandy soils).
  - Differences between regions include inundation frequency, creek structure, and dominant vegetation.
- Habitat characteristics:
  - Mudflats in Essex: cohesive clays, mud, silt.
  - Mudflats in Morecambe Bay: coarser, more mobile sediments.

## Data collection and variables
- Primary variable: Population bioturbation potential (BPp) per sample.
- Field procedures:
  - At each quadrat: 3 cylindrical cores (10 cm depth, 10 cm diameter) fixed in 4% buffered formalin in seawater.
  - Cores processed by sieving (0.5 mm) and preserving residue in 70% IMS.
  - Species identified to species level; abundance counted; biomass measured (0.0001 g precision; if too light, recorded as 0.0001 g).
  - Abundance and biomass data converted to per-square-meter values using a fixed multiplier (127.323955) prior to BPp calculation.
- BPp calculation:
  - Bioturbation potential per species: BPi = (sqrt(Bi)) × Mi × Ri
    - Bi = biomass per m^2 for the species
    - Mi = mobility of the species
    - Ri = reworking ability of the species
  - Per-sample BPp: BPp = BPi × Ai
    - Ai = abundance per m^2
- Taxa covered:
  - Detailed species list includes Arenicola marina, Ampharete lindstroemi, Capitella sp., Eteone longa, various polychaetes, crustaceans, molluscs, and meiofauna. Numerous taxa are enumerated with BPp allocations.
- Temporal scope:
  - Winter (W) and Summer (S) 2013 sampling; no planned repeat sampling beyond this CBESS field campaign.

## Data quality, calibration, and validation
- Data entry:
  - Raw data entered by two people and double-checked.
  - Biomass data cross-checked against abundance data to ensure consistency between files.
- Calculations:
  - BPp calculations double-checked to ensure accuracy.
- Calibration:
  - Calibration field noted as NA where not applicable.

## Data formats, organization, and metadata
- File format: CSV.
- Dataset structure:
  - Field descriptions include: Row Number, Season (Winter or Summer), Location (Essex or Morecambe), Site (AH, FW, TM, CS, WS), Quadrat Number, Scale (A–D representing 1 m to 100 m scales), Replicate (1–3), Measurement Type (BPp), and species-specific BPp/abundance data.
- Available variables:
  - Seasonal and spatial metadata, site-level descriptors, habitat types, quadrat and scale identifiers, replicate numbers.
  - Species-specific BPp values alongside corresponding abundance and biomass data.

## Monitoring context and usage
- Part of the general CBESS field campaign, employing standardised methods to facilitate cross-site comparisons and trend assessment.
- Outputs suitable for inclusion in reports, maps, and charts to communicate environmental health and policy performance.
- Data stewardship:
  - Raw and processed datasets are stored and uploaded to appropriate data portals to enable access by others.

## Data limitations and considerations
- Temporal limitation: Single field campaign (Winter and Summer 2013) with no planned repeats, limiting long-term trend inferences from this dataset alone.
- Spatial scope: Two UK regions (Essex and Morecambe Bay) with habitat-specific contrasts; may limit generalisation to other mudflat/saltmarsh systems.
- Complexity: Large number of species and derived BPp metrics may require careful interpretation when aggregating across taxa or scales.

## Staff and contact
- Staff responsible: Christina Wood and Martin Solan.