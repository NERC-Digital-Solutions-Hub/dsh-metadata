# Column heading explanations for 1_Spatial_dataset.csv

## Overview
- Provides a data dictionary for a spatial soil dataset focused on radiological contamination.
- Documents column purposes, data types, units, and methodological notes for each field.
- Reflects measurements of radionuclides (e.g., 137Cs, 134Cs, 90Sr, plutonium isotopes, 154Eu) and related soil properties at sampling sites with geographic coordinates (WGS-84).

## Key data fields

- Code: Database serial number; unique ID for each record.
- Identifier: UIAR unique label – chemical analysis number.
- Latitude / Longitude: Sampling site coordinates in decimal degrees (WGS-84); GPS-derived with approximate accuracy (about 100 m, systematic deviation ~300 m).
- ADR: Absorbed dose rate at 1 m height; units in micro Gray per hour (µGy h^-1).
- Hr: Hydrolytic acidity (Kappen method); units in mg of H+ per 100 g dry soil.
- Ca: Exchangeable calcium in soil; units in mg per 100 g soil.
- pH_KCl / pH_H2O: Soil acidity measures (salt-extracted and water-extracted), respectively; linked to specific GOST standards.
- P2O5: Mobile phosphorus content; units in mg per 100 g soil.
- Humus / Soil_type: Organic matter content and soil classification references (per FAO/UNESCO system; notes reference Stolbovoi and related sources).
- Date_of_activity_measurement: Date when measurements were taken.
- 137Cs / 134Cs / 90Sr / 238Pu / 239+240Pu / 154Eu: Radionuclide activity-related fields (see below for units and methods).
- Relative_uncertainty_...: 95% confidence interval uncertainty for each radionuclide measurement.

## Radionuclide measurements (specific fields)

- 137Cs, 134Cs, 154Eu, 90Sr, 238Pu, 239+240Pu:
  - Activity densities or concentrations (units vary by isotope and measurement context; e.g., kBq m^-2 or marked as per 100 g soil in some fields).
  - Measurement methods:
    - Gamma spectrometry with HPGe detectors (30% relative efficiency; 1.90 keV FWHM at 1333 keV) using specific equipment.
    - 90Sr: radiochemical method (Pavlotskaya, 1997) for measurement.
    - Pu isotopes (238Pu, 239+240Pu): radiochemical dissolution in 6M HNO3 followed by alpha spectrometry (Soloist Alpha Spectrometer with Soloist-U0300 detector).
  - Relative uncertainties provided for each radionuclide (95% CI).

- Relative_uncertainty fields:
  - Percentages indicating confidence in the corresponding radionuclide measurements.
  - Some entries reflect measurement treatment (e.g., boiling in 6M HNO3) affecting uncertainty.

## Measurement methods and quality

- Gamma spectrometry: details on detectors, efficiency, and energy resolution for cesium and europium isotopes.
- Radiochemical methods: described procedures for strontium and plutonium isotopes, including sample preparation steps.
- Uncertainty reporting: 95% confidence intervals included for key radionuclide measurements.
- Data provenance notes: references to underlying standard procedures and equipment used in analyses.

## Data provenance and standards

- pH and soil chemistry fields reference GOST standards (e.g., 26212-91, 26483-85, 26423-85, 26207-91).
- Soil classification notes reference FAO/UNESCO systems and Stolbovoi (IIASA) work.
- Measurement method notes include instrument models and detector specifications (e.g., GEM-30185, ORTEC; HPGe detectors).

## Data formatting and units

- Latitude/Longitude: decimal degrees; GPS-derived coordinates with noted accuracy.
- ADR: micro Gray per hour (µGy h^-1).
- Hr, Ca: mg per 100 g dry soil (or similar soil-mass basis per field).
- pH_KCl / pH_H2O: dimensionless representations of soil acidity.
- P2O5: mg per 100 g soil.
- Isotope activities: reported in kBq m^-2 or as per 100 g soil, depending on field; uncertainties follow 95% CI.
- Date fields: dd-mmm-yy format (where applicable).

## References and context

- Kashparov et al. (soil contamination with 90Sr near Chernobyl), Journal of Environment Radioactivity, 2001.
- Kashparov (Hot Particles at Chernobyl), Environmental Science and Pollution Research, 2003.
- Kashparov et al. (territory contamination with radionuclides from Chernobyl fallout), The Science of the Total Environment, 2003.
- Pavlotskaya (radiochemical analysis of Sr and transuranic radionuclides), Journal of Analytical Chemistry, 1997.
- Supporting methodological notes on radiochemical analysis and plutonium isotope measurements.

## Relevance for monitoring frameworks

- Provides a structured data dictionary enabling standardized capture of location, soil properties, and radiological measurements for environmental health monitoring.
- Highlights data quality considerations, including the need for metadata, measurement method transparency, uncertainty reporting, and adherence to standards.
- Illustrates integration of geospatial data with radiological indicators, useful for evaluating policy decisions, risk assessment, and informing future monitoring cycles.
- Emphasizes provenance and documentation to support data sharing and governance within monitoring programs.