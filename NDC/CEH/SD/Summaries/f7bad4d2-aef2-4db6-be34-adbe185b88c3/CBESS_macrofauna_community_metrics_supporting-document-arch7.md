# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal community metrics - total abundance (TA), total biomass (TB), species richness (SR), evenness (J) and community bioturbation potential (BPc) in mudflat and saltmarsh habitats

## Overview
- Dataset describing macrofaunal community metrics TA, TB, SR, J (abundance), and BPc in mudflat and saltmarsh habitats.
- Based on observations from 6 sites across 2 locations (Essex and Morecambe Bay), sampling 2 habitats at each site.
- Seasonal sampling in winter and summer 2013; 3 replicates across 22 quadrats at 4 spatial scales.
- Field campaign managed by CBESS; data intended for map-based analysis and GIS visualisation.

## Study design and locations
- Locations and sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitat types: Mudflat (MF) and Saltmarsh (SM)
- Habitat/soil contrasts:
  - Saltmarsh: clay soils (Essex) vs sandy soils (Morecambe Bay)
  - Essex vs Morecambe Bay also differ in inundation frequency, creek structure, and vegetation
- Geographic coordinates provided for observation sites

## Sampling and field methods
- Sampling frame: 3 cylindrical sediment cores (10 cm depth, 0.5 cm diameter) per quadrat
- Preservation: cores fixed in 4% buffered formalin in seawater; processed in the lab
- Processing: sieving through 0.5 mm mesh; residues preserved in 70% Industrial Methylated Spirit (IMS)
- Abundance: individuals counted per species
- Biomass: individuals weighed (0.0001 g precision); when too light, recorded as 0.0001 g
- Conversion: results scaled to per m^2 using a factor of 127.323955
- Replication and scale: 3 replicates per quadrat; data for 22 quadrats across four spatial scales (A-D)

## Metrics and calculations
- TA (Total abundance): sum of abundance of all species per m^2
- TB (Total biomass): sum of biomass of all species per m^2
- SR (Species richness): total number of species per m^2
- J' (abundance): Pielou’s evenness based on abundance (H'/H'max), where H' is Shannon-Wiener index on abundance
- H'max: ln(SR) (maximum possible diversity)
- J' (biomass): Pielou’s evenness based on biomass (H'/H'max), with H' calculated from biomass
- BPc (bioturbation potential): sum of BPp per m^2
  - BPp = BPi × Ai
  - BPi = sqrt(Bi) × Mi × Ri
  - Ai = abundance per m^2; Bi = biomass per m^2
  - Mi = mobility; Ri = reworking (behavioural trait)
- Dataset scales: A = 1 m, B = 1–10 m, C = 10–100 m, D = 100 m to upper limit

## Data quality and validation
- Data entry: double-checked by two people
- Biomass cross-check: biomass values validated against corresponding abundance data
- Calculations of metrics double-checked

## Data availability and formats
- File format: CSV (.csv)
- Coverage: no planned repeat sampling noted

## Dataset fields and key variables
- Row Number: sorted order of input
- Season: Winter (W) or Summer (S)
- Location: Morecambe (M) or Essex (E)
- Site: Morecambe: CS, WS, WP; Essex: AH, FW, TM
- Habitat: Mudflat (MF) or Saltmarsh (SM)
- Quadrat Number: 1–22
- Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)
- Replicate: 1–3
- Total abundance: per m^2
- Total biomass: per m^2
- Species richness: per m^2
- H' max: maximum possible diversity (ln SR)
- H' (abundance): Shannon-Wiener index based on abundance
- J' (abundance): Pielou’s evenness based on abundance
- H' (biomass): Shannon-Wiener index based on biomass
- J' (biomass): Pielou’s evenness based on biomass
- BPc: bioturbation potential per m^2

## People and access
- Staff responsible: Christina Wood and Martin Solan
- Data provenance: field campaign during CBESS (winter and summer 2013) with no planned repeat sampling
- Use for GIS: per m^2 metrics across multiple habitats/sites/scales suitable for map-based visualization and spatial analyses