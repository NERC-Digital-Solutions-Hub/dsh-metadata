# TREE_Northumbria_ICPMS_Woodmice_Whole_Organism_FM_Concentration

## Overview
- Dataset of element concentrations in wood mouse whole-organism tissue, measured by ICPMS.
- Focus on fresh mass (FM) concentrations; units are mg/kg for most elements.
- Accompanied by sample metadata to enable discovery and reuse.

## Dataset contents and structure
- Core specimen identifiers:
  - Latin_Species_Name and Common_Species_Name (species identification).
  - Site (sampling location) and Date_Sample_Collected (collection date).
  - CEH_Sample_Description (UKCEH sample description) and Notes about tissues used to calculate whole-organism concentrations.
- Measurement scope:
  - Concentrations for numerous elements in wood mouse whole-organism tissue, with column names indicating element and unit context (e.g., I_mg_kg_whole-organism_FM, Li_mg_kg_whole-organism_FM, Na_mg_kg_whole-organism_FM, Mg_mg_kg_whole-organism_FM, etc.).
  - Each concentration column has an accompanying explanation (e.g., “Concentration of I in wood mouse whole-organism in milligram per kilogram fresh mass”).
  - Some columns include a less-than marker (e.g., <I, <Ni, <Ag, <U) to denote concentrations below a detection threshold.
- Coverage includes a wide range of elements (I, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U), all in mg/kg FM.

## Metadata fields and variable definitions
- For each data column, there is a defined explanation describing:
  - The element concentration measured.
  - The organism and tissue context (wood mouse whole-organism).
  - The unit (mg/kg) and basis (fresh mass).
- Notes field provides context about tissues used for calculations, supporting reproducibility and interpretation.

## Measurement specifics and data flags
- Concentrations are reported on a whole-organism basis using fresh mass as the reference.
- "<" markers indicate values below detection or reporting limits for specific elements (e.g., <Ni, <Ag, <U).
- Metadata includes sample descriptors and site/date information to support provenance and re-use.

## Data quality, standardization, and governance
- Alignment with data stewardship goals: ensure dataset meets appropriate standards, is findable, accessible, interoperable, and reusable.
- Key quality considerations:
  - Consistency in column naming conventions and unit definitions (mg/kg FM).
  - Clear definitions for each element concentration column and its context.
  - Proper handling and documentation of censored data (less-than values).
  - Comprehensive metadata coverage (species names, site, date, sample description, tissue notes) to support discoverability and reuse.
- Data custodians should provide guidance and tooling for data creators to meet standards, and document any data processing steps (quality assurance, cleaning, transformation) before sharing.
- Governance aspects include acknowledging data sharing limitations, disclosure risks, and embargo considerations; ensuring updates are managed and recorded; and uploading to appropriate data portals and catalogues.

## Access, sharing, and updates
- Upload to relevant portals and catalogue data holdings to improve discoverability.
- Maintain documentation of work performed on datasets (e.g., QA, cleaning, transformations) to support transparency.
- Respect any sharing limitations or embargoes and establish routines for updating the dataset as new data become available.

## Particular challenges aligned with this dataset
- Incomplete picture of user needs and priorities for exposure and interpretation of metal concentrations in small mammals.
- Timeliness of data provision from collection to sharing (batch processing and validation may be required).
- Encouraging data creators to meet metadata and standardization requirements across many elements and fields.
- Managing data across multiple systems and formats; handling a large number of concentration columns and potential non-interoperable legacy formats.
- Handling large, high-resolution datasets and ensuring efficient transfer, storage, and access.
- Dealing with legacy or outdated databases that may require bespoke solutions for interoperability.