# TREE_Northumbria_ICPMS_Soil_DM

## Overview
- Defines a data dictionary for a soil ICP-MS dataset (HEavy metals) used to scrutinise environmental health and inform policy decisions.
- Key identifiers: CEH_Sample_Identifier (UKCEH sample Identifier) and CEH_Sample_Description (UKCEH sample description).
- Metadata fields include Site and Sampling_Date (sampling site and date collected).
- Measured variables are concentrations of multiple elements in milligrams per kilogram dry mass (mg/kg_DM).

## Data Model / Variables
- Core metadata fields:
  - CEH_Sample_Identifier
  - CEH_Sample_Description
  - Site
  - Sampling_Date
- Element concentration fields (all in mg/kg_DM): I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
- Each element field has an accompanying Units = mg/kg_DM and an Explanation (describing it as the concentration of the element in dry mass). Note: some Explanation entries appear misaligned or inconsistent (e.g., repeated references to Co for multiple elements).

## Metadata and Provenance
- The dataset uses UKCEH (UK Centre for Ecology & Hydrology) identifiers and descriptions to anchor sample provenance.
- Each variable is paired with a Units annotation and an Explanation, intended to clarify what the value represents.

## Data Quality and Anomalies
- Several Explanation entries are inconsistent or incorrect (e.g., multiple elements labeled with explanations for cobalt). This indicates metadata quality issues that would need correction to ensure reliable interpretation and verification.

## Implications for Monitoring Frameworks
- Provides a structured, multi-element soil contamination profile suitable for:
  - Tracking spatial and temporal trends in soil metal concentrations.
  - Informing environmental health assessments and policy discussions.
  - Supporting dashboards and reports that communicate soil contamination status across sites and times.
- The explicit inclusion of sampling metadata (sample ID, description, site, date) supports data traceability and integration with other monitoring datasets.