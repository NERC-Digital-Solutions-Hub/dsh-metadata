# Supporting documentation for 11-Feedstuff_Gamma_Spectrometry.csv

- This document provides metadata and definitions for the 11-Feedstuff_Gamma_Spectrometry.csv dataset, outlining each column, its meaning, units, and notes.
- The dataset comprises gamma spectrometry measurements for feedstuff samples, with results reported on a dry mass basis for several radionuclides and associated quality indicators.

## Key fields and definitions

- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the sample (foodstuff group).
- Location: Location where the sample was collected.
- Sample_Description: Part of the organism analysed (e.g., whole organism or specific portion).
- Collection_Date: Date of collection (format: dd-mm-yyyy).
- Sample_size: Amount analyzed (units: kg fresh mass).
- Ra-226_Bq/kg_dm: Activity concentration of Ra-226 on a dry mass basis (Bq/kg dry mass); in equilibrium with Pb-214 and Bi-214; blank = below detection limit.
- Unc_Ra-226_Bq/kg_dm: Uncertainty of Ra-226 activity concentration (Bq/kg dry mass); same equilibrium note; blank = below detection limit.
- Detection_Limit_Ra-226_Bq/kg_dm: Detection limit for Ra-226 (Bq/kg dry mass) calculated per ISO 11929; same equilibrium note.
- Cs-137_Bq/kg_dm: Activity concentration of Cs-137 on a dry mass basis (Bq/kg dry mass); blank = below detection limit.
- Unc_Cs-137_Bq/kg_dm: Uncertainty of Cs-137 concentration (Bq/kg dry mass); blank = below detection limit.
- Detection_Limit_Cs-137_Bq/kg_dm: Detection limit for Cs-137 (Bq/kg dry mass) per ISO 11929; note = n/a in some entries.
- Ra-228_Bq/kg_dm: Activity concentration of Ra-228 on a dry mass basis; in equilibrium with Ac-228; blank = below detection limit.
- Unc_Ra-228_Bq/kg_dm: Uncertainty for Ra-228 concentration (format shows enumerated notes); blank = below detection limit.
- Detection_Limit_Ra-228_Bq/kg_dm: Detection limit for Ra-228 (Bq/kg dry mass); enumerated notes include ISO11929 reference; blank = below detection limit.
- K-40_Bq/kg_dm: Activity concentration of K-40 on a dry mass basis; enumerated notes describe Bq/kg dry mass and detection limit handling.
- Unc_K-40_Bq/kg_dm: Uncertainty for K-40 concentration (Bq/kg dry mass); enumerated notes describe formatting.
- Detection_Limit_K-40_Bq/kg_dm: Detection limit for K-40 (Bq/kg dry mass); notes indicate ISO11929 methodology; some entries show n/a.

## Data quality, standards and interpretation

- Measurements are reported on a dry mass basis (Bq/kg_dm) for radionuclides Ra-226, Cs-137, Ra-228, and K-40.
- Detection limits are provided for each radionuclide, calculated according to ISO 11929.
- Where a value is blank, the concentration is below the detection limit.
- Equilibrium relationships are noted for certain isotopes (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228).
- Date format and sample size units are standardized (dd-mm-yyyy; kg fresh mass for sample size).

## Data governance implications for Data Leaders

- Data discoverability and provenance: The metadata clearly describes each column, enabling researchers to understand data origin and measurement context.
- Data standardization needs: Some column names show inconsistent formatting (e.g., spaces in “Ra-226_B q/kg_dm”); harmonization is recommended for integration with broader datasets.
- Data quality management: Inclusion of uncertainties and ISO11929-based detection limits supports transparent quality assessment; ensure consistent handling of blanks across the dataset.
- Metadata completeness: The dictionary provides essential context (equipment-independent notes like equilibrium, detection limits, and sample descriptions) that supports reuse and governance.
- User-centered accessibility: Clear definitions help policy makers and other stakeholders interpret results without requiring domain-specific assumptions.

## Suggested actions for Data Leaders

- Harmonize column naming for consistency across datasets (e.g., remove errant spaces and unify units).
- Enforce consistent missing-value handling for blanks (e.g., represent as standardized NULL or N/A).
- Maintain and extend metadata to document measurement methods, instruments used, and any deviations from ISO11929.
- Ensure provenance and lineage are captured (who collected/measured, when, and under what protocol).
- Facilitate data sharing with clear notes on equilibrium relationships and dry-mass basis reporting to support cross-dataset comparability.