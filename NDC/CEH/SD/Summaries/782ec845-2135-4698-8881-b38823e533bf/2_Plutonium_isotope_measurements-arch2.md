# Column heading explanations for 2_Plutonium_isotope_measurements.csv

## Purpose and scope
- Defines column headers, units, and notes for a CSV of plutonium isotope measurements in soil.
- Supports standardized recording, quality assurance, and subsequent monitoring analyses of environmental contamination.

## Column-by-column definitions
- Code
  - Database serial number - unique ID; units not applicable; notes blank.
- Identifier
  - UIAR unique label - chemical analysis number; units not applicable; notes blank.
- Date_of_Pu_measurement
  - Date of measurement (long date format); units show as dd- mm m-yy; notes blank.
- Terrestrial_density_of_soil_contamination_with_238Pu_kBq_m-2
  - Contamination of soil by 238Pu expressed as aerial density; units: kBq/m^2.
  - Notes describe that one homogenized 100 cm^3 sample was used, heated to 450 °C overnight, boiled in 6M HNO3 for 4 hours, radiochemical extraction per Pavlotskaya (1997), and activity measured on plates with a Soloist alpha-spectrometer and Soloist-U0300 detector.
- Relative_uncertainty_238Pu_%
  - Relative uncertainty of the 238Pu determination; units: percent; notes indicate 95% confidence interval.
- Terrestrial_density_of_soil_contamination_with_239_240Pu_kBq_m-2
  - Contamination of soil by 239,240Pu expressed as aerial density; units: kBq/m^2.
  - Notes describe the same sample preparation and measurement approach as for 238Pu (Pavlotskaya, 1997) and measurement with the Soloist alpha-spectrometer.
- Relative_uncertainty_239_240Pu_%
  - Relative uncertainty of the 239,240Pu determination; units: percent; notes indicate 95% confidence interval.

## Data quality and processing considerations
- Data are obtained using standardized radiochemical methods and a consistent measurement workflow, facilitating comparability across sites and time.
- Notes provide explicit methodological steps to support replication and auditability.

## Measurement methodology
- Sample type: homogenized 100 cm^3 soil aliquots.
- Preparation: heating at 450 °C overnight; digestion in 6M HNO3 for 4 hours.
- Analysis: radiochemical separation of plutonium; activity measured by alpha spectrometry using Soloist alpha-spectrometer with Soloist-U0300 detector (EG&G ORTEC, USA).
- References embedded in notes: Pavlotskaya (1997) for radiochemical methods; Kashparov et al. (2003) for broader context on territory contamination by fuel-component radionuclides of Chernobyl fallout.

## Uncertainty reporting
- Relative uncertainties are provided for both 238Pu and 239,240Pu with 95% confidence intervals.

## Data provenance and references
- Primary methodological and context references:
  - Pavlotskaya, F.I. (1997). Main principles of radiochemical analysis of environmental objects and methods of measurements of strontium and transuranium elements radionuclides.
  - Kashparov et al. (2003). Territory contamination with radionuclides representing the fuel component of Chernobyl fallout.
- Instrumentation and measurement context: Soloist alpha-spectrometer and Soloist-U0300 detector (EG&G ORTEC, USA).

## Relevance to environmental monitoring
- Provides a standardized data structure to track plutonium isotope contamination densities in soils over time.
- Enables data validation, storage, and sharing, and supports integration with other environmental datasets for monitoring performance and policy assessment.