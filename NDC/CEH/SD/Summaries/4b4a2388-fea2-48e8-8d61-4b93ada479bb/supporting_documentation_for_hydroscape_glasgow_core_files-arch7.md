# Headings used to record the stratigraphic data collected for each core

## Overview
- Describes the data structure and headings used to record stratigraphic data for each lake/core.
- Associated files consist of multiple CSVs (WBID and project code in filenames).
- The data are organized as a matrix with columns (determinands) and rows (contiguous core-depth intervals).
- Blanks indicate no measurement recorded for that interval.

## Data schema (core fields)
- Core identification and depth
  - Sub_ID: internal unique ID for core slice
  - Top_Depth_cm: distance to top of sliced core section from sediment/water interface
  - Bottom_Depth_cm: distance to bottom of sliced core section from sediment/water interface
- Mass and composition
  - Mass of sediment following drying at 105°C for 24 hours (DW)
  - Wetd: mass (g) of 1 cm³ of wet sediment
  - LOI 550: carbonate content (%) by combustion at 550°C
  - LOI 950: additional LOI measure (reference method)
- Radiometric dating and age modeling
  - Pb210_Total, Pb210_Total_err: total 210Pb activity and error
  - Pb210_Supported, Pb210_Supported_err: supported 210Pb activity and error
  - Pb210_Unsupported, Pb210_Unsupported_err: unsupported 210Pb activity and error
  - Cum_Unsupported_Pb210, Cum_Unsupported_Pb210_er r: cumulative unsupported 210Pb and its error
  - Cs137, Cs137_err: 137Cs activity and error
  - Am241, Am241_err: 241Am activity and error
  - Date_AD: calculated year date (AD)
  - Age_yr, Age_yr_err: sediment age (yr) via Constant Rate of Supply model and its error
  - SAR: sediment dry mass accumulation rate (g cm^-2 yr^-1)
  - SR, SR_err: sedimentation rate (cm yr^-1) and its error
- Contaminants and elements
  - Hg (µg/g): total mercury by cold-vapour technique
  - Elements via XRF (concentrations)
    - Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%
    - V µg/g, Cr µg/g, Mn%, Fe%, Co µg/g, Ni µg/g, Cu µg/g, Zn µg/g, Ga µg/g
    - As µg/g, Br µg/g, Rb µg/g, Sr µg/g, Y µg/g, Nb µg/g, Ba µg/g, Pb µg/g
- Notes on units and interpretation
  - Some values appear as % dry mass; others as µg/g or g/cm^3 as indicated
  - Data gaps indicate no measurement for that determinand at that depth interval

## References and methods
- LOI methodology reference: Heiri, Lotter, & Lemcke (2001) for organic and carbonate content estimation.
- Dating methodology reference: Appleby & Oldfield (1978) for 210Pb dating with a constant rate of supply model.

## Practical implications for GIS and mapping
- Enables depth- and time-resolved mapping of sediment properties across multiple cores (WBIDs) and projects.
- Facilitates cross-core comparisons of LOI, radiometric ages, accumulation rates, and elemental compositions.
- Supports integration with spatial layers (core locations) to visualize spatial patterns of sediment characteristics.

## Data quality and challenges
- Data may be incomplete (blanks) or vary in resolution across cores.
- Data exist in multiple files and locations; standardization and provenance tracking are important.
- Cleaning and transforming data (unit harmonization, handling missing values) may be required before GIS integration.