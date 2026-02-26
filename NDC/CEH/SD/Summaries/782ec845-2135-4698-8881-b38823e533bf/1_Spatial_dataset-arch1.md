# Column heading explanations for 1_Spatial_dataset.csv

- The document serves as a reference that explains each column in the 1_Spatial_dataset.csv file, detailing meanings, units, and data provenance.

## Spatial identifiers and site data

- Code: unique database serial number (ID).
- Identifier: UIAR unique label corresponding to the chemical analysis number.
- Latitude / Longitude: site coordinates in decimal degrees using WGS-84; GPS accuracy ~100 m with a systematic deviation around 300 m.

## Environmental and soil chemistry measurements

- ADR: Absorbed dose rate at 1 metre height; units micro Gray per hour (μGy/h); measured with certified dosimeters DRG-01T.
- Hr: Hydrolytic acidity (Kappen method); units mg H+ per 100 g dry soil; linked to GOST 26212-91.
- Ca: Exchangeable calcium in soil; units mg per 100 g soil; linked to GOST 26487-85.
- pH_KCl: Salt-extracted soil acidity (dimensionless).
- pH_H2O: Water-extracted soil acidity (dimensionless).
- P2O5: Mobile phosphorus content in soil; units mg per 100 g soil.
- Humus: Organic matter-related measures; discussions reference Humus content and related standards (GOST 26213-91, 26207-91); units include mg per 100 g soil and percentage.

## Soil classification and metadata

- Soil_type: Classification using FAO/UNESCO system (habitat type) with references to GOST standards.
- Date_of_activity_measurement: Date when the measurement was taken.

## Radioactive contaminants and related measurements

- 137Cs, 134Cs: Terrestrial density of soil contamination with cesium isotopes; units kBq/m²; measured with gamma spectrometry.
- 90Sr: Terrestrial density of soil contamination with strontium-90; units kBq/m²; measurement using a radiochemical method (Pavlotskaya, 1997); includes relative uncertainty fields.
- 238Pu, 239+240Pu: Terrestrial density of soil contamination with plutonium isotopes; units kBq/m²; measurement involves radiochemical processing, heating in 6M HNO3, alpha spectrometry (Soloist system), and specific notes about sample treatment and measurement details; each isotope includes relative uncertainty fields.

## Uncertainty and measurement details

- Relative uncertainties: Fields for 137Cs, 134Cs, 90Sr, 238Pu, and 239+240Pu representing measurement confidence (95% CI) as percentages.
- Pu measurements: Include particular processing steps (e.g., sample homogenization, heating, boiling in nitric acid) and detection method (alpha spectrometry) with specified equipment.

## Methods, standards, and references

- Methods: Gamma spectrometry using HPGe detectors (30% relative efficiency, ~1.90 keV FWHM for 1333 keV) and radiochemical techniques for certain isotopes.
- References and standards: GOST-based methods (26212-91, 26483-85, 26423-85, 26207-91, 26213-91) and literature cited for contamination studies near Chernobyl (Kashparov et al., Pavlotskaya, etc.).

## Practical use and notes for analysts

- The dataset combines spatial, soil chemical, and radioisotope contamination data, enabling mapping, correlation analysis, and risk assessment at site scales.
- Units are standardized (notably kBq/m² for radionuclides) and include measurement uncertainties to support statistical modeling and interpretation.
- Important caveats include GPS positional accuracy, reliance on specific GOST standards, and detailed measurement workflows that affect data interpretation and comparability across sites.