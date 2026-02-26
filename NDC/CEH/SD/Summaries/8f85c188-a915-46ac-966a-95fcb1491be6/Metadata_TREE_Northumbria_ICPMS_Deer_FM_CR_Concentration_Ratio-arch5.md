# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration_Ratio

## Overview
- Metadata schema for a woodmice ICPMS concentration ratio dataset (Fresh Mass Woodmice divided by Dry Mass Soil).
- Captures taxonomic information, sampling context, and a comprehensive set of elemental concentration ratios.
- Indicates that many fields have no specified units (n/a) and that some concentration values may be reported as “less than” values.

## Key fields and purpose
- Latin_Species_Name: Latin name of species.
- Common_Species_Name: Common name of species.
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- CEH_Sample_Description: Description of the CEH sample.
- Notes: Additional notes for the Woodmice sample.
- Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: Description of the soil sample used to compute the ratio.
- I_Concentration_Ratio: Concentration ratio indicator (and related format guidance for less-than values).
- Elemental Concentration Ratios: Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U, etc. Each represents the ratio: Fresh Mass Woodmice (wholebody) divided By Dry Mass Soil.
- Notation details: Some entries use a “<” marker to indicate a less-than value; some fields include dual indexing (e.g., 1 and 2) for specific concentration ratio representations.
- Units: Generally indicated as n/a for these concentration ratio fields.

## Data governance and quality considerations
- Data standards: Metadata and field definitions should be consistent with a shared data schema; ensure uniform species naming, site identifiers, sampling dates, and soil context.
- Calculation traceability: Ratio method must be documented and reproducible (Woodmice fresh mass ÷ soil dry mass).
- Metadata completeness: Ensure CEH sample descriptions and notes are sufficiently detailed to interpret results.
- Availability and updates: Establish clear data-sharing permissions, embargo rules if any, and update mechanisms for new samples and revised calculations.
- Documentation: Record any data processing or transformations performed before sharing.
- Portal deposition: Upload to appropriate data portals and catalogue holdings with proper metadata so datasets are discoverable and usable.

## Particular challenges for data stewardship
- Incomplete understanding of user needs for dataset use and discovery.
- Timely acquisition of data from creators and suppliers.
- Getting data creators to meet metadata and standardization requirements (e.g., species names, site details, CEH descriptions).
- Handling multiple systems and formats, including legacy or non-interoperable data.
- Managing large datasets with numerous elemental ratios and potential file transfer constraints.
- Working with outdated databases that require bespoke solutions to maintain interoperability.

## Recommendations for action (Data Steward focus)
- Define and enforce a minimal metadata template aligned with organizational standards (taxonomy, site, date, sample descriptions, co-located soil context).
- Require explicit documentation of the calculation method for all concentration ratios and capture any less-than values with appropriate flags.
- Implement data validation rules to ensure consistency across all elemental ratio fields and correct handling of n/a and less-than indicators.
- Coordinate with data creators to obtain complete and timely metadata, including soil sample context and date of collection.
- Establish data update workflows and determine embargo/sharing restrictions upfront.
- Ensure data are uploaded to the designated data portals with complete cataloging and accessible documentation.
- Maintain an audit trail of data processing steps and provide clear, user-focused dataset documentation.