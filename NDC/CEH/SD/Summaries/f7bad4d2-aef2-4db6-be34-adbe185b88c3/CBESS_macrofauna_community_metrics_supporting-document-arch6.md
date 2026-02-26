# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal community metrics - total abundance (TA), total biomass (TB), species richness (SR), evenness (J) and community bioturbation potential (BPc) in mudflat and saltmarsh habitats.

## Overview
- Dataset captures macrofaunal community metrics: Total abundance (TA), Total biomass (TB), Species richness (SR), Evenness based on abundance (J_abundance), Evenness based on biomass (J_biomass), and Community bioturbation potential (BPc) per square metre.
- Derived from 6 sites across 2 locations and 2 habitat types (mudflat and saltmarsh) sampled in winter and summer 2013.
- Sampling framework includes 3 cores per quadrat across 22 quadrats at 4 spatial scales.
- Staff responsible: Christina Wood and Martin Solan.

## Study design and locations
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
  - Coordinates are provided for each site.
- Habitat types:
  - Saltmarsh and Mudflat
  - Saltmarsh sites represent contrasting soils: clay soils in Essex and sandy soils in Morecambe Bay; broader differences in inundation frequency, creek structure, and vegetation.
  - Mudflat sites differ by region in sediment type: cohesive clays, mud, and silt in Essex vs coarser, more mobile sediments in Morecambe Bay.
- Monitoring context:
  - Part of the CBESS field campaign (winter and summer 2013).
  - No planned repeat sampling.

## Data collection and processing
- Field sampling:
  - At each quadrat: 3 cylindrical cores (10 cm depth, 10 cm diameter).
  - Cores fixed in 4% buffered formalin in seawater; processed by sieving (0.5 mm) and preserved in 70% Industrial Methylated Spirit (IMS).
- Observations and measurements:
  - Abundance: count individuals per species; debris and damaged specimens recorded as major groups with presence noted.
  - Biomass: weigh individuals to 0.0001 g; damaged/debris similarly processed.
  - All data converted to per-m^2 values using a factor of 127.323955; results rounded to the nearest individual (abundance) or nearest 0.0001 g (biomass).
- Metrics calculations:
  - TA: sum of abundance per m^2.
  - TB: sum of biomass per m^2.
  - SR: total number of species per m^2.
  - J_abundance: Pielou’s evenness based on abundance (H'/H'max) with H' calculated from abundance data.
  - J_biomass: Pielou’s evenness based on biomass (H'/H'max) with H' calculated from biomass data.
  - BPc: sum of BPp across all species per m^2, where BPp = BPi × Ai, and BPi = (√Bi) × Mi × Ri (Bi = biomass per m^2, Mi = mobility, Ri = reworking).
- Quality control:
  - Raw data input by two people and double-checked; biomass cross-checked against abundance data file.
  - Calculations checked and verified.

## Data formats and quality
- File format: CSV
- Data checks and validation steps are documented (double entry, cross-checks, and consistency between abundance and biomass files).

## Dataset field descriptions
- Field structure includes: Row Number, Season (Winter W, Summer S), Location (Morecambe M, Essex E), Site (CS, WS, WP, AH, FW, TM), Habitat (Mudflat MF, Saltmarsh SM), Quadrat Number (1–22), Scale (A-D corresponding to 1 m, 1–10 m, 10–100 m, and >100 m), Replicate (1–3).
- Metrics and derived statistics:
  - Total abundance, Total biomass
  - Species richness
  - H'max (maximum diversity) and H' (Shannon-Wiener index) for abundance and biomass
  - J' (Pielou’s evenness) for abundance and biomass
  - BPc (bioturbation potential)
- Descriptions include formulas and unit definitions (e.g., per m^2), and notes on how to interpret each field.