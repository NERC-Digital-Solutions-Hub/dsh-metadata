# Predatory Bird Monitoring Scheme

## Overview
- Data produced by the Predatory Bird Monitoring Scheme (PBMS) for long-term temporal trend analysis.
- Contains contaminant concentrations in predatory bird samples, primarily from eggs (homogenised egg contents) and, for some measures, liver (wet weight basis; dry weight basis for some metals).
- Aims to support analyses of correlations, trends, and potential impacts of contaminants on birds.

## Data structure and fields
- Sample identifiers and context
  - Egg number (unique identifier; numbering may be numeric or alphanumeric due to changes over years)
  - Year (four-digit year indicating when the egg was laid)
  - Location (general nest site location)
  - Shell Index (indicator of eggshell thickness; as described by Ratcliffe)
  - CF (lipid concentration correction factor; to convert to lipid-based concentrations where applicable)
- Contaminants and measurements
  - Pesticides/OC toxins: HCB (hexachlorobenzene); a-HCH and g-HCH (alpha and gamma hexachlorocyclohexane); p,p-DDE; p,p-TDE; p,p-DDT; HEOD; p,p-TDE
  - PCBs: Total PCB (sum of peaks as defined; excluding some identified OC peaks), and numerous individual congeners (PCB 8, PCB 18, PCB 28, PCB 29, PCB 31, PCB 52, PCB 77, PCB 101, PCB 105, PCB 114, PCB 118, PCB 123, PCB 126, PCB 128, PCB 138, PCB 141, PCB 149, PCB 153, PCB 156, PCB 157, PCB 163, PCB 167, PCB 169, PCB 170, PCB 171, PCB 180, PCB 183, PCB 187, PCB 189, PCB 194, PCB 199, PCB 201, PCB 205, PCB 206, PCB 209)
  - Toxicity measure: TEQ (Toxic Equivalencies) calculated using 1997 WHO TEFs for planar/coplanar PCBs (reported per liver wet weight)
  - Metals and metalloids (concentrations in homogenised egg contents; and/or liver on a dry weight basis): Al, As, Cd, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Sb, Se, Zn
- Data quality flags and reporting conventions
  - ND = None Detected
  - NA = Not Analysed
  - Some fields explicitly note “in homogenised egg contents” or “per g of liver on a wet weight basis” to indicate units and matrix
  - Total PCB and TEQ values are derived using specified methods and standards (e.g., TEFs for PCBs)

## Contaminants and measurements (highlights)
- Organochlorines and pesticides: HCB, a-HCH, g-HCH, p,p-DDE, p,p-TDE, p,p-DDT, HEOD
- PCBs: Total PCB plus a broad panel of congeners (8, 18, 28, 29, 31, 52, 77, 101, 105, 114, 118, 123, 126, 128, 138, 141, 149, 153, 156, 157, 163, 167, 169, 170, 171, 180, 183, 187, 189, 194, 199, 201, 205, 206, 209)
- Toxicity metric: TEQ (pg/g liver wet weight)
- Metals and metalloids: Al, As, Cd, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Sb, Se, Zn
- Shell Index and CF used for contextual and normalization purposes

## Availability and access
- Results and reports are downloadable from the PBMS website: http://pbms.ceh.ac.uk/results.htm
- Data are intended to support long-term trend analyses and cross-sample comparisons
- Each record includes the sample matrix (egg contents or liver) and units appropriate to that matrix

## Data quality, interpretation, and caveats
- Many fields use ND or NA, reflecting not detected or not analysed for particular samples or contaminants
- Units vary by contaminant and matrix (egg contents vs liver; wet weight vs dry weight; lipid-normalized via CF)
- The dataset is designed for robust trend analysis but requires careful harmonization across years, sites, and sample types
- The extensive list of PCB congeners and the TEQ calculation rely on standardized reporting conventions and TEFs (as cited in the documentation)

## Practical guidance for analysts
- Prepare for matrix-specific units: eggs (in homogenised egg contents) versus liver (wet/dry weight basis); apply CF where lipid normalization is needed
- Treat ND/NA values appropriately (censoring, imputation, or substitution consistent with analysis plan)
- Use TEQ values with the defined WHO TEFs for comparative toxicity assessment
- Leverage the Year, Location, and Shell Index fields to explore spatial and temporal trends in contaminant burden and eggshell integrity
- Cross-reference with the long-term PBMS results for trend analyses and to track changes in contaminant profiles over time
- Ensure data provenance by consulting the PBMS results portal for methodology notes and dataset metadata

## Notes
- The document functions as a comprehensive data dictionary accompanying the PBMS long-term trend reports, detailing column definitions, units, and data status to support rigorous analytical work.