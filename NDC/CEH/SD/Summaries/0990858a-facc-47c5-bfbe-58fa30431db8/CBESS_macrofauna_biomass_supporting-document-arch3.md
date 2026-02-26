# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal biomass in mudflat and saltmarsh habitats.

- Purpose and scope
  - Provides macrofaunal biomass (grams per square meter) as an indicator of coastal biodiversity and ecosystem service sustainability.
  - Part of the CBESS program; dataset covers 6 sites across 2 locations, with 2 habitat types per site.
  - Sampling occurred in winter and summer 2013, with 3 replicates across 22 quadrats at 4 spatial scales; no planned repeat sampling.

- Study sites and habitats
  - Locations: Essex and Morecambe Bay.
  - Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
  - Habitats: Mudflat and Saltmarsh.
  - Habitat and site differences describe sediment types (clay in Essex; sandy sediments in Morecambe Bay) and broader ecological context (inundation frequency, creek structure, vegetation).

- Sampling and laboratory methods
  - Field sampling: at each quadrat, three cylindrical cores (10 cm depth and diameter) collected.
  - Preservation and processing: cores fixed in 4% buffered formalin in seawater, sieved through 0.5 mm mesh, residue preserved in 70% Industrial Methylated Spirit (IMS).
  - Identification and counting: organisms identified to species level (or major group debris when damaged), stored in IMS.
  - Biomass measurement: individuals blotted to remove excess IMS, weighed to 0.0001 g; biomass values converted to g per m² using a factor of 127.323955 and rounded to 0.0001 g.
  - Quality control: data entered by two people and double-checked; biomass data cross-checked with accompanying abundance data (CBESS_macrofauna_abundance.csv); species names validated against WoRMS (World Register of Marine Species).

- Variables and data structure
  - Primary variable: biomass of each taxon (g per m²); includes a long list of species (e.g., Arenicola marina, Hediste diversicolor, Macoma balthica, Mytilus edulis juveniles, etc.) and major debris categories.
  - Dataset fields and organization: Row Number, Season (Winter/W), Location (Morecambe or Essex), Site (e.g., CS, WS, AH, FW, TM), Habitat (Mudflat or Saltmarsh), Quadrat Number (1–22), Scale (1 m, 1–10 m, 10–100 m, etc.), Replicate (1–3), Measurement Type (Macrofauna), and taxa-specific biomass columns.
  - Additional data: a separate abundance dataset is provided (CBESS_macrofauna_abundance.csv); metadata includes explicit descriptions for each field (e.g., Season, Location, Site, Habitat, Scale, Replicate).

- Data quality, governance, and formats
  - Data quality: validation through dual data entry and cross-checks with abundance dataset; species names validated against an authoritative taxonomy source.
  - Data provenance: detailed methodological notes on sampling, processing, and conversion to biomass; explicit quality control steps documented.
  - Data formats and accessibility: data provided in CSV format; extensive field descriptions included to support re-use and comparability.

- Relevance for monitoring frameworks
  - Provides a structured, repeatable method for estimating macrofaunal biomass as an indicator of ecosystem health and service provision across contrasting habitats and locations.
  - Demonstrates rigorous QA processes, metadata completeness, and clear data processing steps, aligning with monitoring governance needs.
  - Highlights practical considerations for data sharing and reuse (e.g., potential barriers to publicly sharing underlying datasets, the necessity of metadata and provenance to enable policy-relevant analyses).
  - Note on limitations: no planned repeats beyond 2013 campaign, which may affect temporal trend assessments; links to separate abundance data help contextualize biomass.