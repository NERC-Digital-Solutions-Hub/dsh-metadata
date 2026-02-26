# TREE_Northumbria_ICPMS_Vole_FM_Fresh_Mass_Concentration

## Overview
- Dataset describing fresh-mass concentrations of multiple elements in vole samples (Northumbria, UK) analyzed by ICP-MS.
- Focuses on enabling data discovery, combination, analysis, and self-serve exploration through data products (dashboards, pivot tables, reports).

## Key Metadata Fields
- Latin_Species_Name: Latin species name; Units and explanation provided.
- Common_Species_Name: Common name; Units and explanation provided.
- Site: Sampling site; explanation provided.
- Date_Sample_Collected: Date the sample was collected; explanation provided.
- CEH_Sample_Codes: UKCEH sample codes; explanation provided.
- Sample_Details: Sample preparation details; explanation provided.
- CEH_Sample_Description: UKCEH sample description; explanation provided.
- Tissue: Notes on vole preparation (e.g., whether separate tissues were prepared).
- Fresh_Mass_Ash_Mass_Ratio: Ratio of whole animal fresh mass (excluding gut and pelt) to ash mass.
- I_mg_kg_FM to U_mg_kg_FM: Concentrations of elements in mg/kg fresh mass, covering a wide suite of elements.
  - Included elements: I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U.
  - Notes on < (less-than) values appear for some elements (e.g., <Be, <Ag, <U) to indicate concentrations below a reporting threshold.
- Units: All concentration measurements are mg/kg of fresh mass (mg/kg_FM).

## Primary Data Structure
- Wide-range panel of elemental concentrations measured per sample alongside rich metadata (species, site, date, sample codes, tissue, preparation details).
- Concentrations are reported as mg/kg_fresh_mass, with explicit handling notes for values reported as "<" a threshold.
- Comprehensive data dictionary-like descriptions accompany each column to aid interpretation and data quality checks.

## Data Use and Applications
- Supports cross-sample comparisons of vole contaminant profiles across sites and times.
- Enables creation of dashboards, pivot-table analyses, and self-serve reports to explore:
  - Species and site-level patterns
  - Elemental concentration distributions and outliers
  - Relationships between sample preparation details (e.g., tissue type) and element concentrations
  - Mass ratio analyses (Fresh Mass vs. Ash Mass) in relation to element concentrations
- Facilitates data quality workflows, including verification of data formats, unit consistency, and handling of less-than values.

## Challenges and Considerations
- Data availability may be patchy and presented in a wide range of formats across datasets.
- Communication of complex metadata (e.g., sample preparation, tissue notes) may require careful interpretation for end users.
- Less-than values need consistent treatment in analyses and visualisations.

## How This Supports Data Use
- Provides a well-documented schema for a rich ICP-MS vole dataset, enabling researchers and analysts to locate, clean, combine, and analyse data efficiently.
- Supports reproducible analysis and the creation of user-friendly data products to share insights with broader audiences.