# TREE_Northumbria_ICPMS_Woodmice_FM_Concentration

## Purpose and scope
- Dataset listing concentrations of multiple elements in wood mice tissues using ICP-MS, on a fresh mass basis (FM).
- Aimed at environmental monitoring and policy performance evaluation through standardized, comparable outputs.

## Dataset structure and key fields
- Metadata
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
  - Notes on data applicability (e.g., “n/a” placeholders)
- Analyte concentrations (mg/kg_FM)
  - I, Li, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - Some columns indicate less-than values (e.g., <I, <Al, <V, etc.)
  - Several entries include tissue-specific contexts (e.g., “Tissue containing thyroid”)
- Data completeness notes
  - No data for Hind Leg Bone and woodmouse 8 liver
  - “<marker is used to identify concentration given in column …” indicating censored/upper-bound data
  - Some fields show variations like “1 = mg/kg, 2 = fresh mass” for certain analyte entries

## Measurement details
- Concentrations expressed as mg/kg_FM (milligrams per kilogram fresh mass)
- Indicators for censored data where actual values are below detection or reporting thresholds
- Some measurements are linked to specific tissues (e.g., thyroid-containing tissue contexts)

## Data quality, standardisation, and accessibility
- Reflects a standardised approach suitable for verification, quality assurance, cleaning, and transformation
- Outputs are designed to be presented as clear reports, maps, and charts
- Datasets are stored/uploaded to appropriate portals to facilitate access by others

## How this supports environmental monitoring
- Enables consistent cross-site and temporal comparisons of metal exposure in small mammals
- Supports assessment of environmental health and policy performance through standardized metrics and metadata
- Encourages integration with other monitored datasets to enhance data value beyond single-use applications

## Data handling and provenance
- Includes UKCEH sample codes and descriptions to trace samples
- Metadata covers sampling site, date, tissue, and morphological ratios (fresh/dry mass)
- Clear note of data gaps and limitations to inform interpretation and further data collection efforts