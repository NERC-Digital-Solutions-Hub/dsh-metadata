# This data has been generated as part of Predatory Bird Monitoring Scheme which periodically produces long term temporal trend analysis of this data.

## Overview
- Contaminant data collected under the Predatory Bird Monitoring Scheme (PBMS), designed for long-term temporal trend analysis.
- Reports and underlying data available for download from the PBMS website.
- Data supports monitoring exposure to pesticides and persistent organic pollutants in predatory birds.

## Data content and scope
- Data structure includes long-running datasets with measurements taken from predatory birds (eggs and related tissues).
- Key sample types mentioned: homogenised egg contents and liver (for certain analytes), with some measurements in egg contents and others in liver on different weight bases.
- The dataset covers a wide range of contaminants, including:
  - Hexachlorobenzene (HCB)
  - Hexachlorocyclohexane isomers (a-HCH, g-HCH)
  - DDE and related DDT metabolites (p,p-DDE, p,p-DDT, p,p-TDE)
  - Heptachlorinated and nonachlorinated PCB congeners (e.g., PCB 8, PCB 18, PCB 28, PCB 52, PCB 77, PCB 101, PCB 105, PCB 114, PCB 118, PCB 123, PCB 126, PCB 128, PCB 138, PCB 141, PCB 149, PCB 153, PCB 156, PCB 157, PCB 163, PCB 167, PCB 169, PCB 170, PCB 171, PCB 180, PCB 183, PCB 187, PCB 189, PCB 194, PCB 199, PCB 201, PCB 205, PCB 206, PCB 209, and total PCB)
  - Toxic Equivalents (TEQ) calculated from planar/coplanar PCB congeners using 1997 WHO TEFs (per Van den Berg et al., 1998)
  - Additional elements/metals: Al, As, Cd, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Sb, Se, Zn
- The dataset includes both aggregated metrics (Total PCB, TEQ) and individual congener measurements (e.g., PCB 8, PCB 18, PCB 28, etc.).
- Column descriptions indicate data can include fields such as Egg number (unique identifier), Year (year of egg lay), Location (nest site), Shell Index (eggshell thickness proxy), and CF (lipid-adjustment factor).

## Key variables and measurement details
- Egg number: unique identifier for each egg (nomenclature may vary across years).
- Year: year the egg was laid; some rows may have Not Applicable values.
- Location: general nest site location (spatial context for trend analysis).
- Shell Index: indicator of eggshell thickness (as described in literature cited in the data dictionary).
- CF: conversion factor to convert concentrations to lipid-based values.
- Analyte measurements (examples include):
  - HCB, a-HCH, g-HCH
  - p,p-DDE, p,p-DDT, p,p-TDE
  - HEOD, p,p-TDE
  - Total PCB and individual PCB congeners (e.g., PCB 8, PCB 18, PCB 28, PCB 52, PCB 77, PCB 101, PCB 105, PCB 114, PCB 118, PCB 123, PCB 126, PCB 128, PCB 138, PCB 141, PCB 149, PCB 153, PCB 156, PCB 157, PCB 163, PCB 167, PCB 169, PCB 170, PCB 171, PCB 180, PCB 183, PCB 187, PCB 189, PCB 194, PCB 199, PCB 201, PCB 205, PCB 206, PCB 209, etc.)
  - TEQ: Toxic Equivalencies (per WHO TEFs for birds)
  - Al, As, Cd, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Sb, Se, Zn
- Measurement basis and units (as described in the data dictionary):
  - HCB, a-HCH, g-HCH, p,p-DDE, HEOD, p,p-TDE, p,p-DDT: concentrations reported as ng/g or similar, with liver on a wet weight basis where specified.
  - Total PCB and individual congeners: concentrations reported per g of liver on a wet weight basis.
  - TEQ: pg/g of liver on a wet weight basis.
  - Al, As, Cd, Co, Cu, Fe, Hg, Mn, Mo, Ni, Pb, Sb, Se, Zn: concentrations reported in homogenised egg contents; for some elements the data are NA (Not Analysed) or ND (None Detected). For some elements (Al, etc.), liver concentrations may be reported on a dry weight basis.
- Data completeness:
  - Many fields marked NA (Not Analysed) or ND (None Detected) in the provided extract.
  - Some years/samples may lack certain measurements; numbering and data availability may vary across years.

## Access, provenance and usage notes
- Primary data and reports: PBMS website (http://pbms.ceh.ac.uk/results.htm).
- Data is intended to support long-term trend analyses and public-facing reporting of contaminant exposure in predatory birds.
- The dataset uses a mix of tissue types (eggs and liver) and weight bases (wet/dry) with lipid-adjustment through CF to enable cross-analyte comparisons.
- Important caveats for data use:
  - “Not Analysed” and “None Detected” values are common; handle missing data appropriately.
  - Egg numbering and site metadata may have inconsistencies across years.
  - Some measurements are lipid-adjusted via CF—ensure correct interpretation when comparing across tissues or analytes.

## Data quality, gaps and caveats
- Patchy data coverage across years and sites can complicate trend analysis.
- The presence of many Not Analysed (NA) and None Detected (ND) entries indicates incomplete analytical coverage for numerous analytes.
- Units and basis (wet weight vs. dry weight vs. lipid-adjusted) vary by analyte; careful unit harmonisation is required for cross-analyte comparisons.
- The data dictionary-style presentation suggests the need for careful data cleaning and documentation when integrating into dashboards or analyses.

## How this data supports insights and data products
- Enables visualization of temporal trends in contaminant exposure in predatory birds, at both egg and tissue (liver) levels.
- Supports lipid-adjusted comparisons across a broad panel of organochlorines (PCBs, DDT metabolites, HCH isomers, HCB) and emerging contaminants.
- Facilitates regional comparisons via Location and Year, potentially informing conservation and policy decisions.
- The data dictionary informs data product development (dashboards, pivot-style reports) by clarifying variable meanings, measurement bases, and units, aiding self-serve analysis.
- Provides a foundation for calculating TEQ-based risk assessments using established TEFs for birds.