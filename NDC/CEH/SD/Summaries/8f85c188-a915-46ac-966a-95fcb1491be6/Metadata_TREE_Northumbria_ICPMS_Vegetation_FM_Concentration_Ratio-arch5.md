# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration_Ratio

## Overview
- A dataset describing concentration ratios of various elements in vegetation relative to co-located soil, calculated as Fresh Mass Vegetation divided by Dry Mass Soil.
- Includes taxonomic identifiers for plant species, sampling site and date, and unique CEH sample identifiers and descriptions.
- Captures preparation notes, description of related soil sample used to compute the ratio, and indicators for less-than concentration values.
- Designed to support data discovery, governance, and reuse within large datasets and networks.

## Data structure and key fields
- Species identifiers:
  - Latin_Species_Name
  - Common_Species_Name
- Location and timing:
  - Site
  - Date_Sample_Collected
- Sample metadata:
  - CEH_Sample_Identifier
  - CEH_Sample_Description
  - Notes (preparation/handling notes)
- Calculation context:
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
  - I_Concentration_Ratio (and similarly prefixed fields) indicating concentration ratio values for various elements
- Element concentration ratios:
  - Ca_Concentration_Ratio, Ti_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio, and others indicated in the table.
  - For several elements, there are sub-fields indicated as “1” and “2” (e.g., Ca_Concentration_Ratio, 1 and Ca_Concentration_Ratio, 2) describing the data state; some entries include marker semantics such as < indicating a threshold value.
- Notation and semantics:
  - <I, <Li, <Be, etc., denote concentration ratio values that are 'less than' a threshold, with corresponding explanatory fields detailing the meaning.
  - Where present, units are noted as n/a; many fields embed explicit definitions (e.g., “Concentration Ratio (Fresh Mass Vegetation divided By Dry Mass Soil)”).

## Data quality and standards
- Metadata completeness gaps to address:
  - Consistent units and data types across all concentration ratio fields (currently many show n/a for units).
  - Standardized naming for species (Latin vs Common) and consistent site naming.
  - Explicit data provenance and collection dates in a uniform format.
- Quality considerations:
  - Ensure accuracy and consistency of concentration ratio calculations using correctly paired vegetation and soil samples.
  - Validate handling of less-than markers to preserve data integrity during import, analysis, and sharing.
  - Documentation of preparation steps and any deviations across samples.
- Documentation needs:
  - Clear guidance on each element’s unit, measurement method, and quality checks to accompany the concentration ratio fields.

## Data governance and sharing
- Data ownership and provenance:
  - Ties to CEH sample identifiers and vegetation/soil pairings; co-located soil samples used for ratio calculations must be traceable.
- Access, embargo, and licensing:
  - Clarify any restrictions on soil-related data, sample descriptions, or proprietary methods; ensure appropriate licenses accompany the dataset.
- Update and maintenance:
  - Establish versioning and update cycles for new sampling events, re-calculations, or corrected identifiers.
- Portal and catalogue considerations:
  - Ensure compatibility with data portals/catalogues requiring consistent metadata schemas, with clear mappings for Latin/Common names, site codes, and sample IDs.

## Ingestion, curation and workflow
- Data reception:
  - Receive vegetation concentration ratio records with accompanying notes and soil co-sample references.
- Quality assurance and transformation:
  - Validate field presence, data types, and value ranges; standardize species names; harmonize site identifiers; verify date formats.
  - Resolve less-than markers and ensure consistent encoding across all concentration ratio fields.
- Upload and documentation:
  - Upload to relevant data portals/catalogues with accompanying metadata and provenance notes.
  - Document data provenance, processing steps, and any transformations or assumptions applied.

## Interpretation and usage notes
- Purpose of concentration ratios:
  - Indicate the uptake or accumulation of elements in vegetation relative to the soil baseline, aiding comparative studies across sites and species.
- Important caveats:
  - Less-than values indicate detection limits or thresholds; interpretation should account for these bounds.
  - Data quality and comparability depend on consistent sampling, preparation, and calculation conventions; ensure metadata-driven understanding of any deviations.

## Challenges and mitigation (aligned to Data Stewards’ typical concerns)
- Incomplete user needs and priorities:
  - Engage data users to confirm required fields, units, and preferred naming conventions; document any deviations.
- Timeliness of data:
  - Implement clear data submission windows and prompt QA processes to minimize delays.
- Metadata completeness and standardization:
  - Mandate comprehensive metadata for species, site, samples, and preparation; enforce standardized vocabularies.
- Diverse systems and formats:
  - Normalize data into a consistent schema before sharing; maintain mappings to source systems.
- Large datasets and transfer:
  - Plan scalable storage and transfer strategies; optimize for efficient loading and querying.
- Outdated or bespoke databases:
  - Prefer interoperable, well-documented data models; maintain backward-compatible mappings and clear migration plans.