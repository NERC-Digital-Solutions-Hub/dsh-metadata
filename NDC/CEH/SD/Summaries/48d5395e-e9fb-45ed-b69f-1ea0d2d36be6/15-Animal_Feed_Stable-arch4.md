# Supporting documentation for 15-Animal_Feed_Stable.csv

## Purpose and scope
- Provides the metadata and field explanations for the 15-Animal_Feed_Stable.csv dataset.
- Defines the general data structure and each variable’s meaning, units, and notes.
- Covers concentrations of multiple elements in the total diet on a dry mass basis (mg per kg dry mass) across animals, locations, and feeding regimes.
- Includes fields for concentration, uncertainty, and detection limits for several elements (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th, etc.).
- Notes reflect handling of below-detection-limit values and potential data formatting inconsistencies.

## Data schema and key fields
- Core identifiers:
  - Animal
  - Location
  - Feeding
- Elemental concentration fields (example pattern for each element):
  - Element_mg/kg_dm: concentration in mg per kg dry mass
  - Unc_Element_mg/kg_dm: uncertainty (quadratic propagation) in mg per kg dry mass
  - Detection_Limit_Element_mg/kg_dm: detection limit in mg per kg dry mass
  - Notes: indicates when blank means concentration is below or above the detection limit
- Elements covered include Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th, with similar subfields for each.
- Units are consistently mg per kg dry mass (mg/kg_dm), though header notation occasionally uses shortened forms (kg_dm).

## Metadata conventions and data quality
- Explanations clarify what each field represents (e.g., total diet concentration on a dry mass basis).
- Uncertainty fields are described as quadratic propagation.
- Detection limit fields specify the threshold above which a value is detectable.
- Notes explain data interpretation rules (e.g., blank indicates below detection limit; some notes indicate above detection limit).
- Inconsistencies observed in the Na, Pb, and related sections (e.g., numbering in field names, incomplete notes) suggest potential formatting issues.

## Practical implications for data leaders
- The dictionary supports data discovery, interpretation, and cross-dataset integration by standardizing description, units, and detection-limit handling.
- Enables assessment of data readiness for analyses involving trace elements in animal feed and comparison across samples.
- Highlights the need for consistent metadata standards around detection limits, uncertainties, and below-detection-limit handling to ensure reliable analyses.

## Recommendations and next steps
- Clean and standardize column naming, especially for Na, Pb, and related uncertainty/detection fields (avoid inconsistent numbering like Unc_Na_mg/kg_dm, 1/2).
- Harmonize notes with corresponding fields to remove ambiguities (e.g., “blank” meaning below vs above detection limit).
- Ensure uniform application of units (mg/kg_dm) and confirm correct representation of all elements’ subfields.
- Document measurement methods and data provenance to complement this metadata and support reproducibility.