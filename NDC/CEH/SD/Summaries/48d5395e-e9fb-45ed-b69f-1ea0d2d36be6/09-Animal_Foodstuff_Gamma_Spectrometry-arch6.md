# Supporting documentation for 09-Animal_Foodstuff_Gamma_Spectrometry.csv

## Purpose and scope
- Provides definitions and explanations for each column in the gamma spectrometry dataset.
- Focuses on animal foodstuff samples and measured radioisotopes (Ra-226, Cs-137, Ra-228, K-40) on a fresh mass basis.
- Defines sample identifiers, sample metadata, measurement results, uncertainties, and detection limits to enable consistent interpretation and reuse.

## Key fields and data types
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of the sample (e.g., foodstuff group).
- Location: Location where the sample was collected.
- Sample_Description: Part of the organism analysed.
- Collection_Date: Date of sample collection (format: dd-mm-yyyy).
- Sample_size: Amount analyzed; units are kg fresh matter or L for milk.
- Isotope measurement blocks (per isotope):
  - [Isotope]_Bq/kg_fm: Activity concentration on a fresh mass basis (Bq/kg_fm).
  - Unc_[Isotope]_Bq/kg_fm: Uncertainty of the activity concentration.
  - Detection_Limit_[Isotope]_Bq/kg_fm: Detection limit calculated per ISO 11929.
  - Notes: Equilibrium context or generic notes (e.g., blank equals below detection limit).

## Measurement details and isotopes
- Radionuclides measured: Ra-226, Cs-137, Ra-228, K-40.
- Units: Bq per kg fresh mass (or Bq per L for milk) for activity concentrations; uncertainties share the same units.
- Equilibrium notes:
  - Ra-226 is in equilibrium with Pb-214 and Bi-214.
  - Ra-228 is in equilibrium with Ac-228.
- Detection limits:
  - Defined for each isotope using ISO 11929.
  - In many rows, blank values indicate concentrations below the detection limit.

## Data quality rules and handling of missing data
- "Where blank, then concentration was below the detection limit" indicates non-detects flagged as blanks.
- Some fields explicitly note when concentrations are below detection limits (e.g., for K-40 or other isotopes in certain rows).
- Data may be patchy across isotopes and samples; detection limits and uncertainties accompany measured values where available.

## Units and normalization considerations
- Primary basis: fresh mass (kg_fm) for solid samples; milk samples use liters (L).
- Consistency across isotopes is maintained by using Bq/kg_fm (or Bq/kg_fm for milk) and corresponding uncertainties and detection limits.

## How this data supports end users
- Enables self-serve analysis through clearly defined fields for sample metadata and isotope concentrations.
- Facilitates quality assurance by explicit detection limits and uncertainty fields.
- Supports data storytelling and dashboards by providing structured, explainable columns with equilibrium context and measurement limits.
- Allows straightforward data cleaning and transformation (e.g., marking non-detects, harmonizing date formats, converting units if needed).

## Considerations for data governance and reuse
- Maintain ISO 11929-based detection limit interpretation.
- Preserve equilibrium notes to ensure correct interpretation of Ra-226 and Ra-228 contexts.
- Treat blank values as non-detects unless supplemented with explicit detected values and uncertainties.