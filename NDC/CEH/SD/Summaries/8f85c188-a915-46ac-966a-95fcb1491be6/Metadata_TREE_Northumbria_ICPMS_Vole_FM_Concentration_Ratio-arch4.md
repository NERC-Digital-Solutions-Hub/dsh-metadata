# TREE_Northumbria_ICPMS_Vole_FM_Concentration_Ratio

## Overview
- A dataset describing concentration ratios of various elements in vole tissue relative to dry soil, derived from ICP-MS measurements.
- Includes sample metadata (species, site, collection date, CEH identifiers) and notes, plus the soil sample location used to calculate the concentration ratios.
- Primary calculation: Concentration Ratio = Fresh Mass Vole (whole body) divided by Dry Mass Soil.
- Contains ratios for I and numerous elemental concentrations (Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U, and others as labeled), with some entries marked as “less than” values.

## Data Structure and Key Variables
- Taxonomic and sampling metadata
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Code, CEH_Sample_Description
  - Notes
- Sampling and context
  - Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio
  - I_Concentration_Ratio (overall ratio for whole dataset)
- Elemental concentration ratios (per element)
  - Li_Concentration_Ratio, Be_Concentration_Ratio, Na_Concentration_Ratio, Mg_Concentration_Ratio, Al_Concentration_Ratio, P_Concentration_Ratio, K_Concentration_Ratio, Ca_Concentration_Ratio, Ti_Concentration_Ratio, V_Concentration_Ratio, Cr_Concentration_Ratio, Mn_Concentration_Ratio, Fe_Concentration_Ratio, Co_Concentration_Ratio, Ni_Concentration_Ratio, Cu_Concentration_Ratio, Zn_Concentration_Ratio, As_Concentration_Ratio, Se_Concentration_Ratio, Rb_Concentration_Ratio, Sr_Concentration_Ratio, Mo_Concentration_Ratio, Ag_Concentration_Ratio, Cd_Concentration_Ratio, Cs_Concentration_Ratio, Ba_Concentration_Ratio, Tl_Concentration_Ratio, Pb_Concentration_Ratio, U_Concentration_Ratio
- Value formatting notes
  - Some columns labeled with a leading “<” (e.g., <Be_Concentration_Ratio) indicate a “less than” value.
  - Certain fields show duplicated or variant labels (e.g., Ba_Concentration_Ratio, 1 and Ba_Concentration_Ratio, 2; Tl_Concentration_Ratio_1) likely due to formatting inconsistencies.
  - Units for all concentration ratios are n/a (dimensionless ratios).

## Calculation and Measurement Details
- Concentration ratios are calculated as fresh mass vole tissue divided by dry mass soil for each sample.
- Includes both an overall I_Concentration_Ratio and per-element concentration ratios.
- Data notes reflect that some concentration values may be reported as “less than” a threshold; care needed when interpreting these entries.

## Data Quality, Gaps, and Constraints
- Metadata and column naming exhibit inconsistencies and formatting irregularities (e.g., columns with leading “<” symbols, duplicated labels).
- Units are not applicable (dimensionless ratios), which requires careful interpretation alongside site and sample metadata.
- Potential gaps or ambiguities in which soil sample location corresponds to each vole sample, and how the soil sample was chosen for ratio calculation.
- Requires verification of data content and format, and standardization of column labels for consistent downstream use.

## Access, Metadata, and Governance
- The dataset emphasizes cross-site and cross-sample context (soil-sample linkage, collection details), aligning with needs to improve data discoverability, metadata completeness, and traceability.
- Suitable for integration into broader data systems that track species, sampling locations, and environmental metal exposure metrics.
- Governance should address data standardization, handling of censored (<) values, and clear documentation of any formatting quirks.

## Use Cases and Value for Data Leaders
- Environmental monitoring and risk assessment: assess uptake of metals by small mammals relative to soil, informing ecological and public health analyses.
- System-level data planning: integrate with other data assets (soil metal concentrations, habitat data, policy-related datasets) to support end-to-end data strategies.
- Data quality improvement: identify and address metadata gaps, standardize naming conventions, and establish processes for recording and sharing censored values.
- Collaboration and co-ownership: enable stakeholders (policy teams, researchers, external partners) to access a well-documented data asset with clear lineage and calculation methods.

## Practical Guidance for Data Leaders
- Prioritize metadata completion: document site mappings, soil sampling methodology, and exact definitions for each concentration ratio column.
- Standardize column naming: resolve inconsistent labels (e.g., Be_Concentration_Ratio vs. <Be_Concentration_Ratio) and reconcile duplicated Ba/Tl/Ti entries.
- Establish data quality controls: handle less-than values appropriately, decide on imputation vs. reporting thresholds, and audit sample-to-soil linkage.
- Ensure discoverability and access: create a data dictionary, versioning, and clear provenance to support wider reuse by partners and policy stakeholders.