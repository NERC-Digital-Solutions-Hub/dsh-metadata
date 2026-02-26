# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) individual bioturbation potential in mudflat and saltmarsh habitats.

## Overview
- A CBESS dataset measuring individual bioturbation potential (BPi) across coastal mudflat and saltmarsh habitats.
- Collected from 6 sites over 2 locations (Essex and Morecambe Bay) during winter and summer 2013.
- Sampling involved 3 replicates across 22 quadrats at 4 spatial scales, covering two habitats per site.
- Data produced: per-species BPi values, abundances, and biomasses to enable habitat- and species-level bioturbation assessments.
- Staff responsible: Christina Wood and Martin Solan.

## Dataset scope and geography
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
- Habitat types:
  - Mudflat (Essex) and saltmarsh (both regions), with contrasting sediment types (clay in Essex; sandy sediments in Morecambe Bay)
- Context: Essex saltmarsh and Morecambe saltmarsh regions differ in inundation frequency, creek structure, and vegetation; mudflats differ in sediment cohesion and mobility.

## Sampling design and procedures
- Campaign: CBESS field campaign conducted in winter and summer 2013.
- Design: 3 replicates per quadrat across 22 quadrats, at 4 spatial scales.
- Core sampling: three cylindrical sediment cores (10 cm depth, fixed in 4% buffered formalin in seawater) per quadrat.
- Processing: cores sieved (3 mm or 0.5 mm mesh as stated), organisms identified to species or appropriate taxon, counted and weighed.
- Biomass/mass conversion: biomass per taxon converted and standardized; abundance data scaled to per square meter using a conversion factor (127.323955).
- Output: Bioturbation potential per individual (BPi) and per-m^2 (BPc) values.

## Variables, calculations, and data structure
- Primary measurement: BPi (bioturbation potential per individual); BPc = sum of BPp across species per m^2, where BPp = BPi × Ai (Ai = species abundance per m^2).
- Formulae used:
  - BPi = (√Bi) × Mi × Ri
  - BPc = Σ BPp of all species per m^2
  - BPp = BPi × Ai
- Observed taxa include a long list of invertebrates (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Cerastoderma edule, etc.) and other groups.
- Data fields include season (Winter W, Summer S), location (Morecambe M, Essex E), specific sites, habitat type, quadrat number (1–22), scale (A–D), and per-species BPi values.
- File format: .csv
- Data notes: “NA” indicates no data; row numbers provide original input order.

## Data collection quality and provenance
- Data entry: raw data input by two people with double-checks; biomass values cross-validated against abundance data.
- Calculations for BPi and BPc checked and verified.
- Documentation of procedures and variables is included to support reproducibility.

## Metadata, accessibility, and data structure
- Detailed dataset field descriptions are provided (season, location, site, habitat, scale, measurement type, and per-species BPi values).
- Summary rows and species-specific columns enable cross-site comparisons and aggregation.
- The dataset is designed for integration with broader CBESS data assets and supports assessments of data quality, discoverability, and reuse.

## Reuse, governance, and implications for Data Leaders
- Use cases: cross-site comparison of bioturbation potential to inform coastal ecosystem function and service assessments; integration with ecosystem service models; policy and management planning.
- Governance considerations:
  - Clear provenance (staff, sites, habitats, sampling periods) supports accountability and traceability.
  - Comprehensive metadata enables discoverability and reuse across networks.
  - No planned repeats beyond 2013 sampling; users should account for temporal limitations when integrating with ongoing data streams.
  - Data quality controls (double data entry, cross-checks) support reliability for decision-making.
  - Potential need for harmonization if combined with other CBESS datasets or future data to maintain consistency in measurement units and scaling.