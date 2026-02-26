# Column heading explanations for 2_Plutonium_isotope_measurements.csv

## Purpose and scope
- Documents metadata for each column in the 2_Plutonium_isotope_measurements.csv dataset.
- Defines what each column represents, preferred units, and any notes or methods relevant for data users and for governance.

## Key metadata fields (column-level) and data types
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
  - Notes: For determination of plutonium radioisotopes at a given site, one of the homogenized 100 cm^3 samples was used. After heating at 450 °C overnight, the samples were boiled for 4 hours in 6M HNO3. Plutonium radioisotopes were extracted by a standard radiochemical method (Pavlotskaya, 1997). Activities on the plates were measured using a Soloist alpha-spectrometer with a Soloist-U0300 detector (EG&G ORTEC, USA).
- Relative_uncertainty_238Pu_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval).
  - Units: %
  - Notes: .
- Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2
  - Explanation: 239,240Pu contamination in soil expressed on an aerial basis.
  - Units: kBq/m^2
  - Notes: (Same sample preparation and measurement details as for 238Pu)
- Relative_uncertainty_239_240Pu_%
  - Explanation: Relative uncertainty of determination (at 95% confidence interval).
  - Units: %
  - Notes: .

## Data collection, preparation, and provenance
- Sample handling and preparation
  - Homogenized 100 cm^3 soil sample used per site.
  - Heating at 450 °C overnight, followed by digestion in 6M HNO3 for 4 hours.
  - Plutonium radiochemical extraction performed per established method (Pavlotskaya, 1997).
- Measurement technique
  - Activities measured on plates using a Soloist alpha-spectrometer with a Soloist-U0300 detector (EG&G ORTEC, USA).
- Purpose of metadata notes
  - Documents the exact procedures and instruments used to support reproducibility, auditability, and data reuse.
  - Provides context for interpreting concentrations and uncertainties.

## Data quality and governance considerations
- Standardization
  - Clear definitions of column content, units, and methodological notes to support consistent data integration and downstream discovery.
- Transparency
  - Detailed notes link each measurement field to the specific preparation and measurement protocol.
- Uncertainty reporting
  - Includes 95% confidence interval uncertainties for both 238Pu and 239,240Pu measurements, enabling proper uncertainty propagation in analyses.
- Reproducibility and interoperability
  - References to established methods and instruments facilitate cross-dataset comparisons and replications.

## References
- Kashparov V.A., Lundin S.M., Zvarich S.I., Yoschenko V.I., Levtchuk S.E., Khomutinin Yu.V., Maloshtan I.N., Protsak V.P. Territory contamination with the radionuclides representing the fuel component of Chernobyl fallout. The Science of The Total Environment, vol.317, Issues 1-3, 2003, pp. 105-119.
- Pavlotskaya, F.I.: Main principles of radiochemical analysis of environmental objects and methods of measurements of strontium and transuranium elements radionuclides. Journal of analytical chemistry, 52 (2), 126-143. (In Russian), 1997.