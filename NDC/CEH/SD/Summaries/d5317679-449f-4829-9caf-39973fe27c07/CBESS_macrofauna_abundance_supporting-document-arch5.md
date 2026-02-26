# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal abundance in mudflat and saltmarsh habitats.

## Overview
- Macrofaunal abundance data collected per square meter (abundance, individuals per m²).
- Study design: 6 sites across 2 locations (Essex and Morecambe Bay) with 2 habitat types each (mudflat and saltmarsh).
- Sampling timeframe: CBESS field campaign conducted in winter and summer 2013.
- Sampling resolution: 3 replicates across 22 quadrats at 4 spatial scales.
- Data processing: abundance counts converted from raw counts using a factor (127.323955) and rounded to the nearest whole individual.
- Staff responsible: Christina Wood and Martin Solan.
- Related dataset: CBESS_macrofauna_biomass.csv for cross-checking biomass.

## Location, habitats and site details
- Essex locations: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay locations: Cartmel Sands (CS), Warton Sands (WS), West plain (WP).
- Habitat descriptions:
  - Saltmarsh with contrasting soil types: clay soils in Essex; sandy soils in Morecambe Bay.
  - Mudflat: Essex sites with cohesive clays, mud and silt; Morecambe mudflats with coarser, more mobile sediments.
- Broader site characteristics also include differences in inundation frequency, creek structure, and dominant vegetation between Essex and Morecambe Bay saltmarsh regions.

## Data collected and variables
- Primary variable: Species abundance (number of individuals) per square meter for listed taxa.
- Taxa monitored include a comprehensive list of macrofauna (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, various Mollusca and Crustacea, among others) with explicit abundance data per taxon.
- Additional recorded categories:
  - Debris: major group debris (annelid, mollusc, crustacea debris) and mollusc debris; presence/absence indicators used.
  - Nematoda, Nemertea, and other groups with presence or abundance records.
- Data fields (structure and codes):
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe (CS, WS, WP) or Essex (AH, FW, TM).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A=1 m; B=1–10 m; Replicate C=10–100 m; D=100+ m.
  - Replicate: codes corresponding to spatial grouping.
  - Measurement Type: Macrofauna (Maf) or related taxon-level abundance.
  - Abundance values: numeric counts for listed species; presence/absence for debris categories.
- Data checks: cross-validated against CBESS_macrofauna_biomass.csv to ensure consistency between abundance and biomass data.
- Taxon verification: species names checked against WoRMS (World Register of Marine Species).

## Data collection, processing and transformation
- Field collection: three cylindrical cores per quadrat (10 cm depth; diameter not specified in summary) collected and fixed in 4% buffered formalin in seawater.
- Laboratory processing: cores sieved with a 0.5 mm mesh; residue examined under a stereo microscope; specimens identified to species level (or appropriate taxon) and stored in 70% IMS.
- Counting method: individuals counted to produce abundance data; damaged specimens assessed by presence of a head or grouped as debris if not identifiable.
- Data conversion: raw counts multiplied by 127.323955 and rounded to the nearest whole number to yield abundance per m².
- Quality checks: two-person data entry with double-checking; cross-check of abundance data against biomass data; species names standardized via WoRMS.

## Data quality and metadata management
- Data entry and compilation involve independent verification by two staff members.
- Consistency ensured by relating abundance data to biomass data file and standard taxonomic nomenclature.
- Metadata include sampling design, locations, habitat types, spatial scale, and coding schemes for fields and categories to support reproducibility and discoverability.

## File formats and structure
- Primary data format: CSV.
- Dataset field descriptions provided (coding for Season, Location, Site, Habitat, Scale, Replicate, Measurement Type, and taxa abundances).
- Related documentation includes a detailed field description table mapping codes to meanings (e.g., Season: W/S; Location: M/E; Site: CS/WS/WP or AH/FW/TM; Habitat: MF/SM; Scale: A/B; Replicate: C/D; and taxa names with Abundance values).

## Data stewardship and usage considerations
- Monitoring status: no planned repeats; dataset reflects a finite CBESS field campaign (winter and summer 2013).
- Publication and reuse readiness: CSV format with explicit field codes and a comprehensive field description to facilitate sharing, integration, and reuse by researchers and data managers.
- Standards and governance: records include standardization of species names, metadata completeness (locations, habitats, seasons, sites, scales), data validation against biomass, and provenance through staff attributions.
- Opportunities for Data Stewards:
  - Maintain alignment with CBESS data standards and ensure ongoing accessibility.
  - Track any updates, re-annotations, or integration with biomass or other CBESS data products.
  - Ensure availability of the related CBESS_macrofauna_biomass.csv for users performing cross-analyses.