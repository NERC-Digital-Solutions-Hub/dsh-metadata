# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Study sites, targets, and scope
- Dersingham Bog (52.83° N, 0.48° E) and Brandon Country Park (52.43° N, 0.62° E) as field sites; habitats include bog heathland, heathland, shaded woodland, and fen.
- Target moss species include Aulacomnium palustre, Dicranum scoparium, Sphagnum species (e.g., S. cuspidatum, S. fallax, S. papillosum, S. rubellum), Polytrichum spp., Pleurozium schreberi, and others listed in Table 1.
- Aim to capture moss physiological responses and stable isotope signals to model spatial and temporal climatic signals; link field physiology to palaeoclimate analogues.

## Field work and sampling design
- Fieldwork conducted approximately monthly from April 2017 to September 2018.
- On each visit, three samples per target species (approx. 2 x 2 x 2 cm) were harvested, voucher specimens verified by bryologists, and permissions obtained from landowners/managers.
- Sampling included selecting species representing diverse moss lifeforms and growing conditions to enable comparable analogues for palaeoclimate work.

## In-field measurements and physiological assessments
- Chlorophyll fluorescence measurements using Walz MINI-PAM II conducted at moss tips.
- Procedure: three field measurements per sample, followed by at least 30 minutes of dark adaptation, then three additional dark measurements.
- Calculated parameters:
  - Fluorescence yield in dark (Φ) and light
  - Non-photochemical quenching (NPQ)
  - Electron transport rate (ETR) = 0.84 × PAR × 0.5 × Φ (units μmol electrons m⁻² s⁻¹)
- Replicates averaged to produce mean and standard error.

## Water content and carbohydrate analyses
- Water content: approx. 0.3 g sample dried to constant mass at 70°C to compute field relative water content (RWC) = (Fresh − Dry) / Dry.
- Post-drying, cellulose extraction performed on samples via Soxhlet (per Loader et al. 1997) to obtain α-cellulose.
- Fresh water samples collected at each site; atmospheric precipitation collected near the field area (Ely, UK).
- Enzymatic photo-spectrophotometric sucrose content analyses performed on selected fresh moss samples (Stitt et al. 1989).

## Isotope analysis (stable isotopes)
- Water samples and moss-derived distillates analyzed for D/H (δD) and 18O/16O (δ18O) by IRMS.
- Analytical workflow:
  - Filtration through glass wool; duplicate runs.
  - δD: reduction with Chromate on a Vario PyroCube EA; measured on Isoprime100 IRMS.
  - δ18O: pyrolysis on VarioPyroCube EA; measured on Isoprime100 IRMS.
- Standards and calibrations:
  - Standards: VSMOW2 (IAEA), Low Water (Elemental Microanalysis), LEC TAP (in-house), traceable to VSMOW-GISP.
  - δD precision ±1‰; δ18O precision ±0.5‰.
  - Oxygen isotopes calibrated to V-SMOW via IAEA inter-lab standards; precision better than 0.4‰.
- Additional carbon and oxygen isotope analyses performed at the Godwin Laboratory (Cambridge) using EA-IRMS setups with standard calibrations; carbon isotope precision better than 0.1‰.

## Datasets and data structure
- Four CSV datasets provided:
  1) Royles_Field_data_by_time
  2) Royles_RWC_and_Isotope_data
  3) Royles_Sample_Number_Key
  4) Royles_Water_Samples
- Content highlights:
  - Field data fields include sample type, RWC, C13, O18, location, species, session/date, and descriptive notes.
  - RWC and isotopic data include sample-cellulose reference numbers, weights (wet/dry), dry/tube specifics, isotope ratios (δ13C, δ18O, δD), and sample metadata.
  - Sample numbering key links sample references to dates, locations, species, herbarium information, and collection details.
  - Water samples document collection dates, locations, water type, source, and isotope values (δ18O and δD) with notes on missing data due to vial breakage or sample volume.
- Data management practices:
  - Data collected monthly with clear provenance, specimen verification, and metadata to support reproducibility and discoverability.
  - Datasets are linked to standard references and field/lab protocols to facilitate re-analysis and integration with other studies.

## Methods and references
- Field sampling and measurement protocols aligned with established practices for moss physiology and stable isotope work.
- References cited for methodological steps include:
  - Loader et al. 1997: cellulose extraction technique
  - Stitt et al. 1989: enzymatic pigment/metabolite analyses
  - West et al. 2006: water extraction times for stable isotope analysis
- Data collection and analysis emphasize traceable standards, duplicate measurements, calibration to international isotope scales, and transparent documentation of methods and metadata.