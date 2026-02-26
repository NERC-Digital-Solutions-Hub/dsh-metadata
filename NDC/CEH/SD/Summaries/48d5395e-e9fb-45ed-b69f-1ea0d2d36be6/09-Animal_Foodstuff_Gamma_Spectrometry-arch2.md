# Supporting documentation for 09-Animal_Foodstuff_Gamma_Spectrometry.csv

## Purpose and scope
- Defines metadata and measurement variables for gamma spectrometry results of animal-derived foodstuffs.
- Captures activity concentrations, uncertainties, and detection limits for specific radionuclides.
- Provides guidance on data interpretation (e.g., blanks indicate concentrations below detection limits; equilibrium relationships with decay products).

## Data fields and metadata
- Sample_Code: unique sample identifier.
- Sample_Type: general description of sample (foodstuff group).
- Location: location where sample was collected.
- Sample_Description: part of the organism analysed (e.g., specific tissue or animal part).
- Collection_Date: date of sample collection (dd-mm-yyyy).
- Sample_size: amount analyzed (kg fresh matter or L for milk).

## Radionuclide measurements and QA flags
- Ra-226_Bq/kg_fm: activity concentration of Ra-226 on a fresh mass basis; includes notes on equilibrium with Pb-214 and Bi-214; blank if below detection limit.
- Unc_Ra-226_Bq/kg_fm: uncertainty of Ra-226 activity concentration; same equilibrium note; blank if below detection limit.
- Detection_Limit_Ra-226_Bq/kg_fm: detection limit calculated per ISO 11929; same equilibrium note; blank if below detection limit.
- Cs-137_Bq/kg_fm: activity concentration of Cs-137 on a fresh mass basis; blank if below detection limit.
- Unc_Cs-137_Bq/kg_fm: uncertainty of Cs-137 activity concentration; blank if below detection limit.
- Detection_Limit_Cs-137_Bq/kg_fm: detection limit calculated per ISO 11929; blank if below detection limit.
- Ra-228_Bq/kg_fm: activity concentration of Ra-228 on a fresh mass basis; notes indicate equilibrium with Ac-228; blank if below detection limit.
- Unc_Ra-228_Bq/kg_fm: uncertainty for Ra-228; equilibrium note retained; blank if below detection limit.
- Detection_Limit_Ra-228_Bq/kg_fm: detection limit per ISO 11929; blank if below detection limit.
- K-40_Bq/kg_fm: activity concentration of K-40 on a fresh mass basis; blank if below detection limit.
- Unc_K-40_Bq/kg_fm: uncertainty for K-40; blank if below detection limit.
- Detection_Limit_K-40_Bq/kg_fm: detection limit per ISO 11929; blank if below detection limit.

## Data handling and interpretation
- Values below detection limits are represented by blanks.
- Detection limits are calculated according to ISO 11929.
- Equilibrium relationships: Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228; K-40 not specified with an equilibrium note.
- Units are Bq per kg fresh matter (fm) or L for milk.

## Relation to environmental monitoring objectives
- Supports standardised, QA-driven reporting of radionuclide activity in animal foods for environmental health monitoring.
- Facilitates data verification, cleaning, and transformation into consistent outputs for monitoring over time.
- Datasets are prepared for storage in appropriate data portals and future interoperability.

## Practical considerations for analysts
- Ensure consistent use of units (kg fresh matter or liters for milk) and date formats.
- Treat blank fields as concentrations below the detection limit.
- Maintain documentation of equilibrium assumptions when interpreting Ra-226 and Ra-228 results.