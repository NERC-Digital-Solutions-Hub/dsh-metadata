# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) individual bioturbation potential in mudflat and saltmarsh habitats.

## Overview
- Metadata describes a CBESS dataset on individual bioturbation potential (BPi) in mudflat and saltmarsh habitats.
- Focuses on per-species BPi, derived from field samples across multiple sites, habitats, seasons, and spatial scales.

## What is included
- Individual bioturbation potential (BPi) for numerous species, plus derived metrics:
  - BPi per species
  - BPc (sum of BPp for all species per square metre)
  - BPp = BPi × Ai (Ai = abundance per m²)
- Abundance and biomass data used to compute BPi
- Dataset field descriptions detailing variables, scales, and species list
- File format: CSV
- Data quality checks and procedures described

## Study design and locations
- Sites: 6 sites across 2 locations
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitats: mudflat (MF) and saltmarsh (SM) at each site
- Sampling period: winter and summer 2013
- Replication and sampling structure: 3 cores per quadrat across 22 quadrats, at 4 spatial scales

## Data collection methods
- Core sampling: three cylindrical sediment cores (10 cm depth, 10 cm diameter) per quadrat
- Processing: cores fixed in formalin, sieved (0.5 mm), organisms identified to species or appropriate taxon
- Abundance and biomass: counted individuals and weighed biomass per replicate
- Data handling: biomass values checked against abundance data; QA procedures include double data entry and cross-checks

## Variables and measurements
- Primary variable: Bioturbation potential per individual (BPi)
- Per-species measurements: abundance and biomass for listed taxa
- Derived measurements:
  - Ai: individual species abundance per m²
  - Bi: individual biomass
  - Mi: mobility of species
  - Ri: reworking capacity
  - Bioturbation potential per species (BPi) and per m² (BPp)
  - BPc: sum of BPp across all species per m²
- Spatial scale categorization:
  - A = 1 m
  - B = 1–10 m
  - C = 10–100 m
  - D = 100 m to upper limit
- Data columns include season, location, site, habitat, quadrat number, scale, measurement type, and per-species BPi/BPp values

## Data processing and quality assurance
- Calculation formula: BPi = (sqrt(Bi)) × Mi × Ri; BPp = BPi × Ai; BPc = sum(BPp) per m²
- Data checks:
  - Two-person data entry and double-checking
  - Biomass validated against abundance data
  - Calculations of BPi and BPc double-checked
- Calibration procedures noted as NA where not applicable

## Data structure and file formats
- Primary file format: CSV
- Dataset field descriptions include:
  - Row Number (sorting), Season (Winter or Summer), Location (Morecambe or Essex), Site, Habitat (Mudflat or Saltmarsh), Quadrat Number, Scale (A–D), Measurement Type (BPi), and per-species measurements
- Species list includes numerous benthic taxa (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Crangon crangon, Mytilus edulis juveniles, etc.)

## Spatial and temporal coverage
- Spatial: coastal sites in Essex and Morecambe Bay with contrasting sediment/habitat types
- Temporal: winter and summer 2013; no planned repeats beyond the 2013 campaign

## How GIS specialists can use this dataset
- Create map-based visualisations of BPi and BPc across sites, habitats, and spatial scales
- Join per-species BPi maps with other spatial layers (habitat type, sediment type, inundation patterns)
- Analyze spatial patterns of bioturbation potential to inform ecosystem service assessments
- Use scale classifications (A–D) to visualize fine-to-coarse spatial gradients
- Retrieve per-quadrat and per-species data for targeted GIS analyses or to populate map dashboards

## Contacts
- Staff responsible: Christina Wood and Martin Solan

## Notes for users
- Data represent a single sampling campaign (no repeats planned) and should be interpreted accordingly
- Ensure proper handling of per-m² normalization and the derived BPi/BPp calculations when integrating with other datasets
- Consider habitat-specific differences ( Essex: clay soils; Morecambe Bay: sandy soils) and inundation/creek structure when comparing sites
- The dataset includes comprehensive field methods and QA steps to support reproducibility in GIS analyses