# Column heading explanations for 2_Plutonium_isotope_measurements.csv

## Overview
- Defines the dataset schema for plutonium isotope measurements, including unique IDs, measurement dates, soil contamination densities for Pu-238 and Pu-239/240, and related uncertainty.
- Includes methodological notes on sample preparation and measurement procedures.
- Cites references underpinning the radiochemical analysis methods.

## Dataset schema (Columns and definitions)
- Code, Explanation: Database serial number - unique ID.
- Code, Units: n/a.
- Code, Notes: .
- Identifier, Explanation: UIAR unique label - chemical analysis number.
- Identifier, Units: n/a.
- Identifier, Notes: .
- Date_of_Pu_measurement, Explanation: Date of measurement (long date format).
- Date_of_Pu_measurement, Units: dd-mm-yy.
- Date_of_Pu_measurement, Notes: .
- Terrestrial_density_of_soil_contamination_with_238Pu_kBq_m-2, Explanation: 238Pu contamination in soil expressed on an aerial basis.
- Terrestrial_density_of_soil_contamination_with_238Pu_kBq_m-2, Units: kilo bequerels per square metre.
- Terrestrial_density_of_soil_contamination_with_238Pu_kBq_m-2, Notes: For determination of plutonium radioisotopes at a given site, one of the homogenized 100 cm3 samples was used. After heating at 450 °C overnight, the samples were boiled for 4 hours in 6M HNO3. Plutonium radioisotopes were extracted by a standard radiochemical method (Pavlotskaya, 1997). Activities on the plates were measured using a Soloist alpha-spectrometer equipped with a Soloist-U0300 detector (EG&G ORTEC, USA).
- Relative_uncertainty_238Pu_%, Explanation: Relative uncertainty of determination (at 95% confidence interval).
- Relative_uncertainty_238Pu_%, Units: percent.
- Relative_uncertainty_238Pu_%, Notes: .
- Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2, Explanation: 239,240Pu contamination in soil expressed on an aerial basis.
- Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2, Units: kilo bequerels per square metre.
- Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2, Notes: For determination of plutonium radioisotopes at a given site, one of the homogenized 100 cm3 samples was used. After heating at 450 °C overnight, the samples were boiled for 4 hours in 6M HNO3. Plutonium radioisotopes were extracted by a standard radiochemical method (Pavlotskaya, 1997). Activities on the plates were measured using a Soloist alpha-spectrometer equipped with a Soloist-U0300 detector (EG&G ORTEC, USA).
- Relative_uncertainty_239_240Pu_%, Explanation: Relative uncertainty of determination (at 95% confidence interval).
- Relative_uncertainty_239_240Pu_%, Units: percent.
- Relative_uncertainty_239_240Pu_%, Notes: .

## Measurement methodology (Notes within columns)
- Sample type: Homogenized 100 cm3 sample per site.
- Preparation: Heating to 450 °C overnight, dissolution in 6M HNO3 with a 4-hour boil.
- Analysis: Radiochemical extraction following Pavlotskaya (1997).
- Detection: Alpha spectrometry using Soloist alpha-spectrometer with Soloist-U0300 detector.

## Data quality and uncertainty
- Uncertainty reported as relative uncertainty with 95% confidence.
- Methodological notes provide traceability to established radiochemical analysis protocols.

## Metadata and provenance
- Unique identifiers and explicit date format enable traceability.
- Notes detail the exact sample preparation and instrumentation, supporting reproducibility and QA/QC.

## Relevance for Monitoring Frameworks
- Demonstrates a well-defined schema with clear units and measurement methods, aiding cross-site comparability.
- Emphasizes the importance of comprehensive methodological metadata for data interpretation and governance.
- Provides a model for linking measurement results (kBq/m2) with uncertainty data to support policy evaluation and decision-making.

## References
- Kashparov V.A., et al. Territory contamination with radionuclides representing the fuel component of Chernobyl fallout. The Science of the Total Environment, 2003.
- Pavlotskaya, F.I. Main principles of radiochemical analysis of environmental objects and methods of measurement of strontium and transuranium radionuclides. Journal of Analytical Chemistry, 1997.