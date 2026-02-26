# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal abundance in mudflat and saltmarsh habitats..

- Overview
  - A macrofaunal abundance dataset (individuals per square metre) collected from mudflat and saltmarsh habitats as part of the CBESS program.
  - Aimed at supporting environmental health monitoring, assessment, and informing future decisions.

- Study design and locations
  - 6 sites across 2 locations: Essex and Morecambe Bay.
  - Each location includes two habitat types: mudflat and saltmarsh.
  - Seasonal sampling during winter and summer 2013; no planned repeat sampling.
  - Sampling framework includes 3 replicates across 22 quadrats, at 4 spatial scales.

- Habitat and site details
  - Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
  - Saltmarsh contrasts: clay soils in Essex vs sandy soils in Morecambe Bay; differing inundation frequency, creek structure, and vegetation.
  - Mudflat contrasts: Essex mudflats with cohesive clays, mud, and silt vs Morecambe mudflats dominated by coarse, mobile sediments.

- Data collection and processing
  - Primary variable: species abundance (number of individuals) per square metre.
  - Field sampling: three cylindrical cores per quadrat (10 cm depth, 10 cm diameter).
  - Specimens fixed in 4% buffered formalin in seawater, sieved (0.5 mm), preserved in 70% IMS.
  - Species identification to species level where possible; abundance determined from intact heads or debris separated as presence/absence for debris categories.
  - Abundance conversion: counts multiplied by 127.323955 to yield per m² values.
  - Quality control: two-person data entry with double-checking; cross-check with CBESS_macrofauna_biomass.csv to ensure consistency; species names validated against WoRMS.

- Data structure and metadata
  - File format: CSV.
  - Core data fields include: Row Number, Season (Winter W, Summer S), Location (Morecambe M, Essex E), Site (CS, WS, WP; AH, FW, TM), Habitat (Mudflat MF, Saltmarsh SM), Quadrat Number (1–22), Scale (A: 1 m, B: 1–10 m, D: 10–100 m and beyond), Replicate, Measurement Type (Maf for Macrofauna), plus abundance records for numerous species and presence/absence for debris categories.
  - Extensive species list with abundances for key polychaetes, molluscs, crustaceans, and various debris categories; includes ecological and taxonomic notes like Arenicola marina, Hydrobia ulvae, Macoma balthica, Crangon crangon, among others.
  - Supplementary data: a detailed field-description mapping for many coded variables (e.g., Season, Location, Site, Habitat, Quadrats, Scales, Replicate, Measurement Type, and numerous species entries).

- Data quality, standards, and governance
  - Calibration and statistical treatment fields are marked NA, indicating limited or no calibration procedures documented within this record.
  - Data quality is supported by explicit QC steps and cross-validation with biomass data and taxonomic verification.
  - Data sharing: the record notes openness and data governance considerations (reliant on public sharing of underlying data and appropriate data management), but explicit access terms are not detailed here.
  - Metadata completeness: robust core metadata provided, with some fields NA for calibration/statistical treatment.

- Relevance to monitoring frameworks
  - Demonstrates practical development of a standardized, replicable monitoring dataset across multiple sites and habitat types.
  - Highlights the importance of metadata clarity (units, scales, coding schemes) and QA/QC processes for trustworthy indicators.
  - Shows integration with existing data (biomass cross-check) and taxonomic validation (WoRMS), underscoring data provenance and interoperability.
  - Illustrates potential data governance barriers (data sharing constraints, metadata completeness in some areas) that monitoring framework authors must address to enable timely access and reuse.

- Notes for further use
  - No planned repeat sampling suggests this dataset captures a specific temporal snapshot; future monitoring could benefit from explicit repeat design.
  - The dataset provides a comprehensive species-centric abundance framework suitable for assessing coastal biodiversity and ecosystem service implications, with clearly defined habitat contrasts and environmental drivers.