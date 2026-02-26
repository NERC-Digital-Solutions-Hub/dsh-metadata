# Column heading explanations for 2_Plutonium_isotope_measurements.csv

## Overview
- Defines the column headings and metadata used in the 2_Plutonium_isotope_measurements.csv dataset.
- Provides explanations, units, and notes to support data understanding, traceability, and reuse.

## Column definitions (key fields)
- Code
  - Explanation: Database serial number – unique ID.
  - Units: n/a
  - Notes: .
- Identifier
  - Explanation: UIAR unique label – chemical analysis number.
  - Units: n/a
  - Notes: .
- Date_of_Pu_measurement
  - Explanation: Date of measurement (long date format).
  - Units: dd-mm-yy
  - Notes: .
- Terrestrial_density_of_soil_contamination_with_238Pu_kBq_m-2
  - Explanation: 238Pu contamination in soil expressed on an aerial basis.
  - Units: kBq/m^2
  - Notes: For determination, one homogenized 100 cm^3 sample was used; details of heating (450 °C overnight) and boiling in 6M HNO3, radiochemical extraction (Pavlotskaya, 1997), and activity measurement with a Soloist alpha-spectrometer (Soloist-U0300 detector, EG&G ORTEC, USA).
- Relative_uncertainty_238Pu_%
  - Explanation: Relative uncertainty of determination (95% confidence interval).
  - Units: %
  - Notes: .
- Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2
  - Explanation: 239,240Pu contamination in soil expressed on an aerial basis.
  - Units: kBq/m^2
  - Notes: Same sample preparation and measurement approach as 238Pu.
- Relative_uncertainty_239_240Pu_%
  - Explanation: Relative uncertainty of determination (95% confidence interval).
  - Units: %
  - Notes: .

## Measurement methodology and context (Notes)
- The notes describe a radiochemical method for plutonium isotope determination, including:
  - Use of homogenized 100 cm^3 soil samples.
  - Heating at 450 °C, boiling in 6M HNO3.
  - Plutonium radiochemical extraction following Pavlotskaya (1997).
  - Activity measurements with a Soloist alpha-spectrometer and Soloist-U0300 detector (EG&G ORTEC, USA).

## Data quality, provenance, and formats
- Date format is specified as long date format with the dd-mm-yy convention noted.
- Measurements are provided for two isotopes: 238Pu and 239+240Pu, each with accompanying 95% confidence interval uncertainties.
- Units are consistently expressed as kiloBequerels per square meter (kBq/m^2) for soil contamination densities.

## References
- Kashparov, V.A. et al. (2003). Territory contamination with radionuclides representing the fuel component of Chernobyl fallout. The Science of The Total Environment, 317, 105-119.
- Pavlotskaya, F.I. (1997). Main principles of radiochemical analysis of environmental objects and methods of measurements of strontium and transuranium elements radionuclides. Journal of Analytical Chemistry, 52(2), 126-143. (In Russian)