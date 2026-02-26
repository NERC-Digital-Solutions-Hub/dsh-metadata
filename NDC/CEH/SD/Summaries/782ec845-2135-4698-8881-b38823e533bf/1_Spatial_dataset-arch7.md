# Column heading explanations for 1_Spatial_dataset.csv

## Overview
- Provides explanations for each column header in the Spatial_dataset dataset, detailing what each field represents, its units, and any notes or standards used for measurement and labeling.
- Focuses on coordinates, soil chemistry variables, and radiological contaminants measured at sampling sites.

## Spatial and coordinate information
- Latitude and Longitude: location of sampling site, in decimal degrees, using WGS-84.
- GPS context: coordinates determined with satellite GPS receivers (Trimble Navigation Scout Master GPS and MAGELLAN NAV DLX-10); typical accuracy around 100 m with a systematic deviation of about 300 m.
- Importance for GIS: enables mapping of sampling sites and spatial analysis; coordinate precision impacts downstream decisions.

## Identification and data linkage
- Code: database serial number; a unique ID for each record.
- Identifier: UIAR unique label – chemical analysis number.
- Notes: fields marked as n/a or with cross-referenced standards; used to link records to analysis events or samples.

## Soil and analytical attributes
- ADR (Absorbed dose rate at 1 m height): units micro Gray per hour (µGy h⁻¹); associated with certified dosimeters (DRG-01T).
- Hr (Hydrolytic acidity): measured as mg equivalent of H+ per 100 g dry soil; references GOST 26212-91.
- Ca (Exchangeable calcium): units mg per 100 g soil; linked to GOST standards.
- pH_KCl: salt-extracted soil acidity (dimensionless); indicates soil pH in KCl extract.
- pH_H2O: water-extracted soil acidity (dimensionless); indicates soil pH in water extract.
- P2O5: Mobile phosphorus content in soil; units mg per 100 g soil.
- Humus: organic matter content (notes indicate correlation with organic matter); units may be mg per 100 g soil or percentage depending on context; references to GOST standards.
- Soil_type: classification of soil type using USSR/FAO/UNESCO system (Stolbovoi framework reference and related sources).

## Measurement timing and data quality
- Date_of_activity_measurement (Date_of_measurement): date when the measurement was performed; format dd-mmm-yy.
- Relative_uncertainty fields: percent uncertainty for each radiological measurement (e.g., 137Cs, 134Cs, 154Eu, 90Sr, 238Pu, 239+240Pu); reported at 95% confidence interval.
- Notes on measurement methods: radiochemical and gamma spectrometry approaches described (e.g., HPGe detectors, specific detector models, and general procedures).
- Data treatment details: some samples subjected to chemical treatments (e.g., boiling in 6M HNO3 for four hours) prior to measurement; descriptions are provided for several isotopes.

## Radiological isotopes and units
- 137Cs, 134Cs, 154Eu, 90Sr, 238Pu, 239+240Pu: terrestrial density of soil contamination expressed in kBq/m².
- Measurement specifics: gamma spectrometry with HPGe detectors; details include detector efficiency, energy resolution, and reference isotopes.
- Relative uncertainties: provided for each isotope’s measurement.

## Data standards and references
- Standard references: GOST 26212-91, GOST 26487-85, GOST 26483-85, GOST 26423-85, and related documents; indicate the official methods or classifications used.
- Scientific sources: The References section lists several papers on soil contamination (notably from Chernobyl-related studies) that underpin the radiological context and methodologies.

## Practical GIS considerations
- Data integration: multiple data types (chemical soil properties and radiological measurements) require careful harmonization across fields and units.
- Resolution and accuracy: GPS-derived coordinates have inherent accuracy limits; spatial analyses should account for potential locational error margins (~100 m, with possible systematic deviations).
- Data quality and standards: mixed national standards (GOST) and international classifications (FAO/UNESCO) may affect data harmonization and interpretation.
- Uncertainty awareness: radiological measurements include 95% confidence uncertainties that should be propagated in spatial analyses or risk assessments.
- Documentation needs: the column explanations provide essential metadata for correct interpretation and downstream GIS workflows.

## Takeaways for GIS Specialists
- Use the Latitude/Longitude coordinates with awareness of GPS accuracy limits; consider incorporating location error buffers in analyses.
- Map and symbolize both soil chemistry attributes and radiological contamination (kBq/m²) to support spatial understanding of contamination patterns.
- Ensure unit consistency when integrating with other datasets (e.g., convert or annotate for µGy h⁻¹ vs. kBq/m² as appropriate).
- Leverage the standardized column explanations to maintain data provenance and support transparent GIS modeling and reporting.
- Be mindful of data sources and standards (GOST and FAO/UNESCO references) when comparing with other regional datasets. 

## References
- Kashparov, V. A., et al. Soil contamination with 90Sr in the near zone of the Chernobyl accident. Journal of Environment Radioactivity, 2001.
- Kashparov, V. A. Hot Particles at Chernobyl. Environmental Science and Pollution Research, 2003.
- Kashparov, V.A., et al. Territory contamination with radionuclides representing the fuel component of Chernobyl fallout. The Science of The Total Environment, 2003.
- Pavlotskaya, F.I. Main principles of radiochemical analysis of environmental objects and methods of measurements of strontium and transuranium elements radionuclides. Journal of analytical chemistry, 1997.