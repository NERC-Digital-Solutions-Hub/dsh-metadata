# Supporting documentation for 15-Animal_Feed_Stable.csv

## Overview
- Defines the dataset schema for measuring stable element concentrations in animal total diet samples.
- Includes metadata (Animal, Location, Feeding) and concentration data for multiple elements, each with associated uncertainty and detection-limit fields.
- All concentration values are in mg per kg of dry mass (mg/kg_dm).
- Designed to support standardized QA, cleaning, transformation, and consistent reporting (e.g., reports, maps, charts) and to be stored/uploaded to appropriate data portals.

## Key data fields

- Animal
  - Explanation: General type of animal.
  - Units: n/a.
  - Notes: n/a.

- Location
  - Explanation: Location where the sample was collected.
  - Units: n/a.
  - Notes: n/a.

- Feeding
  - Explanation: Description of the feeding regimes.
  - Units: n/a.
  - Notes: n/a.

- Cs_mg/kg_dm
  - Explanation: Concentration of stable Cs in the total diet on a dry mass basis.
  - Units: mg per kg dry mass.
  - Notes: If blank, concentration is below detection limit.

- Unc_Cs_mg/kg_dm
  - Explanation: Uncertainty (quadratic propagation) of stable Cs concentration.
  - Units: mg per kg dry mass.
  - Notes: If blank, concentration is below detection limit.

- Detection_Limit_Cs_mg/kg_dm
  - Explanation: Detection limit of stable Cs in the total diet on a dry mass basis.
  - Units: mg per kg dry mass.
  - Notes: If blank, concentration is above the detection limit.

- Sr_mg/kg_dm, Unc_Sr_mg/kg_dm, Detection_Limit_Sr_mg/kg_dm
  - Similar structure to Cs fields for stable strontium.

- K_mg/kg_dm, Unc_K_mg/kg_dm, Detection_Limit_K_mg/kg_dm
  - Similar structure to Cs fields for stable potassium.

- Na_mg/kg_dm, Unc_Na_mg/kg_dm, Detection_Limit_Na_mg/kg_dm
  - Similar structure to Cs fields for stable sodium.
  - Notes: Documentation shows numbered subfields (1, 2, 3) for some Na fields, indicating units or notes formatting; overall meaning remains concentration, uncertainty, and detection limit.

- Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm
  - Each element follows the same pattern: concentration (mg/kg_dm), uncertainty (Unc_*), and detection limit (Detection_Limit_*).
  - Pb, U, Th fields include similarly formatted uncertainty and detection-limit descriptors; some entries show formatting irregularities with numbered subfields.

## Data quality and interpretation

- Measurement semantics
  - Concentrations are reported as mg/kg_dm.
  - Blank concentration values indicate the concentration is below the detection limit.
  - Uncertainty fields use quadratic propagation.
  - Detection limit fields indicate the threshold above which concentrations are detectable.

- Data organization
  - Consistent naming convention across elements (element_mg/kg_dm, Unc_element_mg/kg_dm, Detection_Limit_element_mg/kg_dm).
  - Location and Feeding metadata provide context for environmental monitoring and dietary exposure assessments.

- Quality assurance implications
  - Ensure units are uniformly mg/kg_dm across all records.
  - Validate that blanks are correctly flagged as below detection limit.
  - Verify that corresponding Unc and Detection_Limit values exist or are properly flagged when data are missing.
  - Be aware of formatting irregularities in certain fields (notably Na, Pb, U, Th sections) that may require data cleaning.

## Data usage and outputs

- Supports standardized environmental health monitoring outputs (reports, maps, charts) by providing a uniform data schema and clear interpretation rules.
- Facilitates data portal uploads and long-term storage for policy and health-trend analysis.

## Challenges and opportunities for analysts

- Challenge: Increasing the value of these datasets by integrating with additional relevant data sources (e.g., other dietary components, environmental exposure data) to avoid single-use datasets.
- Challenge: Enabling access to underlying data used to generate final outputs, ensuring transparency and reusability.
- Opportunity: Use standardized fields and QA rules to streamline cross-study comparisons and trend analyses over time.