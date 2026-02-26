# TREE_Northumbria_ICPMS_Vegetation_FM_Concentration

## Purpose and Scope
- Data header for ICP-MS concentration measurements in vegetation samples (Northumbria) used to monitor environmental health and inform policy decisions.
- Captures both biological metadata (species) and sampling details (site, date) as well as extensive elemental concentration data.

## Metadata Fields
- Latin_Species_Name: Latin botanical name of species sampled.
- Common_Species_Name: Common name of species sampled.
- Site: Sampling site identifier.
- Date_Sample_Collected: Date the sample was collected.
- CEH_Sample_Identifier: UKCEH sample identifier.
- CEH_Sample_Description: Description of the UKCEH sample.
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass for the sample.
- <I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U>_mG_kg_FM: Concentrations of each element reported in milligrams per kilogram of fresh mass.
- Units and Explanations: For each element, a corresponding Units and Explanation field clarifies that values represent concentration in mg/kg (fresh mass) and what the column denotes.
- Notation for below-detection values: Columns may include a leading "<" to indicate "less than" the reported value.

## Concentration Measurements
- Concentrations reported for a wide suite of elements, including I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
- All concentrations are expressed as mg/kg of fresh mass (FM) where applicable.
- Some columns use a single-letter prefix (e.g., <I, <Li) to denote below-threshold values; these are flagged as less than the stated quantity.

## Data Handling and Quality
- Metadata completeness: The header supports rich metadata essential for data usability and traceability.
- Data transformations: The schema anticipates needs for cleaning and transforming data to support analysis and reporting.
- Handling below-detection values: "<" notation requires clear interpretation during analysis.
- Data provenance: CEH sample identifiers and descriptions aid traceability back to origin.
- Missing information: Occurrences of n/a indicate areas where information is not available in this dataset.

## Data Governance, Access, and Interoperability
- Open sharing considerations: While data sharing supports transparency, publicly sharing underlying datasets can be a barrier for some data.
- Metadata quality: Adequate metadata is critical to verify suitability for use and to enable cross-site comparisons.
- Silo reduction and standardization: The breadth of data fields underscores the need to harmonize datasets across organisations to minimize silos and improve interoperability.
- Governance needs: Establishment of data quality checks, storage, versioning, and clear provenance to ensure datasets meet standards and remain up to date.

## Relevance for Authors of Monitoring Frameworks
- Provides a concrete template for structuring environmental health monitoring data, including both sample metadata and multi-element concentration measurements.
- Demonstrates essential considerations for policy-relevant monitoring: data completeness, metadata clarity, measurement units, handling of non-detect values, and governance for sharing and stewardship.
- Highlights practical challenges to address when designing monitoring frameworks, such as data standardization, access barriers, and the need for robust data governance.