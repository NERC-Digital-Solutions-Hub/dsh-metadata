# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) individual bioturbation potential in mudflat and saltmarsh habitats..

- Purpose and scope
  - Provides individual bioturbation potential (BPi) data for CBESS across mudflat and saltmarsh habitats.
  - Derived from data at 6 sites over 2 locations (Essex and Morecambe Bay), sampled in winter and summer 2013.
  - Three replicates across 22 quadrats, spanning four spatial scales.
  - Staff responsible: Christina Wood and Martin Solan.
  - Focused on abundance and biomass of infaunal taxa to compute BPi and related metrics.

- Locations and site descriptions
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS).
  - Site and habitat context include contrasting sediment types and soil types (Essex saltmarsh with clay soils; Morecambe Bay saltmarsh with sandy soils) and differing inundation, creek structure, and vegetation. Mudflat sites differ (Essex: cohesive clays, mud, silt; Morecambe: coarse, mobile sediments).

- Sampling design and timing
  - General CBESS field campaign conducted in winter and summer 2013.
  - No planned repeat sampling.

- Data collected and observed variables
  - Core data: abundance and biomass of individual taxa to calculate BPi.
  - Measured taxonomic groups listed (numerous species and higher taxa), with BPi values assigned per species.
  - Variables include species-specific counts and biomass per replicate, later aggregated to per square meter (m^2).

- Laboratory procedures and data processing
  - Sampling: three cylindrical sediment cores (10 cm depth, 10 cm diameter) per quadrat; fixed in 4% buffered formalin in seawater.
  - Processing: cores sieved with 0.5 mm mesh; organisms identified to species or appropriate taxon; abundance counted; biomass weighed to 0.0001 g precision.
  - Data handling: specimens damaged or partial noted; biomass data checked against abundance data (from CBESS_macrofauna_abundance.csv).
  - Conversion and calculations: abundance and biomass scaled by factor 127.323955 to yield per m^2 values; BPi computed as BPi = sqrt(Bi) × Mi × Ri, where Bi = biomass, Mi = mobility, Ri = reworking.
  - Derived metrics: BPc (sum of BPp per m^2) where BPp = BPi × Ai (Ai = individual species abundance per m^2).
  - Quality controls: raw data input by two people and double-checked; calculations independently verified.

- Data formats and documentation
  - File format: CSV.
  - Dataset includes a comprehensive field description section, detailing:
    - Row Number (sorting index)
    - Season (Winter W or Summer S)
    - Location (Morecambe M or Essex E)
    - Site (specific site codes)
    - Habitat (Mudflat MF or Saltmarsh SM)
    - Quadrat Number (1–22)
    - Scale (A-D representing spatial scales)
    - Measurement Type (BPi per individual)
    - Species-specific BPi values and counts (e.g., Arenicola marina, Ampharete spp., etc.)

- Data accessibility and reuse considerations
  - Dataset is provided as CSV with explicit methodological and field descriptions to support reuse and replication.
  - Methods and formulas are clearly documented, enabling calculation checks and cross-study comparability.
  - No explicit update plan beyond the stated sampling; currently no planned repeats.

- Governance, provenance, and quality assurance
  - Clear attribution of staff and field campaign timing.
  - Documentation of sampling methods, laboratory processing, and data validation steps.
  - Metadata includes site and habitat context to aid discoverability and interoperability across CBESS datasets.

- Practical considerations for data stewards
  - Ensuring dataset discoverability via portal/catalog entries with the described metadata.
  - Maintaining traceable provenance: link to field campaign year (2013), sites, habitats, and processing workflow.
  - Representing derived metrics (BPi and BPc) with explicit calculation formulas and units.
  - Acknowledging that updates are unlikely unless new sampling occurs; plan for versioning if updated.