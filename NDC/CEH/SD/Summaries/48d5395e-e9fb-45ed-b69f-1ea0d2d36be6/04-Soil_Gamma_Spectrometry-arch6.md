# Supporting documentation for 04-Soil_Gamma_Spectrometry.csv

## Overview
- Metadata and field definitions for the soil gamma spectrometry dataset 04-Soil_Gamma_Spectrometry.csv.
- Captures sample identifiers, sample context, collection details, and measured radioactivity concentrations (in Bq per kg dry mass) for key isotopes.
- Includes uncertainty estimates and detection limits, with notes on isotope equilibrium where applicable.

## Data fields and units
- Sample_Code
  - Description: Unique sample identifier
  - Units: n/a
- Sample_Type
  - Description: Type of sample
  - Units: n/a
  - Example: Soil
- Location
  - Description: Location name where the sample was collected
  - Units: n/a
- Sample_Description
  - Description: Further explication of the sample
  - Units: n/a
  - Example: Soil collected at depth 0-10 cm
- Collection_Date
  - Description: Date of sample collection
  - Units: dd-mm-yyyy
- Sample_size
  - Description: Amount of sample analysed
  - Units: Kg dry matter
- Ra-226_Bq/kg_dm
  - Description: Activity concentration of Ra-226 on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214
- Unc_Ra-226_Bq/kg_dm
  - Description: Uncertainty of Ra-226 concentration
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214
- Detection_Limit_Ra-226_Bq/kg_dm
  - Description: Detection limit for Ra-226
  - Units: Bq per kg dry mass
  - Notes: Calculated according to ISO 11929; in equilibrium with Pb-214 and Bi-214
- Cs-137_Bq/kg_dm
  - Description: Activity concentration of Cs-137 on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below detection limit
- Unc_Cs-137_Bq/kg_dm
  - Description: Uncertainty of Cs-137 concentration
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below detection limit
- Detection_Limit_Cs-137_Bq/kg_dm
  - Description: Detection limit for Cs-137
  - Units: Bq per kg dry mass
  - Notes: Calculated according to ISO 11929
- Ra-228_Bq/kg_dm
  - Description: Activity concentration of Ra-228 on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228
- Unc_Ra-228_Bq/kg_dm
  - Description: Uncertainty for Ra-228 concentration
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228
- Detection_Limit_Ra-228_Bq/kg_dm
  - Description: Detection limit for Ra-228
  - Units: Bq per kg dry mass
  - Notes: Calculated according to ISO 11929; in equilibrium with Ac-228
- K-40_Bq/kg_dm
  - Description: Activity concentration of K-40 on a dry mass basis
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below detection limit
- Unc_K-40_Bq/kg_dm
  - Description: Uncertainty for K-40 concentration
  - Units: Bq per kg dry mass
  - Notes: Where blank, concentration below detection limit
- Detection_Limit_K-40_Bq/kg_dm
  - Description: Detection limit for K-40
  - Units: Bq per kg dry mass
  - Notes: Calculated according to ISO 11929

## Measurement details and context
- Isotopes measured: Ra-226, Cs-137, Ra-228, and K-40 (with associated uncertainties and detection limits).
- Unit convention: All activity concentrations expressed on a dry mass basis (Bq/kg_dm).
- Depth context: Sample description indicates soil collected at 0–10 cm depth.
- Equilibrium notes: Ra-226 is reported with equilibrium references to Pb-214 and Bi-214; Ra-228 is reported in equilibrium with Ac-228.
- Detection limits: Determined per ISO 11929; blanks indicate non-detects.

## Data quality and interpretation notes
- Non-detects: Blank values for concentration and/or uncertainty or detection limit fields indicate the concentration is below the detection limit.
- Formatting irregularities: Some fields contain multi-part notes (e.g., “1 =”, “2 =”, “3 =”) likely artifacts; core meaning remains: uncertainty and detection limits, plus equilibrium context, should be interpreted as standard metadata fields.
- Consistency considerations: Ensure consistent handling of non-detects and isotope equilibrium when integrating across samples or building data products.

## How this supports data exploration and product development
- Enables self-serve analysis of soil radioactivity by location, date, and depth, facilitating dashboards and reports.
- Supports comparisons of isotope concentrations across sites and over time.
- Provides clear metadata on units, detection limits, and uncertainties to inform data quality assessments and downstream analyses.
- Facilitates filtering and annotation based on equilibrium context (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228).

## Usage considerations and next steps for data users
- When aggregating, decide on handling of non-detects (e.g., substitution with detection limit, or censoring) based on analysis goals.
- Verify date formats and convert Collection_Date if integrating with other time-series datasets.
- Align sample_size units and ensure consistent mass-basis conversions if cross-dataset comparisons are planned.
- Leverage equilibrium notes to interpret Ra-226 and Ra-228 measurements in environmental context.