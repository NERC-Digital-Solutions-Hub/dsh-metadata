# Column heading explanations for 1_Spatial_dataset.csv

## Overview
- Describes the meaning, units, and data collection notes for each column in the 1_Spatial_dataset.csv file.
- Dataset covers spatial sampling data and soil/chemical/radioactivity measurements, including radiological contaminants near Chernobyl-era fallout references.
- Location data are in WGS-84 decimal degrees with GPS-derived coordinates and documented accuracy.

## Location and identification fields
- Code: database serial number – a unique identifier for each row.
- Identifier: UIAR unique label – chemical analysis number.
- Latitude: location latitude of sampling site in decimal degrees.
  - Units: decimal degrees.
  - Notes: coordinates determined with satellite GPS receivers (Trimble/Scout Master GPS and MAGELLAN NAV DLX-10) in WGS-84; GPS accuracy ~100 m with a systematic deviation ~300 m.
- Longitude: location longitude of sampling site in decimal degrees.
  - Units: decimal degrees.
  - Notes: as for Latitude.

## Sample and soil metadata
- ADR: Absorbed dose rate at one metre height.
  - Units: micro Gy per hour (μGy h⁻¹).
  - Notes: measured with certified dosimeters DRG-01T.
- Hr: Hydrolytic acidity (Kappen method).
  - Units: milligrams of H⁺ per 100 g dry soil.
  - Notes: GOST 26212-91.
- Ca: Exchangeable calcium in soil.
  - Units: mg per 100 g soil.
  - Notes: GOST 26487-85.
- pH_KCl: Salt-extracted soil acidity (H⁺ concentration).
  - Units: dimensionless (pH-like value).
  - Notes: GOST 26483-85.
- pH_H2O: Water-extracted soil acidity.
  - Units: dimensionless.
  - Notes: GOST 26423-85.
- P2O5: Mobile phosphorus content in soil.
  - Units: mg per 100 g soil.
- Humus: Organic matter-related metric (humus content) in soil.
  - Units: mg per 100 g soil (or percentage in some entries).
  - Notes: references to related GOSTs (26213-91/26207-91) and FAO/UNESCO context.
- Soil_type: Soil classification context (historical USSR/FAO/UNESCO framework).
  - Notes: cites Stolbovoi 2000 and FAO/UNESCO classification; linked to soil type descriptors rather than a single unit.
- Date_of_activity_measurement: Date when measurement activity occurred.
  - Notes: Date format dd-mmm-yy.

## Radiochemical and radiometric measurements
- 137Cs: Terrestrial contamination density with 137Cs.
  - Units: kBq m⁻².
  - Notes: Gamma spectrometry measurements with HPGe detectors (≈30% relative efficiency; 1.90 keV FWHM at 1333 keV).
  - Relative_uncertainty_137Cs_%: reported as a percentage with 95% confidence.
- 134Cs: Terrestrial contamination density with 134Cs.
  - Units: kBq m⁻².
  - Notes: Gamma spectrometry; same detector details as 137Cs.
  - Relative_uncertainty_134Cs_%: reported as a percentage with 95% confidence.
- 154Eu: Terrestrial contamination density with 154Eu.
  - Units: kBq m⁻².
  - Notes: Gamma spectrometry; same detector details.
  - Relative_uncertainty_154Eu_%: reported as a percentage with 95% confidence.
- 90Sr: Terrestrial contamination density with 90Sr.
  - Units: kBq m⁻² (with radiochemical method details noted).
  - Notes: Activity determined by radiochemical method (Pavlotskaya 1997); may include details on measurement treatment (boiling in 6M HNO3).
  - Relative_uncertainty_90Sr_%: reported as a percentage with 95% confidence (and notes on sample treatment).
  - Date_of_Pu_measurement: Date of Pu measurement (seems misaligned but indicates timing relevance for Pu-related measurements).
- 238Pu, 239+240Pu: Contamination densities for plutonium isotopes.
  - Units: kBq m⁻².
  - Notes: Determination methods described (radiochemical approach, heating and acid digestion) and measurement with alpha spectrometry (Soloist) after chemical separation.
  - Relative_uncertainty_238Pu_% and Relative_uncertainty_239+240Pu_%: uncertainties at 95% confidence.
- Notes on measurements: The radionuclide measurements include both direct gamma spectrometry (where applicable) and radiochemical methods, with explicit details on detectors, efficiency, and energy lines used.

## Data quality, uncertainty, and methodology notes
- Uncertainty fields accompany key radionuclide measurements (e.g., Relative_uncertainty_137Cs_%, etc.) to express confidence levels (95%).
- Measurement details include detector type (HPGe), efficiency (~30%), and energy/calibration specifics.
- Some fields include methodological notes and references to standard procedures (e.g., boiling samples in 6M HNO3, Pavlotskaya method) to support traceability and reproducibility.
- Several fields reference Russian/GOST standards and FAO/UNESCO soil classifications to anchor comparability and governance.

## Standards, provenance, and references
- Standards and classifications cited:
  - GOST 26212-91, 26487-85, 26483-85, 26423-85, 26213-91, 26207-91.
  - Stolbovoi (2000) for soil classification alignment with FAO/UNESCO systems.
- Core references for context and methods:
  - Kashparov et al., various studies on soil contamination by 90Sr near Chernobyl (2001; 2003).
  - Pavlotskaya (1997) on radiochemical analysis principles for strontium and actinides.
- The References section at the end enumerates key publications underpinning the measurement approaches and site-specific contamination work.

## Data governance and stewardship implications
- Metadata richness supports discoverability, reusability, and interoperability across systems that recognize GOST-based and FAO/UNESCO soil classifications.
- Clear documentation of coordinates, measurement methods, unit conventions, and uncertainties supports data quality assurance and trusted reuse by data creators and data users.
- Where field descriptions appear misaligned (e.g., Humus and Soil_type lines with cross-references to “Mobile potassium content”), data stewards should ensure cleanup and harmonization during data ingestion to maintain consistency.
- Maintain provenance by preserving instrument details, measurement protocols, date stamps, and uncertainty metrics; capture lineage when updating or transforming data.
- Consider how to handle outdated standards and ensure mapping or crosswalks for interoperability with more modern or international schemas.

## Practical takeaways for data custodians
- Ensure all fields have consistent units and clear, unambiguous explanations; harmonize any misaligned caption lines.
- Preserve source references (GOST numbers, FAO/UNESCO context) to enable audit trails and reproducibility.
- Maintain and publish uncertainty metrics alongside radionuclide measurements to support risk assessment and comparative analyses.
- Document data update policies and ingestion workflows to support timely data availability and version control.
- Provide or enforce data formatting standards (e.g., date formats, coordinate precision) to facilitate automated integration.