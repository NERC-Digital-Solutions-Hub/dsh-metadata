# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

- Purpose and scope
  - Investigates moss physiology and stable isotope ecology to model spatial and temporal climatic signals.
  - Combines monthly field measurements with dark-adapted PAM fluorescence to assess photosynthetic responses.

- Field sites, species, and sampling design
  - Field sites: Dersingham Bog (bog heathland), Brandon Country Park (heathland), Wicken Fen (fen; shaded woodland) with specific coordinates provided.
  - Target taxa include multiple moss species (e.g., Sphagnum spp., Dicranum scoparium, Pleurozium schreberi, Polytrichum spp.) across varied habitat types.
  - Field work conducted approximately monthly from April 2017 to September 2018.
  - Voucher specimens collected and identities verified by bryologists; permissions obtained from landowners/managers before fieldwork.
  - On each visit, three samples per target species (roughly 2 x 2 x 2 cm) were harvested per site.

- Measurements in the field and laboratory analyses
  - Chlorophyll fluorescence (in moss growing tips) using Walz MINI-PAM II; measurements include:
    - In field: F, Fm, PAR, ETR
    - In dark-adapted state: F', Fm'
    - Calculations: fluorescence yield in dark and light, non-photochemical quenching (NPQ), electron transport rate (ETR = 0.84 × PAR × 0.5 × Φ)
  - Water content data:
    - Fresh samples weighed; dried to constant weight at 70°C to compute relative water content (RWC = (Fresh – Dry) / Dry).
  - Biochemical analyses:
    - Cellulose extraction following Loader et al. (1997).
    - Water extraction by cryogenic vacuum distillation (West et al. 2006).
    - Enzymatic sucrose content analysis on select fresh moss samples (Stitt et al. 1989).
  - Auxiliary samples:
    - Fresh water collected at each field site; precipitation collected near the study area center (Ely, UK).

- Dataset structure and contents
  - 14 monthly csv files spanning 01 Jul 2017 to 14 Oct 2018.
  - 18 columns with descriptors including:
    - Session, Date, Site, Species, Sample, Notes
    - Physiological measures: F, Fm, Field_F, Field_Fm, Field_PAR, Field_Y, Field_ETR, Field_NP
    - Water-related: RWC, Cellulose (with reference), and related metadata
    - Value type indicators (mean / SE) and unit descriptions
  - Data provenance notes:
    - Field measurements repeated thrice per sample; mean and SE calculated.
    - Measurements and calculations follow established methods (e.g., fluorescence yield Fm–F/Fm, (Fm' – F')/Fm', etc.).
    - References incorporated for laboratory methods:
      - Loader et al. 1997 for cellulose batch processing
      - Stitt et al. 1989 for metabolite analysis
      - West et al. 2006 for plant/soil water extraction times

- Data quality, provenance, and governance considerations
  - Identities validated by experienced bryologists; voucher specimens retained or documented.
  - Use of standardized instruments (Walz MINI-PAM II) and established procedures enhances comparability.
  - Metadata-rich dataset with explicit column descriptions and field notes supports traceability and reuse.
  - Landowner/manager permissions secured prior to collection, underscoring compliance with governance requirements.
  - Data derived from field-collected samples and laboratory analyses designed to support modelling of climatic signals and moss physiology.

- Relevance for monitoring frameworks and policy evaluation
  - Provides a structured, multi-site dataset linking moss physiological responses (photosynthetic efficiency, water status) to environmental conditions across time.
  - Supports modelling of spatial and temporal climatic signals through moss physiology and related biochemical metrics.
  - Can inform environmental health indicators related to ecosystem responses to climate variability (e.g., moisture regime, photosynthetic performance).
  - Demonstrates a comprehensive approach to data collection, standardization, and documentation that aligns with robust monitoring framework practices:
    - clear aims, stakeholder- and expert-informed design
    - data quality assurance and transformation
    - transparent data sharing-ready outputs and governance considerations
  - The methodology and dataset can serve as a reference for designing moss- or bryophyte-based environmental monitoring initiatives and for evaluating policy-relevant climate-ecosystem interactions.