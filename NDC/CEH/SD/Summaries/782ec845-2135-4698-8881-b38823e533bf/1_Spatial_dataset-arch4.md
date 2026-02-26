# Column heading explanations for 1_Spatial_dataset.csv

## Overview
- Provides column-by-column explanations for the 1_Spatial_dataset.csv file, detailing what each header means, its units, and any notes or data provenance references.
- Emphasizes measurements, coordinates, and radiological/analyte data collected from soil samples, along with associated uncertainties and methods.

## Key fields and their meanings
- Code: Database serial number – unique ID.
- Identifier: UIAR unique label – chemical analysis number.
- Latitude: Location of sampling site; decimal degrees; GPS-determined using GPS receivers (Trimbl Navigation Scout Master GPS and MAGELLAN NAV DLX-10) in WGS-84; typical GPS accuracy ~100 m with a ~300 m systematic deviation.
- Longitude: Location of sampling site; decimal degrees; same GPS details as Latitude.
- ADR: Absorbed dose rate at one metre height; units micro Gray per hour (µGy/h); measured with certified dosimeters DRG-01T.
- Hr: Hydrolytic acidity (Kappen method); units mg equivalent of H+ per 100 g dry soil; linked to GOST 26212-91.
- Ca: Exchangeable calcium in soil; units mg per 100 g soil; notes reference GOST standards.
- pH_KCl: Salt-extracted soil acidity (H+ concentration) represented as a dimensionless value; linked to GOST 26483-85.
- pH_H2O: Water-extracted soil acidity; dimensionless.
- P2O5: Mobile phosphorus content in soil; units mg per 100 g soil.
- Humus: Organic matter content; units mg per 100 g soil (note also mentions percentage in accompanying text).
- Soil_type: Classification of soil type (habitat type) per USSR/Fao-UNESCO framework; units/mapping tied to FAO/UNESCO system; reference Stolbovoi 2000 and related GOSTs.
- Date_of_activity_measurement: Date of measurement.
- 137Cs: Terrestrial density of soil contamination with 137Cs; units kBq/m^2; measured via gamma spectrometry using HPGe detectors (30% relative efficiency, 1.90 keV FWHM at 1333 keV); includes relative uncertainty (95% CI).
- 134Cs: Terrestrial density of soil contamination with 134Cs; units kBq/m^2; same gamma spectroscopy method as 137Cs; includes relative uncertainty.
- 154Eu: Terrestrial density of soil contamination with 154Eu; units kBq/m^2; same gamma spectroscopy method; includes relative uncertainty.
- 90Sr: Terrestrial density of soil contamination with 90Sr; units kBq/m^2; measured via radiochemical method (Pavlotskaya 1997) with relative uncertainty; notes about sample treatment (boiling in 6M nitric acid).
- 238Pu: Terrestrial density of soil contamination with 238Pu; units kBq/m^2; radiochemical measurement details including boiling in 6M HNO3; notes on sample homogenization and measurement with alpha spectrometry; includes relative uncertainty.
- 239+240Pu: Terrestrial density of soil contamination with 239+240Pu; units kBq/m^2; radiochemical method details similar to 238Pu; includes relative uncertainty.
- Relative_uncertainty_137Cs_%, Relative_uncert_137Cs_%: Relative uncertainty of 137Cs measurement (95% CI).
- Relative_uncert_134Cs_%: Relative uncertainty for 134Cs (95% CI).
- Relative_uncert_154Eu_%: Relative uncertainty for 154Eu (95% CI).
- Relative_uncert_90Sr_%: Relative uncertainty for 90Sr (95% CI); notes treatment of samples (boiled in 6M HNO3) for uncertainty calculation.
- Relative_uncert_238Pu_%: Relative uncertainty for 238Pu (95% CI); notes treatment of samples (boiled in 6M HNO3) for uncertainty calculation.
- Relative_uncert_239+240Pu_%: Relative uncertainty for 239+240Pu (95% CI); notes treatment of samples (boiled in 6M HNO3) for uncertainty calculation.
- Date_of_Pu_measurement: Date of Pu measurement; includes treatment details and calculation notes.

## Metadata, provenance, and measurement methods
- Location data (Latitude/Longitude) rely on GPS with specified accuracy and WGS-84 standard.
- Radiological measurements (137Cs, 134Cs, 154Eu, 90Sr, 238Pu, 239+240Pu) use a mix of gamma spectrometry (HPGe detectors) and radiochemical methods, with explicit performance characteristics (e.g., detector efficiency, energy resolution) and specified preparation steps (e.g., boiling in nitric acid for Pu isotopes).
- Uncertainty reporting: Each radionuclide has an associated relative uncertainty (often 95% confidence interval).
- References to standards and methods: Multiple GOST standards (Russian/Soviet norms) are cited for soil chemistry parameters (pH, acidity, P2O5, Ca, Humus, etc.) and measurement procedures; radiochemical methods cite Pavlotskaya (1997) and related methodological notes.
- Habitat/soil classification: Soil_type and related notes tie to FAO/UNESCO systems, with cross-references to Stolbovoi’s work on soils of Russia.
- Data lineage: The dataset is designed to capture both the numerical results and the measurement context (methods, dates, instrument details, and standards used).

## Data quality, standards, and discoverability
- Emphasizes explicit units, measurement methods, and standard references to enable reproducibility and cross-dataset comparability.
- Metadata richness supports data governance, auditability, and proper data stewardship across the data life cycle.
- Potential for standardization challenges due to historical Russian standards, mixed unit practices, and varying documentation quality across parameters.

## References
- Kashparov et al. on soil contamination by 90Sr near Chernobyl; 2001.
- Kashparov 2003 on hot particles at Chernobyl; Environmental Science and Pollution Research.
- Kashparov et al. on territory contamination with radionuclides from Chernobyl fallout; The Science of the Total Environment, 2003.
- Pavlotskaya 1997 on radiochemical analysis principles and methods for strontium and transuranium radionuclides.
- Stolbovoi 2000 and related IIASA/IW-Pure references for soil classification and FAO/UNESCO alignment.

## Practical implications for Data Leaders
- This dataset exemplifies comprehensive data governance through a detailed data dictionary that links each field to units, methods, and standards.
- For effective data strategy, ensure continued alignment with provenance (methods, detectors, calibration), maintain up-to-date metadata, and harmonize standards across datasets to enable cross-network collaboration.
- Leverage the metadata to assess data quality, gaps (e.g., fields with n/a units or noted methodological variations), and potential barriers to interoperability with external partners or public policy teams.
- Maintain traceability of measurement methods and references to support audits, reproducibility, and transparent communication with stakeholders.