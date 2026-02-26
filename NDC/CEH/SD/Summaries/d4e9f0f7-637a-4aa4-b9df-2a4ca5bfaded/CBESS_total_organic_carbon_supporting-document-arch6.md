# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) total organic carbon in mudflat and saltmarsh habitats

- A dataset of total organic carbon measured via loss on ignition (LOI) in mudflat and saltmarsh habitats as part of the CBESS program.
- Samples collected from 6 sites across 2 locations (Essex and Morecambe Bay) during winter and summer 2013.
- 3 replicates across 22 quadrats at 4 spatial scales per habitat.
- Staff: Christina Wood and Martin Solan.

## Study Sites and Habitats

- Essex
  - Abbotts Hall (AH) — 51.783°N, 0.8667°E
  - Fingringhoe Wick (FW) — 51.8167°N, 0.9667°E
  - Tillingham Marshes (TM) — 51.6833°N, 0.9333°E
- Morecambe Bay
  - Cartmel Sands (CS) — 54.1667°N, 3.0000°W
  - Warton Sands (WS) — 54.1333°N, 2.8000°W
  - West Plain (WP) — 54.1500°N, 2.9667°W

- Habitat and soil contrasts:
  - Saltmarsh across sites with contrasting soil types: clay-rich soils in Essex vs sandy soils in Morecambe Bay.
  - Essex saltmarsh and Morecambe Bay saltmarsh differ in inundation frequency, creek structure, and vegetation.
  - Mudflats: Essex characterized by cohesive clays, mud, and silt; Morecambe mudflats with coarser, mobile sediments.

## Data Collection and Processing

- Monitoring: General CBESS field campaign conducted in winter and summer 2013; no planned repeats.
- Sample collection:
  - Mudflats: surface sediment scrapes.
  - Saltmarsh: sediment sampled from 2 cm below the surface.
- Storage and analysis:
  - Samples frozen at -20°C, analyzed by standard LOI techniques.
  - Calibration, data checking, and methodological references provided via linked LOI resources.
- File formats: .csv

## Dataset Structure and Variables

- Core fields (examples):
  - Row Number (sorting order)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A–D; 1 m, 1–10 m, 10–100 m, 100 m–upper limit)
  - Replicate (1–3)
  - Measurement Type (LOI)
  - Cr (g) — crucible weight
  - Cr + Sed (g) — crucible + sediment weight
  - 105, 400, 480, 950 (g) — sediment weight after ignition at specified temperatures
  - 105 (dry weight), 400, 480, 950 (g) — sediment weight excluding crucible after ignition
  - 105, 400, 480, 950 (g) — loss after ignition
  - 480–105 (g) — loss between 480°C and 105°C
  - %Water, %carbohydrate, %total organic, %carbon, %CO2, wtCaCO3, %CaCO3, %Mineral Residue (dry weight)
- Notes:
  - Some fields indicate NA for not applicable data.
  - Data allow computation of organic carbon content, total organic content, and related composition metrics across sites, habitats, seasons, and scales.

## Quality, Access and References

- Data quality context:
  - LOI-based organic carbon measurement with standardized procedure; methodology and calibration detailed via linked LOI resources.
  - Sampling design enables cross-site and cross-habitat comparisons (mudflat vs saltmarsh) across contrasting sediment types.
- Access points:
  - CSV data format for easy integration into dashboards, analyses, and self-serve exploration.
  - Method references and quality checks available through the linked LOI technique descriptions.
- Use cases:
  - Compare organic carbon content and composition between mudflats and saltmarshes across Essex and Morecambe Bay.
  - Explore effects of habitat type, sediment type, season, site, and spatial scale on OC/LOI metrics.
  - Build data products (e.g., dashboards, reports) to support coastal ecosystem assessments and management decisions.