# TREE_Northumbria_ICPMS_Soil_DM

## Overview
- Dataset describing ICP-MS soil element concentrations from Northumbria (UKCEH context).
- Primary identifiers: CEH_Sample_Identifier (UKCEH sample identifier), Site (sampling site), Sampling_Date (date sample collected), CEH_Sample_Description (sample description).
- Concentrations are reported for a wide range of elements as I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
- All concentration units are mg/kg dry mass (DM). Metadata explains each field (e.g., what each sample identifier means, site, and description).

## Dataset structure and key fields
- CEH_Sample_Identifier
  - Type/Notes: String; Explanation = UKCEH sample Identifier
- CEH_Sample_Description
  - Type/Notes: String; Explanation = UKCEH sample description
- Site
  - Type/Notes: String; Explanation = Sampling site
- Sampling_Date
  - Type/Notes: Date; Explanation = Date sample collected
- I_mg_kg_DM to U_mg_kg_DM
  - Type/Notes: Numeric (mg/kg); Explanation = Concentration of element in milligram per kilogram dry mass
  - Elements included: I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Data labeling notes
  - Several lines in the source contain redundant or mislabelled descriptions (e.g., “Concentration of Co in milligram per kilogram dry mass = Concentration of Ni…” and similar). This indicates potential inconsistencies that require data cleaning and field mapping to ensure correct element attribution.

## Semantics, metadata, and documentation
- Units: mg/kg (dry mass) for all element concentrations.
- Core metadata fields to capture in governance records: sample identifiers, site, sampling date, sample description, and per-element concentrations.
- Source context: UKCEH/Northumbria soil sampling with standard ICP-MS analysis.

## Data quality considerations for Data Stewards
- Completeness: verify presence of CEH_Sample_Identifier, Site, Sampling_Date, and all element concentration fields; identify and document any missing values.
- Metadata accuracy: reconcile mislabelled entries (e.g., inconsistent element descriptions) to ensure correct element mapping.
- Metadata fidelity: preserve the intended meaning of each field, ensure explanations align with the dataset’s data dictionary.
- Consistency: check that all element fields use consistent units (mg/kg DM) and that numeric values are within plausible ranges for soil samples.
- Interoperability: align field names and definitions with existing data standards and catalogues to facilitate discovery and reuse.
- Versioning and provenance: track data revisions, corrections to labels, and updates to sample metadata; maintain a changelog.

## Access, sharing, and governance
- Upload pathway: datasets should be uploaded to relevant portals and catalogues as part of data sharing workflows.
- Sharing limitations: document any embargoes, proprietary concerns, or data-use restrictions affecting the dataset.
- Update mechanisms: establish processes for updating datasets when new samples are added or corrections are made, including notification of stakeholders.
- Documentation: maintain accessible data dictionaries and field-level metadata to support data users in understanding concentrations and sampling context.

## Particular challenges to anticipate
- Incomplete picture of user needs and priorities, affecting how the dataset is described and shared.
- Timely acquisition of datasets from data creators to populate or update the repository.
- Ensuring data creators adhere to metadata standards and consistent documentation across elements.
- Handling multiple systems and formats, including non-interoperable legacy data.
- Managing large datasets and potential difficulties in transferring data.
- Dealing with outdated source databases requiring bespoke transformations while maintaining data integrity.

## Recommendations for data stewardship
- Normalize and validate element fields to ensure correct element-to-column mappings (resolve any mislabelled descriptions).
- Create a clear, public data dictionary linking each field to its explanation and unit.
- Implement QA checks for unit consistency, missing values, and plausible concentration ranges.
- Establish a data provenance record capturing source, date of extraction, any transformations, and responsible data creator.
- Align dataset naming and field conventions with institutional data standards to support discoverability.
- Document any access restrictions and update schedules, and provide guidance for data users on how to cite and reuse the dataset.