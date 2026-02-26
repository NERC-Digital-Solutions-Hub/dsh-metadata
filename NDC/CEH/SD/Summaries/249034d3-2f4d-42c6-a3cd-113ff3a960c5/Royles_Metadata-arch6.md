# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Overview
- Study of moss physiology and stable isotope ecology to model spatial and temporal climatic signals.
- Fieldwork conducted monthly from April 2017 to September 2018 across multiple sites in the UK (Dersingham Bog, Brandon Country Park, Wicken Fen).
- Targeted moss species selected to represent a range of lifeforms and ecological conditions; specimens voucher-identified and verified by bryologists.
- Data generated include in-field chlorophyll fluorescence measurements, water content data, cellulose extraction, and water/precipitation sampling, culminating in a structured multi-site dataset for analysis and data products.

## Field sites and sampling
- Sites: Dersingham Bog (multiple coordinates), Brandon Country Park, Wicken Fen.
- Target species: diverse moss taxa including Aulacomnium palustre, Dicranum scoparium, Sphagnum spp., Pleurozium schreberi, Polytrichum spp., and others; site- and species-specific notes recorded.
- Sampling cadence: approximately monthly between April 2017 and September 2018.
- Sampling protocol: on each visit, three samples (each around 2 x 2 x 2 cm) per target species; samples bagged for transport.
- Permissions: permissions obtained from landowners/managers prior to fieldwork.
- Voucher specimens: collected and identity verified by experienced bryologists; linked to Table 1 (target species and locations).

## Measurements and methods
- In-field chlorophyll fluorescence (Walz MINI-PAM II):
  - Measurements: F (instantaneous fluorescence after dark adaptation), Fm (maximum fluorescence after saturating pulse following dark adaptation), PAR, and ETR.
  - Three measurements per sample in the field; samples dark-adapted for at least 30 minutes followed by three additional measurements in the dark.
  - Calculations:
    - Φ (quantum yield in the dark) = (Fm − F) / Fm
    - Φ (light) = (Fm′ − F′) / Fm′
    - Non-photochemical quenching (NPQ) = (Fm − Fm′) / Fm
    - Electron transport rate (ETR) = 0.84 × PAR × 0.5 × Φ (units μmol electrons m⁻² s⁻¹)
- Water content data:
  - Fresh mass ~0.3 g of each sample weighed; dried to constant mass at 70°C to determine field relative water content (RWC = (Fresh − Dry) / Dry).
  - Dry moss subjected to cellulose extraction via standard batch-processing methods.
  - Water extraction: fresh moss portion placed in sealed vials for extraction of water by cryogenic vacuum distillation.
  - Fresh water samples collected at each field site; precipitation collected at Ely (central field area).
- Additional analyses:
  - Enzymatic photo-spectrophotometric sucrose content analysis performed on a subset of fresh moss material using standard procedures.

## Data collected
- Field data: chlorophyll fluorescence parameters (F, Fm, F′, Fm′, Field F, Field Fm, Field PAR, Field Y), calculated Φ, NPQ, and Field ETR; instantaneous and field-derived measurements.
- Water content data: field relative water content (RWC) and cellulose extraction results.
- Isotope/chemical data: water extraction results and sucrose content (subset).
- Meteorological/precipitation data: field-site precipitation records (Ely reference).
- Metadata: site coordinates, sampling dates, sample and site identifiers, species identifications, notes on location and context.

## Dataset structure
- Composed of 14 monthly sequential CSV files, spanning 01 Jul 2017 to 14 Oct 2018.
- Each row includes 18 columns with paired fields (Unit/Description, Session/Collection session number, Date/Date of collection, Cellulose/Cellulose reference, RWC/Relative water content, Value/Type (mean/SE), Sample/Sample collection number, Site/Collection location, Species/Collection species, Notes/Notes about location, F/Field fluorescence, Fm/Field maximum fluorescence, Dark_Y/Instantaneous fluorescence in the field, Field_F/Maximum field fluorescence after saturating pulse, Field_Fm/Field condition fluorescence after saturating pulse, Field_PAR/μmol photons m⁻² s⁻¹, Field_Y Field-derived PAR-based metric, Field_ETR/NP/ETR calculation and related metrics).
- Data references and provenance include standard methodologies for cellulose extraction and metabolite/isotope analyses (Loader et al. 1997; Stitt et al. 1989; West et al. 2006).

## Data processing and calculations
- Per-sample statistics: three field measurements per sample; mean and standard error (SE) calculated for each sample.
- Calculations implemented to derive key physiological metrics:
  - Dark yield Φ = (Fm − F) / Fm
  - Light yield Φ = (Fm′ − F′) / Fm′
  - Non-photochemical quenching NPQ = (Fm − Fm′) / Fm
  - Electron transport rate ETR = 0.84 × PAR × 0.5 × Φ
- Relative water content (RWC) computed as described; cellulose extraction and water extraction performed using established protocols.
- Data include both immediate field values and derived metrics to enable self-service analysis and visualization.

## Quality, provenance and references
- Voucher specimens verified by experienced bryologists to ensure taxonomic accuracy.
- Field sampling and measurement protocols aligned with established methods; data linked to published references for cellulose extraction, metabolite analysis, and water/isotope methodologies.
- Field permissions obtained from landowners/managers; clear documentation of collection sites and dates to support reproducibility and re-use.

## Potential uses for data consumers
- Build self-serve dashboards and data products to explore moss physiology across space and time and its relation to climatic signals.
- Integrate physiological metrics with isotope and moisture data to model spatial-temporal climatic signals using moss proxies.
- Reuse the dataset structure to join with other site-based environmental datasets, enabling cross-site comparisons and palaeoclimate analogue studies.
- Support methodological transparency by providing access to field protocols, measurement calculations, and data lineage.