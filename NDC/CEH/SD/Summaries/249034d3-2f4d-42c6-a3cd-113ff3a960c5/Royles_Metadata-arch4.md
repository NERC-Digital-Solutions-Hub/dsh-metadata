# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

- Overview
  - Study of moss physiology and stable isotope ecology to model spatial and temporal climatic signals.
  - Dataset comprises monthly field measurements and dark-adapted PAM fluorescence measurements.

- Field sites, habitats, and target organisms
  - Dersingham Bog (52.83° N, 0.48° E)
    - Habitat: Bog heathland
    - Target species include Aulacomnium palustre, Dicranum scoparium, several Sphagnum species (cuspidatum, fallax, papillosum, rubellum), Polytrichum, and other mosses.
  - Brandon Country Park (52.43° N, 0.62° E)
    - Habitat: Heathland
    - Target species include Pleurozium schreberi, Polytrichastum formosum, others.
  - Wicken Fen (52.31° N, 0.29° E)
    - Habitat: Shaded woodland / fen
    - Target species include Brachythecium rutabulum, Calliergonella cuspidate, Kindbergia praelonga, among others.
  - Voucher specimens collected and identity verified by bryologists (Preston, C. D.; Hill, M. O.).

- Fieldwork design and logistics
  - Field work conducted approximately monthly from April 2017 to September 2018.
  - Permissions obtained from land owners/managers prior to field work.
  - On each visit, three 2 x 2 x 2 cm samples per target species were harvested for analysis.

- In-field measurements and numerical calculations
  - Chlorophyll fluorescence measurements with Walz MINI-PAM II:
    - In-field: F, Fm, PAR, ETR measured at moss tips (three measurements per sample).
    - Post-field dark adaptation: samples dark-adapted for at least 30 minutes; three additional measurements (F', Fm').
  - Derived metrics:
    - Fluorescence yield in the dark: (Fm - F) / Fm
    - Fluorescence yield in the light: (Fm' - F') / Fm'
    - Non-photochemical quenching (NPQ): (Fm - Fm') / Fm
    - Electron transport rate (ETR): 0.84 * PAR * 0.5 * Φ, with units μmol electrons m^-2 s^-1
  - Water content and tissue properties:
    - Relative water content (RWC): calculated from fresh weight and dry weight after drying to constant mass at 70°C
      - RWC = (Fresh weight - Dry weight) / Dry weight
      - Expressed as proportion of dry mass
  - Additional lab analyses:
    - Cellulose extraction from dried moss (Soxhlet extraction; standardized method)
    - Cryogenic vacuum distillation for extraction of water from moss tissue
    - Fresh water samples collected at each field site; precipitation collected in Ely (52.40° N, 0.26° E)
    - Enzymatic photometric analysis of sucrose content in selected fresh moss samples (Stitt et al. 1989)

- Dataset structure and contents
  - 14 monthly sequential CSV files spanning 01 Jul 2017 to 14 Oct 2018
  - 18 data columns per record, with two-part metadata per field (unit and description)
    - Core fields include: Session (collection session number), Date (collection date), Site (collection location), Species (collection species), Notes
    - Physiological measurements: F, Fm, Dark_Y, Field_F, Field_Fm, Field_PAR Field_Y (PAR in field), Field_ETR Field_NP (ETR/NPQ related), etc.
    - Tissue and chemical measurements: Cellulose (reference number for cellulose collection), RWC (relative water content), and Value (mean or SE)
    - Sample identifiers: Sample (collection number)
  - Purposeful data organization to support discoverability and re-use:
    - Units and descriptions accompany each variable
    - Links to field and laboratory workflows (in-field measurements, dark adaptation, lab analyses)
  - Data quality notes:
    - Triplicate in-field measurements with reported mean and SE
    - Alignment with standard procedures for cellulose extraction and stable isotope workflows
  - Provenance and references:
    - Field measurements tied to voucher specimens and verified identifications
    - References provided for standard methods used (Loader et al. 1997; Stitt et al. 1989; West et al. 2006)

- Data governance, provenance, and ethics
  - Specimens voucher-verified by bryologists; authorship acknowledged (Preston, Hill)
  - Permissions obtained from landowners/managers prior to field work
  - Clear documentation of sample collection, handling, and site-specific context (habitat and coordinates)

- Standards, references, and methodological context
  - In-field PAM fluorescence methodology and calculations (F, Fm, F', Fm', Φ, NPQ, ETR)
  - Stable isotope and water extraction workflows referenced (cryogenic distillation; cellulose reference methods)
  - Cited methodological sources:
    - Loader et al. 1997 (cellulose processing)
    - Stitt et al. 1989 (metabolite measurement protocols)
    - West et al. 2006 (water extraction times for stable isotope analysis)

- Use cases and potential benefits for data leadership
  - Enables modeling of spatial and temporal climatic signals using moss physiology and water relations
  - Provides a structured, multi-site, multi-species dataset with robust metadata for cross-site comparisons
  - Demonstrates end-to-end data stewardship from field collection to lab analyses and final dataset assembly
  - Supports reuse in data ecosystems requiring clear provenance, quality indicators (means/SE), and standardized metadata for complex ecological datasets