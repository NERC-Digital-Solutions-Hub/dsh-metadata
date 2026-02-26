# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Aim
- Investigate moss physiology and stable isotope ecology to model spatial and temporal climatic signals.
- Combine field-based chlorophyll fluorescence measurements with stable isotope and related biochemical analyses.

## Study sites and target taxa
- Dersingham Bog (approx. 52.83° N, 0.48° E) and additional sites: Brandon Country Park (52.43° N, 0.62° E) and Wicken Fen.
- Target species representing a range of moss lifeforms and habitats (e.g., Aulacomnium palustre, Dicranum scoparium, Sphagnum spp., Pleurozium schreberi, Polytrichastum formosum, Calliergonella cuspidate, Kindbergia praelonga), across bog heathland, heathland, fen, and shaded woodland.

## Field methodology
- Fieldwork conducted approximately monthly from April 2017 to September 2018.
- On each visit: identify target species, collect three samples per species (≈2×2×2 cm) and seal for transport.
- Chlorophyll fluorescence measurements using Walz MINI-PAM II:
  - In-field measurements: F, Fm, PAR, ETR; three measurements per sample.
  - Dark adaptation: at least 30 minutes, then three additional measurements (F', Fm').
  - Calculations: fluorescence yield in dark (Fm−F)/Fm, in light (Fm'−F')/Fm', non-photochemical quenching (Fm−Fm')/Fm, and electron transport rate 0.84×PAR×0.5×Φ (μmol electrons m⁻² s⁻¹).
  - Report means and standard errors.
- Water content: fresh mass weighed, then dried at 70°C to determine relative water content (RWC = (Fresh−Dry)/Dry).
- Chemical processing:
  - Dry moss → cellulose extraction (standard method; Loader et al. 1997).
  - Fresh moss → water extraction by cryogenic vacuum distillation (West et al. 2006).
- Environmental measurements:
  - Fresh water samples collected at each site; precipitation collected near the central field area (Ely, UK).
  - Enzymatic photo-spectrophotometric sucrose analysis on a subsample (Stitt et al. 1989).
- Sample handling and documentation:
  - Voucher specimens verified by bryologists ( Preston, Hill).
  - Landowner/manager permissions obtained prior to field work.

## Dataset and data processing
- Dataset composition: 14 monthly sequential CSV files (01 Jul 2017 to 14 Oct 2018).
- Structure: 18 columns per record (units and descriptions provided per column).
- Key data fields include:
  - Session (collection session number), Date (collection date), Site, Species, Sample, Notes.
  - Physiological measurements: F, Fm, Dark_Y, Field_F, Field_Fm, Field_PAR, Field_Y, Field_ETR, Field_NP.
  - Derived metrics: Φ (quantum yield in dark), Field_Y (field yield), Field_NP (non-photochemical parameter), ETR.
  - Water and chemical data: RWC (relative water content), Cellulose (reference and measurements), Value (mean/SE).
- Data provenance and references:
  - Cellulose processing: Loader et al. 1997.
  - Metabolite and plant physiology methods: Stitt et al. 1989; West et al. 2006.
- Data quality and usability:
  - Mean and SE values reported for replicated measurements.
  - Extensive metadata for reproducibility and discoverability, including site, species, sampling date, and methodological references.

## Notes on scope and context
- The study integrates physiological measurements with stable isotope ecology to inform climate-related models using moss proxies.
- Field measurements are designed to capture spatial and temporal variation across multiple moss lifeforms and habitats, with careful documentation and verifiable specimen identity.