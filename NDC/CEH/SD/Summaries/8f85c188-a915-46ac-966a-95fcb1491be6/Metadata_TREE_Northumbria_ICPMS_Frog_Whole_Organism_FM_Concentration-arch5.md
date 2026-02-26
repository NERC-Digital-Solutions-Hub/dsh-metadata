# TREE_Northumbria_ICPMS_Frog_Whole_Organism_FM_Concentration

## Overview
- Dataset detailing concentrations of multiple elements in frog whole-organism samples (fresh mass) from Northumbria ICP-MS analyses.
- Focus on metal/metalloid concentrations across various species, sites, and sampling events; UKCEH sample descriptions referenced.

## Dataset Scope and Content
- Sample identifiers and metadata:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Description
  - Notes (tissues used to calculate concentrations)
- Concentration measurements (mg/kg; fresh mass):
  - I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
- Some columns indicate nondetects using a less-than symbol (<), e.g., Be_mg_kg_whole_organism_FM, Ni_mg_kg_whole_organism_FM, U_mg_kg_whole_organism_FM.
- Note: One column entry shows "Not calculated" for I_mg_kg_whole_organism_FM in its explanation.

## Metadata and Provenance
- Dataset uses fresh mass basis (mg/kg) for concentrations.
- Includes field-level explanations for each concentration column, clarifying units and interpretation (e.g., nondetects).
- References to UKCEH sample descriptions and general sampling context (Site, Date, Notes).

## Data Quality and Standards
- Unit consistency: mg/kg across most concentration columns; some units metadata listed as n/a in certain header fields.
- Field naming includes occasional formatting irregularities (e.g., spacing in "_FM" segments) but overall semantics are clear.
- Nondetects indicated with < values; requires consistent handling in analyses.
- Metadata present for sample context (species, site, date, tissue notes) to support traceability.

## Data Sharing and Governance Considerations
- Data Stewards should ensure:
  - Metadata completeness and clarity (species, site, date formats, notes about tissues).
  - Standardized units and mass basis across all datasets and portals.
  - Consistent handling and documentation of nondetects (< values).
  - Clear data provenance: source descriptions (CEH_Sample_Description) and sample notes.
  - Dataset uploading to appropriate portals and catalogues; track updates and versioning.
  - Documentation of any calculations or transformations applied to raw data (e.g., how concentrations were derived from tissues).

## Challenges and Risk Areas
- Incomplete user needs or expectations regarding dataset scope and interoperability.
- Timely receipt of data from contributors and adherence to standards (metadata, formats).
- Integration with multiple systems/formats and handling very large datasets.
- Potentially outdated databases requiring bespoke, non-interoperable solutions.

## Actions and Recommendations for Data Stewards
- Develop and enforce a concise data dictionary covering all fields, units, and nondetect conventions.
- Standardize species naming, site identifiers, date formats, and tissue description conventions.
- Implement a consistent policy for nondetect values and < notation across portals.
- Ensure provenance and lineage are documented for each dataset (source, sample description, notes).
- Create governance workflows for data intake, quality checks, and update cycles.
- Facilitate alignment with broader data governance standards to support discoverability and reuse.