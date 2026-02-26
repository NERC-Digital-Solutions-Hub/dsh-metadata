# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment chlorophyll concentrations in saltmarsh and mudflat habitats

## Overview
- Measurements: chlorophyll a, b, and c1+c2 concentrations in surface sediments (0–2 mm) expressed as µg g⁻¹.
- Habitat and sites: saltmarsh and mudflat habitats at Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Temporal coverage: winter and summer 2013.
- Replicates and sampling: five replicates per quadrat; sampling occurred across randomly allocated quadrats.
- Responsible staff: Jack Maunder.

## Dataset scope and design
- Site selection: Essex and Morecambe Bay chosen to represent contrasting sediment types and soil types (clay in Essex, sandy soils in Morecambe Bay) with differing inundation, creek structure, and vegetation.
- Habitats: both mudflat and saltmarsh across sites.
- Sampling cadence: part of the CBESS field campaign in 2013 (winter and summer); no planned repeats beyond this campaign.
- Spatial design: 22 1x1 m quadrats per mudflat and saltmarsh site; four spatial scales defined for sub-sampling (A–D) to cover different extents.

## Data collection and processing methods
- Field sampling: surface 2 mm sediment sampled with a contact corer; samples flash-frozen in liquid nitrogen and stored below -80°C to preserve chlorophyll.
- Laboratory processing: samples freeze-dried; chlorophyll extracted with acetone and measured with a Cecil CE3021 spectrophotometer at 630, 647, 664, and 750 nm; concentrations calculated for chl a, chl b, and chl c1+c2.
- Site location: quadrats positioned by random allocation; location data recorded with site and habitat identifiers.
- Quality control and calibration:
  - Calibration scales aligned to standard laboratory protocols; spectrophotometer accuracy checked with standard chlorophyll solutions.
  - Data checks included manual entry of scale readings into spreadsheets; spectrophotometer software used for absorption values.

## Data structure and metadata
- File format: CSV.
- Core dataset fields include: Season (Winter or Summer), Location (Morecambe or Essex), Site (CS, WS, WP, AH, FW, TM), Habitat (Mudflat or Saltmarsh), Quadrat Number, Scale (A–D; representing sampling extent), Chl a (µg g⁻¹), Chl b (µg g⁻¹), Chl c1+c2 (µg g⁻¹), and corresponding Standard Deviation (StDev) where applicable.
- Dataset field descriptions and header definitions accompany the data, enabling sorting and interpretation by data users.
- Handling of missing data: NA indicates missing data due to inaccessibility of the quadrat.

## Governance, provenance, and stewardship
- Documentation includes explicit staff responsibility (Jack Maunder) and detailed methodologies, enabling reproducibility and auditability.
- Provenance captured through description of sampling design, quadrat allocation (randomized via R), laboratory protocols, calibration, and data quality checks.
- Data readiness for discovery and reuse is supported by explicit metadata on sampling design, locations, habitats, temporal coverage, and data formats.
- Note on updates: no explicit plan for future repeats beyond the 2013 campaign.