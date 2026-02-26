# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal biomass in mudflat and saltmarsh habitats

- Dataset purpose and scope
  - Macrofaunal biomass (grams per square meter) collected as part of the CBESS program.
  - 6 sites across 2 locations, each with 2 habitat types (mudflat and saltmarsh).
  - Sampling conducted in winter and summer 2013; 3 replicates across 22 quadrats at 4 spatial scales.
  - Taxa and debris enumerated; biomass values recorded for each listed species and major debris group.

- Location and habitat context
  - Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
  - Saltmarsh habitats differ by soil type (clay in Essex; sandy in Morecambe Bay) and by inundation, creek structure, and vegetation; mudflat habitats differ in sediment type (cohesive clays/mud/silt in Essex versus coarse, mobile sediments in Morecambe Bay).

- Methods and data collection
  - Field sampling: 3 cylindrical sediment cores per quadrat (10 cm depth and diameter) fixed in 4% buffered formalin in seawater.
  - Laboratory processing: cores sieved with 0.5 mm mesh; organisms identified to species level where possible, otherwise grouped as major taxa; preserved in 70% IMS.
  - Biomass determination: organisms blotted to remove IMS, weighed to 0.0001 g; anomalies or very light specimens recorded as 0.0001 g; biomass values converted using a factor (multiply by 127.323955) and rounded to 0.0001 g to yield biomass per m^2.
  - Debris and major groups (e.g., annelid, mollusc, crustacea debris) also recorded.

- Data management and quality control
  - Data entry performed by two individuals with double-checking.
  - Biomass data cross-validated against abundance data (CBESS_macrofauna_abundance.csv) to ensure consistency.
  - Species names validated against World Register of Marine Species (WoRMS).

- Data structure and formats
  - Primary file formats: CSV.
  - Dataset fields and structure (example columns):
    - Row Number (sort key)
    - Season (Winter W or Summer S)
    - Location (Morecambe M or Essex E)
    - Site (e.g., CS, WS, AH, FW, TM)
    - Habitat (Mudflat MF or Saltmarsh SM)
    - Quadrat Number (1–22)
    - Scale (A=1m, B/C/D representing 1–10m, 10–100m, etc.)
    - Replicate (1–3)
    - Measurement Type (Maf = Macrofauna)
    - Taxa biomass columns (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, etc.)
    - Debris columns (Annelid debris, Mollusc debris, Crustacea debris)
  - Taxa coverage includes a wide range of annelids, molluscs, crustaceans, copepods, nematodes, and other invertebrates, plus debris categories.

- Data usage, limitations, and stewardship notes
  - Timeframe: data from general CBESS field campaign in 2013; no planned repeats noted.
  - Data interpretation should consider site- and habitat-specific differences in sediment type and inundation regimes.
  - The comprehensive taxa-by-quadrat biomass matrix supports spatial and temporal comparisons, as well as ecosystem-service assessments.
  - Proper data governance requires referencing the two linked CSVs (biomass and abundance) and ensuring taxonomy alignment with WoRMS; maintain provenance to Christina Wood and Martin Solan as staff responsible.

- Practical considerations for data discovery and sharing
  - Ensure metadata clearly maps site codes to locations and habitat types.
  - Maintain conversion factor documentation (127.323955) and unit definitions (g per m^2).
  - Keep alignment between biomass and abundance datasets for reproducible analyses.
  - Note that the dataset represents a finite, non-repeating snapshot from 2013; any future updates should follow the same schema for interoperability.