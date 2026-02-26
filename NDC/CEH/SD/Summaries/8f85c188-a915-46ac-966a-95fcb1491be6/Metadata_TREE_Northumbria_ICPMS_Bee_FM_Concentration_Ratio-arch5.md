# TREE_Northumbria_ICPMS_Bee_FM_Concentration_Ratio

## Overview
- A dataset documenting concentration ratios between bee samples and co-located soil samples, derived from ICP-MS measurements.
- Key fields cover species identity (Latin and common names), sampling site, date collected, and sampling metadata (CEH codes, sample details, descriptions, and notes).
- Includes the co-located soil sample used to calculate the concentration ratio.
- Concentration ratios are defined as the Fresh Mass Bee (whole-body) concentration divided by the Dry Mass Soil concentration.
- Numerous element-specific ratio columns are provided (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U), with some entries allowing “less than” values for certain ratios.

## Data Model and Key Fields
- Taxonomy and identity
  - Latin_Species_Name
  - Common_Species_Name
- Sampling context
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
- Provenance and linkage
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
- Concentration ratio fields
  - I_Concentration_Ratio
  - Li_Concentration_Ratio
  - Be_Concentration_Ratio (and related entries indicating “less than” where applicable)
  - Na_Concentration_Ratio
  - Mg_Concentration_Ratio
  - Al_Concentration_Ratio
  - P_Concentration_Ratio
  - K_Concentration_Ratio
  - Ca_Concentration_Ratio
  - Ti_Concentration_Ratio
  - V_Concentration_Ratio
  - Cr_Concentration_Ratio
  - Mn_Concentration_Ratio
  - Fe_Concentration_Ratio
  - Co_Concentration_Ratio
  - Ni_Concentration_Ratio
  - Cu_Concentration_Ratio
  - Zn_Concentration_Ratio
  - As_Concentration_Ratio
  - Se_Concentration_Ratio
  - Rb_Concentration_Ratio
  - Sr_Concentration_Ratio
  - Mo_Concentration_Ratio
  - Ag_Concentration_Ratio
  - Cd_Concentration_Ratio
  - Cs_Concentration_Ratio
  - Ba_Concentration_Ratio
  - Tl_Concentration_Ratio
  - Pb_Concentration_Ratio
  - U_Concentration_Ratio
- Notes on values
  - Some columns indicate a “less than” value (e.g., <Be_Concentration_Ratio, <Se_Concentration_Ratio, <U_Concentration_Ratio).

## Data Quality, Standards, and Metadata
- Units for many fields are listed as n/a; explicit units for concentrations (bee tissue and soil) should be defined for interoperability.
- Metadata should clarify measurement methods, detection limits, and data processing steps used to compute concentration ratios.
- Ensure consistent naming for concentration ratio fields and resolve any typos or ambiguous column names (e.g., potential mis-spellings in the dataset).
- Establish controlled vocabularies for species names (Latin vs Common) and for site identifiers.
- Document data provenance, including who produced/edited the data, versioning, and any transformations (cleaning, normalization, or calculations).

## Data Governance and Sharing
- Align dataset with an overarching data governance plan: ownership, access rights, and publication metadata.
- Capture and publish data lineage: raw measurements, QA steps, and the exact formula used for concentration ratios.
- Include data availability statements and any embargo or disclosure considerations related to site locations or sensitive information.
- Ensure data are uploaded to relevant portals/catalogues with proper metadata and discoverability.

## Access, Updates, and Maintenance
- Define update cadence for new samples or re-measurements and ensure updates propagate to catalogs.
- Maintain changelog and version history to track revisions to field definitions or computed ratios.
- Validate incoming data against the data dictionary and run automated quality checks before publishing.

## Challenges to Anticipate
- Incomplete user needs or unclear requirements for metadata completeness.
- Timely ingestion from multiple sources and formats.
- Variability in data formats across different systems and the presence of large datasets.
- Legacy databases requiring bespoke interoperability solutions.
- Ensuring that all metadata fields (especially units and methods) remain consistent across updates.

## Recommendations for Data Stewards
- Implement a formal data dictionary upgrade to standardize field names, units, and definitions.
- Require explicit units for all concentration measurements and ratios; document detection limits and QA procedures.
- Apply controlled vocabularies for species names and sites; enforce validation rules during ingestion.
- Automate data validation and quality assurance checks (consistency between Bee concentration and Soil Dry Mass, plausible value ranges, handling of < values).
- Provide clear data provenance and processing documentation, including the ratio calculation formula and any adjustments.
- Create user-focused documentation and discoverable metadata to support dataset discovery and reuse.
- Establish a clear data sharing plan, including where datasets are published and how updates are communicated to users.