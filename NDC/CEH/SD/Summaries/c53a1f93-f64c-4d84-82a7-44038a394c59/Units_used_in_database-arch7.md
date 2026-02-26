# Please note that the units used in the data base are as listed below.

## Overview
- This document lists the variables in the water chemistry database and the units assigned to each.
- Note: the units shown may differ from the units used by chemical analysts, as documented in Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx.
- The dataset appears to track measurements across multiple sites with identifying fields and qualifiers for many variables.

## Structure and key fields
- Core identifiers:
  - Master_Site
  - Site_Code
  - Date
  - Rep
- Variables and their units (illustrative examples):
  - Ca, Mg, Na, K, Cl, SO4, NO3, NH4, NO2, DOC, pH, Alkalinity
  - Al, Total_N, TON, PO4_P
  - Conductivity (units: us/cm)
  - Si, Fe, Mn, and a broad range of trace elements (e.g., Cr, Ni, Cu, Zn, Pb, U, U, etc.)
  - POM, POC, Salinity, F, Br, TDP, Li, Be, Al27, Sc, V, Se, S, La, Ce, Pr, W, Ti, Sn
- Qualifier fields:
  - Many variables have corresponding Qual fields (e.g., CaQual, MgQual, NO3Qual, etc.) indicating data quality or measurement conditions.

## Data quality and consistency notes
- The units listed in this database may not match the units used in the chemical analyst metadata.
- There is a reference to an external metadata file (Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx) for the analytical methods and unit definitions.
- The dataset uses multiple abbreviations and qualifiers, which can affect interpretation and mapping in GIS.

## Implications for GIS work
- Unit harmonization: Before visualization or spatial analysis, harmonize units to a consistent schema (e.g., convert all concentrations to mg/L or µg/L as appropriate).
- Qualifier handling: Respect Qual fields to indicate data quality, detection limits, or special measurement conditions in maps and analyses.
- Data integration: The database schema includes site-level identifiers (Master_Site, Site_Code) and temporal data (Date), enabling time-series mapping and spatial joins to site geometries.
- Data completeness: Expect incomplete rows and varying data availability across sites and analytes; plan for missing data handling in maps and analyses.
- Metadata alignment: Consult the referenced analytical methods metadata to ensure correct interpretation of units and measurement techniques when integrating with GIS layers.

## Practical GIS workflow recommendations
- Data preparation:
  - Import the dataset and map each variable to a consistent unit system.
  - Create a standardized schema for site-level attributes (Site_Code, Master_Site, Date, Rep) and analyte measurements with corresponding Qual fields.
  - Normalize variables with inconsistent or multiple units; document conversions.
- Mapping and visualization:
  - Build choropleth maps or graduated symbols for key indicators (e.g., NO3, NH4, Ca, Conductivity) by site and date.
  - Use Qual fields to filter or annotate data quality in maps (e.g., display only records with acceptable Qual).
  - Create time-enabled maps or animations to reflect changes over sampling dates.
- Data quality and governance:
  - Maintain a data dictionary that records the final unit standardization decisions and which Qual criteria were applied.
  - Link to the external metadata file for provenance and method-specific notes.
- Validation:
  - Cross-check a sample of site records against the original Metadata_Analytical methods document to confirm unit interpretations and measurement contexts.
  - Flag and review outliers or unexpected unit conversions during GIS processing.

## End notes
- The dataset captures a wide range of chemical and physical parameters relevant to catchment water chemistry, with extensive use of qualifiers to convey data context.
- Effective GIS use hinges on careful unit harmonization, qualifier-aware visualization, and alignment with the referenced analytical metadata.