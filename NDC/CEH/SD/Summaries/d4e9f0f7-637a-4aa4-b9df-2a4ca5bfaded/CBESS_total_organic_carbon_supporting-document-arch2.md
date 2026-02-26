# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) total organic carbon in mudflat and saltmarsh habitats.

- Dataset purpose and scope
  - Measures total organic carbon (TOC) in mudflat and saltmarsh habitats as part of CBESS.
  - TOC calculated from samples across 6 sites in 2 locations (Essex and Morecambe Bay), each with 2 habitat types (mudflat and saltmarsh).

- Sampling design and locations
  - Locations/sites:
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Spatial and habitat design:
    - Saltmarsh chosen to represent two contrasting soil types (clay in Essex; sandy in Morecambe Bay).
    - Mudflat and saltmarsh sites reflect differences in sediment types, inundation frequency, creek structure, and vegetation.
  - Coordinates provided for each site; selection aims to capture environmental contrasts.

- Sampling and replication
  - Sampling periods: winter and summer 2013.
  - 3 replicates across 22 quadrats.
  - Spatial scales: A (1 m), B (1–10 m), C (10–100 m), D (100–upper limit).

- Measurements and laboratory methods
  - Primary variable: organic carbon content measured by Loss on Ignition (LOI).
  - Sample processing:
    - Mudflats: surface sediment scrapes.
    - Saltmarsh: sediment collected from 2 cm below the surface.
    - Samples frozen at -20°C prior to LOI analysis.
  - LOI methodology linked to an external protocol.

- Data structure and file formats
  - Data format: CSV.
  - Key dataset fields and descriptions (examples):
    - Row Number: sortable identifier.
    - Season: Winter (W) or Summer (S).
    - Location: Morecambe (M) or Essex (E).
    - Site: CS, WS, WP (Morecambe); AH, FW, TM (Essex).
    - Habitat: Mudflat (MF) or Saltmarsh (SM).
    - Quadrat Number: 1–22.
    - Scale: A–D (spatial extent).
    - Replicate: 1–3.
    - Measurement Type: LOI.
    - Cr (g), Cr + Sed (g), Cr + Sediment Weight, etc. (crucible and sediment weights at various states).
    - %Water, %carbohydrate, %total organic, %carbon, %CO2, wtCaCO3, %CaCO3, %Mineral Residue, etc.
  - Data quality and checks:
    - Calibration, QA, and data checking procedures reference the LOI technique page.
    - NA entries indicate missing data.

- Data provenance and stewardship
  - Staff responsible: Christina Wood and Martin Solan.
  - Monitoring context: part of the general CBESS field campaign.
  - Data handling notes:
    - No repeat sampling planned for these sites within this dataset.
    - Data stored and described with explicit field definitions and procedural references.