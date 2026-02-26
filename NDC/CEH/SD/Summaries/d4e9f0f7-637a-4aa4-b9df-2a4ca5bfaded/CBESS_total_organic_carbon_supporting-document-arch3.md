# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) total organic carbon in mudflat and saltmarsh habitats.

## Overview
- Dataset measuring total organic carbon in coastal mudflat and saltmarsh habitats using Loss on Ignition (LOI).
- Collected from 6 sites across 2 locations: Essex and Morecambe Bay.
- Habitats surveyed: mudflat and saltmarsh.
- Sampling occurred during winter and summer 2013; 3 replicates across 22 quadrats at 4 spatial scales.
- Staff responsible: Christina Wood and Martin Solan.
- Provides detailed metadata, sampling design, and QA references; data structured for sharing and reuse.

## Sampling design and locations
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat/soil contrasts:
  - Saltmarsh with two contrasting soil types: clay soils (Essex) and sandy soils (Morecambe Bay).
  - Mudflat sites: cohesive clays/mud/silt in Essex; coarse, mobile sediments in Morecambe Bay.
- Broader site characteristics differ in inundation frequency, creek structure, and dominant vegetation.
- Campaign scope: CBESS field campaign conducted in winter and summer 2013; no planned repeats.

## Measurement methods and data handling
- Primary measurement: Organic carbon content via Loss on Ignition (LOI).
- Field collection methods:
  - Mudflats: surface sediment scrapes.
  - Saltmarsh: sediment cut from 2 cm below the surface.
- Sample preservation: all samples frozen at -20°C prior to LOI analysis.
- Calibration and data checks: detailed LOI procedure referenced at http://www.geog.cam.ac.uk/facilities/laboratories/techniques/loi.html.
- Data visibility: datasets intended to be open with underlying data shared; full procedural details reside in the LOI methodology page.

## Data structure and formats
- File format: CSV.
- Core fields and structure:
  - Row Number: sortable index.
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe: CS, WS, WP; Essex: AH, FW, TM.
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit).
  - Replicate: 1–3.
  - Measurement Type: LOI.
  - Multiple numeric fields documenting crucible weights, sediment weights at various temperatures, dry weights, losses after ignition, and various composition metrics (e.g., % Water, %Total Organic, %Carbon, %CaCO3, %Mineral Residue, etc.).
- Dataset Field Descriptions (selected):
  - Cr (g): Crucible weight.
  - Cr + Sed: Crucible plus sediment weight.
  - 105, 400, 480, 950: sediment weight after ignition at specified temperatures (°C).
  - 105 (dry weight), 400, 480, 950: weight excluding crucible after ignition (drying steps).
  - 105, 400, 480, 950: Loss (g) after ignition.
  - %Water, %carbohydrate, %total organic, %carbon, %CO2, wtCaCO3, %CaCO3, %Mineral Residue: composition metrics on dry weight basis.

## Quality assurance, metadata, and governance
- Explicit QA and data checking procedures reference the LOI technique page for consistency and traceability.
- Metadata richness includes site coordinates, habitat types, sampling season, scales, and replication details to support data verification and cross-site comparability.
- Data sharing considerations highlighted by the dataset’s detailed field descriptions and standardized structure, aiding transparency and future reuse under a monitoring framework.

## Relevance for Monitoring Frameworks
- Demonstrates a standardized approach to quantify coastal soil organic carbon across multiple sites and habitats, aligned with environmental health monitoring objectives.
- Provides multi-scale sampling design (A–D scales) and replicate structure suitable for trend analysis and policy evaluation.
- Comprehensive metadata and clear measurement procedures support data governance, provenance tracking, and open data practices.
- Highlights practical monitoring challenges (e.g., metadata completeness, data transformation needs, and ensuring open access) and how this dataset addresses them through explicit field definitions and external methodology references.