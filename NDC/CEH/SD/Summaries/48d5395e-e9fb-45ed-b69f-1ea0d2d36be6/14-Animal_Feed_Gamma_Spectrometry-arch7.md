# Supporting documentation for 14-Animal_Feed_Gamma_Spectrometry.csv

## Overview
- Metadata and field definitions for a CSV containing radionuclide activity concentrations in animal feed/diet samples.
- Captures target nuclides (Ra-226, Cs-137, Ra-228, K-40) with concentration values, uncertainties, and detection limits.
- Includes contextual fields such as Animal type, Location, and Feeding regime.
- Notes on sample equilibrium (e.g., Ra isotopes in equilibrium with decay products) and how blanks are interpreted (below detection limit or above detection limit depending on the field).

## Data schema (key fields)
- Animal
  - Description: General type of animal.
  - Units: n/a
- Location
  - Description: Name of the location where the sample was collected.
  - Units: n/a
- Feeding
  - Description: Description of the feeding regime.
  - Units: n/a
- Ra-226_Bq/kg_dm
  - Description: Activity concentration of Ra-226 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214; blank = concentration below the detection limit
- Unc_Ra-226_Bq/kg_dm
  - Description: Uncertainty (quadratic propagation) of Ra-226 concentration.
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214; blank = concentration below the detection limit
- Detection_Limit_Ra-226_Bq/kg_dm
  - Description: Detection limit for Ra-226 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Pb-214 and Bi-214; blank = concentration was above the detection limit
- Cs-137_Bq/kg_dm
  - Description: Activity concentration of Cs-137 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: Where blank = concentration below the detection limit
- Unc_Cs-137_Bq/kg_dm
  - Description: Uncertainty (quadratic propagation) of Cs-137 concentration.
  - Units: Bq per kg dry mass
  - Notes: Where blank = concentration below the detection limit
- Detection_Limit_Cs-137_Bq/kg_dm
  - Description: Detection limit for Cs-137 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: Where blank = concentration was above the detection limit
- Ra-228_Bq/kg_dm
  - Description: Activity concentration of Ra-228 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228; blank = concentration below the detection limit
- Unc_Ra-228_Bq/kg_dm
  - Description: Uncertainty (quadratic propagation) of Ra-228 concentration.
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228; blank = concentration below the detection limit
- Detection_Limit_Ra-228_Bq/kg_dm
  - Description: Detection limit for Ra-228 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: In equilibrium with Ac-228; blank = concentration below the detection limit
- K-40_Bq/kg_dm
  - Description: Activity concentration of K-40 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: Where blank = concentration below the detection limit
- Unc_K-40_Bq/kg_dm
  - Description: Uncertainty (quadratic propagation) of K-40 concentration.
  - Units: Bq per kg dry mass
  - Notes: Where blank = concentration below the detection limit
- Detection_Limit_K-40_Bq/kg_dm
  - Description: Detection limit for K-40 in the total diet on a dry mass basis.
  - Units: Bq per kg dry mass
  - Notes: Where blank = concentration was above the detection limit

## Data quality and interpretation
- Detection limits and blanks:
  - Blank values in concentration fields indicate concentrations below the detection limit.
  - Blank values in uncertainty fields correspond to below-detection-limit cases for the associated concentration.
  - Detection limit fields indicate the threshold above which concentrations would be detectable; blanks there imply the opposite per field’s notes.
- Equilibrium notes:
  - Ra-226, Ra-228, and K-40 columns reference equilibrium relationships with related isotopes (e.g., Pb-214/Bi-214 for Ra-226; Ac-228 for Ra-228).
- Units and basis:
  - All activity concentrations are reported in Bq per kilogram dry mass (Bq/kg_dm).

## GIS usage recommendations
- Data preparation:
  - Join by Location (and optionally Animal) to enable spatial analyses and map visualizations.
  - Normalize or separate data by nuclide (Ra-226, Cs-137, Ra-228, K-40) for clarity; consider separate layers per nuclide or a multi-layer schema.
  - Represent blanks thoughtfully: use nulls for missing concentrations or a specific “below detection limit” category, and optionally store DL values for legend ranges.
- Visualization approaches:
  - Choropleth or dot density maps to display concentration magnitudes by Location or by animal type.
  - Use gradient color ramps for each nuclide; consider separate symbology per nuclide to avoid confusion.
  - Overlay detection limits as reference layers or use hatch patterns to indicate limits on concentration values.
- Data integration and provenance:
  - Include Animal, Location, and Feeding as attributes to support filtering by species, site, or feeding regime.
  - Document equilibrium notes in attribute metadata to support interpretation in spatial analyses.
- Quality control:
  - Validate unit consistency (all in Bq/kg_dm) and ensure proper handling of blanks as below detection limit.
  - Check for inconsistent notes across fields (e.g., detection limit notes versus blanks) and consult data custodian if needed.

## Limitations and notes
- Some field notes are verbose or partially repetitive about equilibrium and detection-limit conditions; treat blanks as per the specific field’s stated rule.
- The documentation reflects a single dataset (14-Animal_Feed_Gamma_Spectrometry.csv) and may require harmonization if combined with other datasets.