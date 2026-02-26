# Predatory Bird Monitoring Scheme

## Overview
- Dataset from the Predatory Bird Monitoring Scheme (PBMS) used for periodic long-term temporal trend analyses.
- Focuses on contaminant measurements in predatory bird eggs, with potential inclusion of liver-based data.
- Data aims to support monitoring of environmental contaminants and their trends over time.

## Data Content and Structure
- Key identifiers: Egg number (unique per egg; numbering may be numeric or alphanumeric), Year (four-digit), Location (nest site general area).
- Egg quality metric: Shell Index (shell thickness indicator related to pesticide exposure in some studies).
- Data fields capture both the egg contents and, where applicable, liver basis concentrations.
- Contaminant groups included:
  - Organochlorines: HCB, a-HCH, g-HCH, p,p-DDE, HEOD, p,p-TDE, p,p-DDT.
  - PCBs: Total PCB, TEQ (toxic equivalents), plus numerous congeners (e.g., PCB 8, PCB 18, PCB 28, PCB 29, PCB 31, PCB 52, PCB 77, PCB 101, PCB 105, PCB 114, PCB 118, PCB 123, PCB 126, PCB 128, PCB 138, PCB 141, PCB 149, PCB 153, PCB 156, PCB 157, PCB 163, PCB 167, PCB 169, PCB 170, PCB 171, PCB 180, PCB 183, PCB 187, PCB 189, PCB 194, PCB 199, PCB 201, PCB 205, PCB 206, PCB 209, etc.).
  - Metals and other elements: Al, As, Cd, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Sb, Se, Zn.
- Measurement basis and units vary:
  - Some contaminants reported per g of liver on a wet weight basis.
  - Others reported per g of liver on a dry/wet weight basis, or per g of egg contents (homogenate).
  - “NA” or “ND” indicate not analysed or none detected; a variety of entries use these indicators.
- Data completeness:
  - Many fields show NA/ND or Not Analysed, indicating partial data coverage across years and analytes.
- Access:
  - Results and reports are downloadable from the PBMS website (http://pbms.ceh.ac.uk/results.htm).

## Metadata and Access
- The dataset includes a comprehensive data dictionary with column headings and descriptions (e.g., Year, Location, Shell Index, CF, contaminant names, units, and analysis status).
- Describes analytical scope (which analytes were analysed, which were not) and the basis for concentration reporting (egg contents vs liver tissue; wet/dry weight).
- PBMS results page is the primary access point for downloadable reports and accompanying metadata.

## Data Quality and Gaps
- Notable gaps: many analytes marked as NA or ND; inconsistent analysis across years and sites.
- Heterogeneity in units and reporting bases (egg contents vs liver; wet vs dry weight) requiring careful standardization for longitudinal comparisons.
- Limited transparency in some years due to missing data fields and varying analysis status.

## Implications for Data Strategy and Use
- For Data Leaders: treat PBMS as a long-term, multi-analyte monitoring dataset with substantial value for trend analysis but with notable data gaps and heterogeneity.
- Priorities:
  - Standardize reporting units and baselines across years (e.g., harmonize liver vs egg-content reporting and weight basis).
  - Improve metadata completeness to enhance discoverability and reuse (clear mapping of each field, units, and analysis status).
  - Foster co-ownership of data products with policy colleagues and external partners to ensure alignment with user needs.
  - Explore commissioning or integrating additional data to fill granularity gaps and reduce data silos.
- Data governance: maintain versioned datasets, document changes in analysis status (NA/ND) and analytical methods, and ensure results are accessible via the PBMS results page.

## Key Takeaways and Next Steps
- PBMS provides a valuable, long-term view of contaminant trends in predatory birds, with a rich suite of analytes including organochlorines, PCBs, and metals.
- The data dictionary offers essential metadata, but users must navigate incomplete data and varying reporting bases.
- To maximize value, pursue standardization, complete metadata, and coordinated effort to close data gaps, while leveraging the PBMS results platform for ongoing access and updates.