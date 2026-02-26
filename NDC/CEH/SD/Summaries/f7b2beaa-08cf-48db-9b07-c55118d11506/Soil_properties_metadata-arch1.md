# Soil chemical properties from a field experiment in the Conwy Valley, North Wales, UK (20156) Metadata for Soil_properties.csv

- Purpose and scope
  - Metadata for a soil-properties dataset from a field experiment in the Conwy Valley, North Wales (UK), 2016.
  - Describes experimental design, sampling regime, analytical methods, data structure, and quality control to support data reuse and analysis.

- Experimental design and sampling regime
  - Three 75-meter-long transects located across the hillslope, spaced ~20 meters apart and running perpendicular to a river.
  - Along each transect, intact soil cores were extracted at 2, 12, and 75 meters.
  - Intact cores collected as 1-meter lengths, with total cores n = 18 (details depend on depth and core length description).
  - Maximum sampling depth determined by soil profile or an impermeable boundary identified via a geophysical survey.

- Collection methods
  - Intact soil cores gathered with a Cobra percussion hammer corer.
  - Core lengths and storage described to maintain core integrity; cores stored at 4°C before analysis.

- Fieldwork and laboratory instrumentation
  - Field tools: Cobra percussion hammer corer.
  - Laboratory instruments include:
    - Gravimetric soil water content (24 h, 105°C).
    - Loss on ignition (OM) at 450°C for organic matter.
    - pH and EC measured in 1:2.5 soil:deionised water suspension.
    - Various chemical analyses performed on extracts (NH4-N, NO3-N, PO4-P).
    - TruSpec elemental analyzer for total C (TC) and N (TN).
    - Multi N/C 2100 TOC analyzer for dissolved organic C (DOC) and total dissolved N (TDN).
    - Microbial biomass C and N by chloroform fumigation.
    - High-throughput PLFA analysis (96-well format).
    - Phosphorus sorption experiments using 33P with liquid scintillation counting.

- Analytical methods
  - NH4-N and NO3-N: colorimetric methods (Mulvaney 1996; Miranda et al. 2001) in 0.5 M K2SO4 extracts (1:5 w/v).
  - Available P: ascorbic acid-molybdate blue method after extraction with 0.5 M acetic acid (Murphy and Riley 1962).
  - TC and TN: TruSpec elemental analyzer.
  - DOC and TDN: 1:5 soil to 0.5 M K2SO4 extracts analyzed by TOC.
  - Microbial biomass C and N: chloroform fumigation (72 h; k_ec = 0.45; k_en = 0.54).
  - PLFA: high-throughput method (Buyer and Sasser 2012).
  - P sorption: 1 g soil shaken with 0.01 M CaCl2 and known P concentrations (including 33P tracer) to derive adsorption; isotherms analyzed via Langmuir equation.
  - P sorption parameters estimated to determine adsorption maxima (Pmax).

- Nature and units of recorded values
  - Values correspond to the column names described in the dataset (see Details of data structure).
  - Units include pH, µS/cm for EC, percent for MC and LOI, mg/g or mg/kg for various nutrients, g/kg for TC/TN, and other dataset-specific units.
  - Empty cells indicate no data.

- Quality control
  - All samples analyzed in triplicate.

- Miscellaneous supporting documents
  - Plot_locations.csv: details of plot locations.
  - Plot_locations_metadata.rtf: description of Plot_locations.csv.

- Details of data structure
  - Columns include: Transect, Row, Depth (cm), pH, EC (µS/cm), MC (%), LOI (%), TOC (mg/g), TDN (mg/g), Microbial_C (mg/g), Microbial_N (mg/g), PO4_P (mg/kg), NH4_N (mg/kg), NO3_N (mg/kg), CtoN_ratio, TC (g/kg), TN (g/kg), Pmax (mg/kg), NH4Adsorp (mg/kg).
  - Some entries may be missing (empty cells) where data were not obtained or applicable.