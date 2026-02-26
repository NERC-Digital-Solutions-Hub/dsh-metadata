# Column heading explanations for 2_Plutonium_isotope_measurements.csv

## Overview
- Provides metadata for a CSV of plutonium isotope measurements, formatted for GIS use with per-site soil contamination data expressed as aerial density (kBq/m²).
- Includes unique identifiers, measurement date, isotope-specific contamination densities (238Pu and 239,240Pu), and their relative uncertainties (95% confidence interval).
- Units are specified for each contaminant; dates use a long date format. The notes describe sample preparation and measurement methods to enable reproducibility.

## Column definitions and intended GIS use
- Code: Database serial number – a unique ID; Units: n/a; Notes: (blank)
- Identifier: UIAR unique label – chemical analysis number; Units: n/a; Notes: (blank)
- Date_of_Pu_measurement: Date of measurement; Units: dd-mm-yy (long date format); Notes: (blank)
- Terrestrial_density_of_soil_contamination_with_238Pu_kBq_m-2: 238Pu soil contamination density expressed on an aerial basis; Units: kBq/m²; Notes: One homogenized 100 cm³ sample was used; preparation and radiochemical method described.
- Relative_uncertainty_238Pu_%: Relative uncertainty of the 238Pu determination (95% CI); Units: percent; Notes: (blank)
- Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2: 239,240Pu soil contamination density expressed on an aerial basis; Units: kBq/m²; Notes: Same sample preparation and radiochemical method as above.
- Relative_uncertainty_239_240Pu_%: Relative uncertainty of the 239,240Pu determination (95% CI); Units: percent; Notes: (blank)

## Measurement methods and data provenance
- Sample preparation: homogenized 100 cm³ samples; heated at 450 °C overnight; boiled for 4 hours in 6M HNO₃.
- Radiochemical analysis: Pu radioisotopes extracted using a standard radiochemical method (Pavlotskaya, 1997).
- Measurement: Activities on plates measured with a Soloist alpha-spectrometer using a Soloist-U0300 detector (EG&G ORTEC, USA).

## Data quality, standards, and limitations
- Clear linking of measurements to specific samples and dates supports traceability and GIS integration.
- Methodological notes enable assessment of data quality and comparability across sites.
- Relative uncertainties provide an understanding of precision for mapping and analysis.

## References
- Kashparov V.A., et al. Territory contamination with radionuclides representing the fuel component of Chernobyl fallout. The Science of the Total Environment, 2003.
- Pavlotskaya F.I. Main principles of radiochemical analysis of environmental objects and methods of measurements of strontium and transuranium elements radionuclides. Journal of Analytical Chemistry, 1997.