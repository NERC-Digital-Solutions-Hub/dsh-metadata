# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) total organic carbon in mudflat and saltmarsh habitats..

## Overview
- Dataset measuring total organic carbon (TOC) in mudflat and saltmarsh habitats within the CBESS program.
- Focus: Organic carbon content as determined by loss on ignition (LOI) across multiple habitats and sites.
- Timeframe and design: Samples collected in winter and summer 2013 from 6 sites across 2 locations, with 2 habitat types at each site, 3 replicates, across 22 quadrats at 4 spatial scales.
- Lead personnel: Christina Wood and Martin Solan.
- Data format: CSV files; includes detailed field and measurement descriptors and quality notes.

## Sampling design and scope
- Spatial scope: 6 sites across 2 locations (Essex and Morecambe Bay).
- Habitat scope: Each site includes 2 habitat types—mudflat and saltmarsh.
- Temporal scope: Winter and summer 2013; no planned resampling.
- Replication and scale: 3 replicates across 22 quadrats, spanning 4 spatial scales (A, B, C, D corresponding to 1 m, 1–10 m, 10–100 m, and 100 m to upper limit).
- Measurement focus: Organic carbon content via LOI on sediment samples; samples frozen at -20°C prior to LOI analysis.
- Supplementary context: Saltmarsh and sediment type vary by location (Essex vs. Morecambe Bay).

## Locations, habitats and site details
- Essex sites (clay-dominated, cohesive sediments): Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites (sandy or coarse sediments): Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat contrasts:
  - Saltmarsh: two soil types represented (clay in Essex; sandy in Morecambe Bay).
  - Mudflat: Essex mudflats are cohesive clays; Morecambe Bay mudflats are coarse, mobile sediments.
- Regional differences across saltmarsh sites include inundation frequency, creek structure, and dominant vegetation.

## Observations, methods and data lifecycle
- Primary variable: Organic carbon content estimated via Loss on Ignition (LOI) following standard LOI techniques.
- Sample collection procedures:
  - Mudflats: surface sediment scrapes.
  - Saltmarsh: sediment cut from 2 cm below the surface.
- Sample handling: All samples frozen at -20°C before LOI analysis.
- Calibration and references: Full LOI protocol and calibration details available at the LOI facilities page (external link provided in dataset).
- Data quality and checks: Quality control procedures referenced through LOI methodology page; dataset notes indicate where to find data checking procedures.

## Dataset structure and field descriptions
- Core fields (examples):
  - Row Number: sortable order of input.
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP), Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m–upper limit).
  - Replicate: 1–3.
  - Measurement Type: LOI.
  - Cr (g): Crucible weight before ignition.
  - Cr + Sed (g): Crucible + sediment weight before ignition.
  - 105, 400, 480, 950 (g): weights corresponding to various stages of ignition.
  - 105 (dry weight), 400, 480, 950 (g): weights excluding crucible after ignition at specified temperatures.
  - 105, 400, 480, 480-105, 950 (g): loss figures after ignition at specified temperatures, including differential losses (e.g., 480-105).
  - %Water, %carbohydrate, %total organic, %carbon, %CO2, wtCaCO3, %CaCO3, %Mineral Residue: LOI-derived composition metrics (dry weight basis).
- Data format: CSV.
- Notes: Some cells marked NA indicate no data; metadata describes unit formats and permissible values.

## Data quality, access and metadata
- Data quality and provenance: Data collection aligned with CBESS field campaigns; LOI-based methods linked to publicly documented protocols.
- Data availability: CSV files with comprehensive field descriptors and measurement metadata; site coordinates and location descriptions provided for reproducibility.
- Metadata references: External LOI technique page cited for full methodological details and calibration; data checking and quality control procedures referenced via LOI page and dataset notes.

## Practical considerations for analysis
- Analytic opportunities: Compare TOC across habitats (mudflat vs. saltmarsh), soil types (clay vs. sand), and locations; assess seasonal variation (winter vs. summer 2013); explore scale-dependent patterns across the four spatial scales.
- Potential models: Correlations between LOI-derived TOC and habitat type, sediment type, inundation context, and vegetation; multilevel or hierarchical models across sites and scales.
- Data limitations: Single campaign (2013) with no planned repeat sampling; potential gaps at local scales for some variables; reliance on LOI as proxy for organic carbon requires awareness of methodological assumptions.