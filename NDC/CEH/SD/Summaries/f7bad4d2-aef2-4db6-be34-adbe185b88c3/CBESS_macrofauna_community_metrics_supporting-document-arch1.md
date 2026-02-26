# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal community metrics - total abundance (TA), total biomass (TB), species richness (SR), evenness (J) and community bioturbation potential (BPc) in mudflat and saltmarsh habitats.

## Overview
- Datasets on macrofaunal community metrics: TA, TB, SR, J (abundance-based), and BPc.
- Spatial and temporal scope: 6 sites across 2 locations (Essex and Morecambe Bay), 2 habitats (mudflat and saltmarsh).
- Sampling period: winter and summer 2013.
- Sampling design: 3 replicates across 22 quadrats at 4 spatial scales.

## Study design and sites
- Locations and sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat contrasts:
  - Saltmarsh representing two soil types: clay soils (Essex) and sandy soils (Morecambe Bay).
  - Mudflat sites with contrasting sediment types between Essex (cohesive clays) and Morecambe Bay (coarse, mobile sediments).
- Spatial scales:
  - Scales A to D corresponding to increasing area (1 m, 1–10 m, 10–100 m, 100 m to basin limit).
- Observation details:
  - Observations include winter (W) and summer (S) seasons, across 22 quadrats per habitat-site.

## Sampling and laboratory methods
- Field sampling:
  - At each quadrat, 3 cylindrical cores (sediment 10 cm depth, diameter unspecified) collected.
- Sample processing:
  - Cores fixed in 4% buffered formalin in seawater; sieved through 0.5 mm mesh.
  - Residue preserved in 70% Industrial Methylated Spirit (IMS).
  - Specimens identified to species level when possible; otherwise sorted into major groups with presence recorded as YES/NO if damaged.
- Biomass and abundance:
  - Abundance: individuals counted per species per replicate.
  - Biomass: individuals weighed (0.0001 g precision); for very light specimens, recorded as 0.0001 g.
  - Conversion: abundance and biomass values converted to per m^2 using a factor of 127.323955.
- Data quality:
  - Raw data input by two people with double-checking; biomass cross-checked against abundance data; calculations validated.

## Metrics and calculations
- TA: total abundance per m^2 (sum of species abundances).
- TB: total biomass per m^2 (sum of species biomasses).
- SR: species richness per m^2.
- J' (abundance): Pielou’s evenness based on abundance; J' = H' / H'max.
- H' (abundance): Shannon-Wiener index based on abundance.
- H' (biomass): Shannon-Wiener index based on biomass.
- H'max: maximum diversity possible, equal to ln(SR).
- BPc: community bioturbation potential per m^2; BPc = sum of BPp for all species per m^2.
  - BPp = BPi × Ai; Ai = abundance per m^2; BPi = sqrt(Bi) × Mi × Ri.
  - Bi = biomass per m^2; Mi = mobility; Ri = reworking.
- Data products: all metrics computed per m^2; results organized in a CSV.

## Data formats and accessibility
- Primary format: .csv.
- Dataset reference: CBESS_macrofauna_abundance.csv (used for cross-checking biomass against abundance).
- Dataset fields include: Season, Location, Site, Habitat, Quadrat Number, Scale, Replicate, Total abundance, Total biomass, Species richness, H' max, H' (abundance), J' (abundance), H' (biomass), J' (biomass), BPc, along with supporting identifiers (Row Number, etc.).

## Dataset field descriptions (highlights)
- Season: Winter (W) or Summer (S).
- Location: Morecambe (M) or Essex (E).
- Site: AH, FW, TM (Essex); CS, WS, WP (Morecambe).
- Habitat: Mudflat (MF) or Saltmarsh (SM).
- Quadrat Number: 1–22.
- Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
- Replicate: 1–3.
- Metrics: 
  - Total abundance, Total biomass, Species richness.
  - H' max, H' (abundance), J' (abundance).
  - H' (biomass), J' (biomass).
  - BPc.

## Context for analysis and interpretation
- Purpose: enable correlations, pattern discovery, and predictive insights about coastal biodiversity and ecosystem service sustainability.
- Intended use: cross-site comparisons, habitat-type differences, seasonal dynamics, and scale-dependent analyses.
- Data provenance and handling: includes location coordinates, habitat descriptions, and standardized procedures to ensure comparability across sites and scales.

## Limitations and considerations
- Temporal scope: single field campaign across winter and summer 2013; no planned repeats noted.
- Local-scale emphasis: designed to capture fine-scale to landscape-scale patterns, with potential limitations for broader generalization.
- Data variability: habitat and sediment type differences, plus site-specific inundation and vegetation differences, may influence metrics.