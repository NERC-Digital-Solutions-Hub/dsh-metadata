# TREE_Northumbria_ICPMS_Deer_Whole_Organism_FM_Concentration

## Scope and purpose
- Dataset containing concentrations of multiple elements in deer whole-organism tissue using ICP-MS, expressed as mg/kg fresh mass.
- Includes metadata to support discovery and reuse: species (Latin and common names), sampling site, date of collection, UK Centre for Environment and Health (CEH) sample codes and descriptions, and notes on tissues used.

## Dataset structure and fields
- Metadata fields:
  - Latin_Species_Name, Common_Species_Name
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Notes (tissues used to calculate whole-organism concentrations)
- Concentration fields (example pattern: Element_mg_kg_whole-organism_FM or similar; units consistently mg/kg):
  - I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - Some elements have dual columns (e.g., Ba_mg_kg_whole-organism_FM, 2; Tl_mg_kg_whole-organism_FM, 2) or markers for censored values (e.g., <Be, <Ni, <Mo, <Ag, <U)
- Notable data formatting quirks:
  - Occasional typographical inconsistencies in field names (e.g., Mn_mg_kg_wholebod y_FM) and spacing (e.g., "whole- organism" vs "whole-organism")
  - Presence of less-than markers indicating upper-bound values

## Data encoding and quality considerations
- Concentrations are reported in mg/kg fresh mass.
- Censored values indicated with “<” should be treated as upper bounds in analyses.
- Metadata tied to UKCEH sampling codes facilitates traceability and provenance.
- Tissue notes provide context for how whole-organism concentrations were derived.

## Metadata provenance and notes
- Notes field captures details about tissues used and any methodological considerations affecting calculation of whole-organism concentrations.

## Governance, sharing, and updates
- Data should be uploaded to the appropriate data portals and cataloged with the associated CEH codes and descriptions.
- Respect any sharing limitations, disclosures, or embargoes; ensure mechanisms exist for updates and versioning.
- Documentation of data processing and any transformations may be beneficial to support reuse.

## Practical challenges for data stewards
- Incomplete user needs and priorities may misalign metadata and dataset usability.
- Timely submission of data from creators and adherence to metadata standards (especially for metadata like tissue details and sample descriptions) can be difficult.
- Managing cross-system and cross-format interoperability given varied data structures and potential legacy database formats.
- Handling very large datasets and updates from multiple sources, including older or non-interoperable databases.