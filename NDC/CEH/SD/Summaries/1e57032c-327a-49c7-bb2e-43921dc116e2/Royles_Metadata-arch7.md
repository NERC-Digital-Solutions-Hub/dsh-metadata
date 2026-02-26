# Physiology and stable isotope ecology of moss growth for modelling spatial and temporal climatic signals NERCDMP-555 - monthly field and dark adapted PAM fluorescence measurements

## Overview
- Investigates moss physiology and stable isotopes to model spatial and temporal climatic signals.
- Monthly field work (April 2017 – September 2018) with chlorophyll fluorescence measurements on moss tips using a Walz MINI-PAM II.
- Data intended for map-based analysis and spatial-temporal modelling of climate signals.

## Spatial coverage and study sites
- Dersingham Bog (52.83° N, 0.48° E) — habitats include bog heathland; multiple moss species sampled.
- Brandon Country Park (52.43° N, 0.62° E) — heathland habitat; sampled species listed.
- Wicken Fen (52.31° N, 0.29° E) — shaded woodland and fen habitats; moss species sampled.
- Additional field activities near Ely (precipitation collection center).
- Target species across sites include Aulacomnium palustre, Dicranum scoparium, Sphagnum spp., Pleurozium schreberi, Polytrichum formosum, Brachythecium rutabulum, Calliergonella cuspidate, Kindbergia praelonga and others.

## Sampling framework and measurements (field methods)
- Approximately monthly field visits from April 2017 to September 2018.
- On each visit: three samples per target species; voucher specimens collected and verified by bryologists; permissions obtained from landowners/managers.
- Chlorophyll fluorescence measurements at moss tips:
  - In-field: F, Fm, PAR, ETR; three measurements per sample.
  - Dark adaptation: minimum 30 minutes; three additional measurements (F', Fm').
  - Derived metrics: fluorescence yield Φ (dark and light), non-photochemical quenching (NPQ), ETR calculated as 0.84 × PAR × 0.5 × Φ.
  - Outcome: mean and standard error across three measurements.
- Water content data:
  - Fresh ~0.3 g sample weighed; dried at 70°C to compute field relative water content (RWC = (Fresh − Dry)/Dry).
  - Dry moss subjected to cellulose extraction; fresh moss processed for water extraction by cryogenic vacuum distillation.
  - Fresh water collected at each field site; precipitation collected near field area.

## Isotope analysis (lab methods)
- Isotopes analyzed:
  - Hydrogen/Deuterium (δD) and Oxygen-18 (δ18O) on fresh and moss distillate water.
  - Carbon isotopes (δ13C) in moss cellulose.
- Instruments and labs:
  - δD and δ18O: Isoprime100 IRMS with Vario PyrocubeEA and VarioPyroCubeEA; calibrated to VSMOW/GISP; precision: δD ±1‰, δ18O ±0.5‰.
  - Oxygen isotopes: EA-IRMS (Thermo Finnigan TC/EA → Thermo Delta V) at Cambridge; precision better than 0.4‰; standards calibrated to IAEA for V-SMOW.
  - Carbon isotopes: Costech EA with Thermo DELTA V; precision better than 0.1‰; IAEA standards used.
- Standards and traceability:
  - VSMOWIAEA standards for water isotopes; IAEA reference standards for O and C isotope calibration.

## Datasets and data structure
- Four CSV files:
  1) Royles_Field_data_by_time
  2) Royles_RWC_and_Isotope_data
  3) Royles_Sample_Number_Key
  4) Royles_Water_Samples
- Royles_Field_data_by_time:
  - Columns capture sample metadata (Location, Session, Month, Date, Site, Species) and variables (RWC, C13, O18, Sphagnum flag, Description).
- Royles_RWC_and_Isotope_data:
  - Includes sample-cellulose number, reference number, wet/dry weights, dry weight, RWC, d13C, d18O, dD.
- Royles_Sample_Number_Key:
  - Links sample numbers to reference numbers; includes Date, Location, Species, Herbarium information.
- Royles_Water_Samples:
  - Includes Date, Location, Water type (fresh or leaf distillate), Source, d18O, dD; notes on missing data.
- Data fields use coded descriptors (e.g., A–K categories) to denote measurement types and metadata.

## Data quality and provenance
- Field data collected under formal permissions; vouchers verified by bryologists.
- Isotope analyses calibrated to internationally recognized scales with specified precision.
- Methods referenced from Loader et al. (1997), Stitt et al. (1989), and West et al. (2006) for sample preparation and extraction.
- Data intended for quality assurance through replication (triplicate field measurements) and cross-laboratory calibration.

## GIS-related applications and integration
- Spatial layers for sampling sites with attributes: site name, coordinates, habitat, sampling dates, moss species, and measurement results (RWC, isotopes, chlorophyll metrics).
- Temporal layers enabling time-series visualisation by session/month (chlorophyll fluorescence, RWC, isotopic signals).
- Joins possible via sample-reference numbers to unify field data, isotopes, and water samples for comparative analyses.
- Potential to combine with climatic layers (precipitation, temperature) to model spatial-temporal climatic signals using moss proxies.

## References
- Loader, N. J. et al. 1997. An improved technique for batch processing of small wood samples to α-cellulose.
- Stitt, M. et al. 1989. Metabolite levels in specific cells and subcellular compartments of plant leaves.
- West, A. G. et al. 2006. Water extraction times for plant and soil materials in stable isotope analysis.