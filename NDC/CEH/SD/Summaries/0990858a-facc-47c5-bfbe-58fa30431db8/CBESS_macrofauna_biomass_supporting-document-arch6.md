# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal biomass in mudflat and saltmarsh habitats..

- Purpose and scope
  - A CBESS dataset recording macrofaunal biomass (grams per square meter) in mudflat and saltmarsh habitats across six sites in two locations.
  - Covers winter and summer 2013 field campaigns with three replicates across 22 quadrats, at four spatial scales.
  - Aims to support understanding of biodiversity and ecosystem service sustainability, enabling cross-site and habitat comparisons.

- Spatial and habitat coverage
  - Locations:
    - Essex, UK: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
    - Morecambe Bay, UK: Cartmel Sands (CS), Warton Sands (WS)
  - Habitat types: Mudflat (MF) and Saltmarsh (SM)
  - Salinity- and sediment-context: Essex saltmarsh with clay soils; Morecambe saltmarsh with sandy soils; Essex mudflat with cohesive clays/mud/silt; Morecambe mudflat with coarser sediments
  - Site coordinates provided for all locations

- Sampling design and workflow
  - Sampling rounds: winter and summer 2013
  - Replication: 3 replicates per quadrat; 22 quadrats per site
  - Spatial scales: four scales (A–D) representing progressively larger areas (1 m to 100+ m)
  - Quadrat-level sampling: 3 cylindrical cores per quadrat (10 cm depth, 10 cm diameter)

- Field and laboratory procedures
  - Field: cores fixed in 4% buffered formalin in seawater; residues kept in 70% IMS
  - Processing: organisms identified to species level (or grouped as major debris when damaged)
  - Biomass measurement: biomass of each taxon determined by weighing individuals to 0.0001 g after blotting; if too light, a minimum weight of 0.0001 g recorded
  - Conversion: biomass values converted to g/m^2 using a fixed multiplier (127.323955)
  - Quality control: data entered by two people and double-checked; biomass cross-validated against CBESS_macrofauna_abundance.csv; species names checked against WoRMS

- Data structure and formats
  - File format: CSV
  - Core fields (example list):
    - Season: Winter (W) or Summer (S)
    - Location: Morecambe (M) or Essex (E)
    - Site: Morecambe CS/WS; West Plain (WP); Essex AH/FW/TM
    - Habitat: Mudflat (MF) or Saltmarsh (SM)
    - Quadrat Number: 1–22
    - Scale: A, B, C, D corresponding to progressively larger spatial extents
    - Replicate: 1–3
    - Measurement Type: Macrofauna
  - Taxa data: biomass measurements provided for numerous species (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, Mya arenaria, Mytilus edulis juv., etc.), plus records for various taxa groups and major debris
  - Dataset field descriptions: include row-level metadata (row number, season, location, site, habitat, quadrat, scale, replicate) and per-taxon biomass fields

- Related data and provenance
  - Staff: Christina Wood and Martin Solan
  - Related dataset: CBESS_macrofauna_abundance.csv (abundance data for cross-checking)
  - Taxonomic validation: species names cross-checked against the World Register of Marine Species (WoRMS)

- Intended uses and limitations
  - Suitable for analyses of spatial and seasonal variation in macrofaunal biomass, habitat-type effects, and site-level comparisons
  - Supports data-driven dashboards and self-serve exploration of biomass distributions
  - Limitations: cross-sectional snapshot for 2013 (no planned repeat sampling beyond this campaign); biomass values rely on a fixed conversion factor; taxa coverage is extensive but not necessarily exhaustive of all present organisms