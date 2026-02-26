# This document describes the headings used to record the stratigraphic data collected for each core.

## Overview
- Defines the headings (determinands) used to record stratigraphic data for lake sediment cores.
- Data are organized as a matrix: columns are measurements (determinands) and rows are contiguous core-depth intervals.
- Blanks indicate missing measurements.
- Core data are associated with WBID-based files and project codes, enabling GIS-based mapping and cross-lake analyses.

## Data structure and file naming
- Associated files: multiple CSV files (e.g., 28965_DERW_DEEP.csv, 28965_DERW_LITT.csv, 28965_DERW_INT.csv, 29166_EASE_DEEP.csv, etc.) covering different lakes and core sections (DEEP, LITT, INT).
- File naming convention: WBID (water body identification number) + project code name of lake/core location.
- Each file contains measurements for a given core and depth intervals; rows correspond to depth slices with top and bottom depths, and columns to determinations (determinands).

## Core data fields (Determinants)
- Core metadata and depth
  - Sub_ID (internal unique core-slice ID)
  - Top_Depth_cm, Bottom_Depth_cm (depth interval from sediment–water interface)
- Sediment mass and composition
  - DW (percentage dry weight)
  - LOI_550 (loss on ignition at 550°C)
  - LOI_950 (loss on ignition at 950°C)
  - wetd (mass of 1 cm³ of wet sediment)
- Chronology and dating
  - Date_AD (calculated year date)
  - Age_yr (age of sediment by Constant Rate of Supply model)
  - Age_yr_err (error in age)
  - Pb210_Total, Pb210_Total_err
  - Pb210_Supported, Pb210_Supported_err
  - Pb210_Unsupported, Pb210_Unsupported_err
  - Cum_Unsupported_Pb210, Cum_Unsupported_Pb210_err
  - Cs137, Cs137_err
  - Am241, Am241_err
  - SAR (sediment dry mass accumulation rate)
  - SR (sedimentation rate)
  - SR_err
- Geochemistry and elemental concentrations (XRF)
  - Hg_µg_g
  - Na_per, Al_per, Si_per, P_per, S_per, Cl_per, K_per, Ca_per, Ti_per
  - V_µg_g, Mn_per, Fe_per, Co_µg_g, Ni_µg_g, Cu_µg_g, Zn_µg_g
  - Ga_µg_g, As_µg_g, Br_µg_g, Rb_µg_g, Sr_µg_g, Y_µg_g, Nb_µg_g, Ba_µg_g, Pb_µg_g
  - Notes: concentrations expressed as % dry mass (for some elements) or µg/g (others) as measured by XRF.
  
## Measurements and methods
- Loss on ignition and density
  - LOI and DW procedures follow Heiri et al. (2001) to estimate organic and carbonate content.
  - Wet density (wetd) measured in 2 cm³ vessels; three replicates per sample, mean used and converted to g cm⁻³.
- XRF spectroscopy
  - Samples are freeze-dried, milled, and measured by energy-dispersive XRF in helium.
  - ~2 g aliquots loaded into vessels; calibration and QC via reference sediments; daily re-calibration.
  - QC documented in supporting_file: supporting_documentation_for_hydroscape_lakedistrict_core_xrf_qc.docx.
- 210Pb dating and 137Cs measurements
  - 210Pb dating using gamma assay; 46.5 keV for 210Pb; 226Ra via 214Pb daughters after equilibration.
  - 137Cs and 241Am measured at their principal gamma energies (662 keV and 59.5 keV) with corrections for self-absorption.
  - CRS (constant rate of supply) model used for 210Pb chronology (Appleby & Oldfield; Appleby 2001).

## GIS and data use
- Enables creation of map-based data products: plotting core locations, age-depth relationships, and sedimentation rates across lakes.
- Depth intervals can be translated to ages (Date_AD/Age_yr) for chronological mapping and cross-lake comparisons.
- Multi-element geochemical data supports spatial analyses of lake catchment changes and environmental proxies.

## Data quality, standards, and documentation
- Data blanks indicate missing measurements; highlights need for data cleaning and standardization across datasets.
- QC considerations include daily XRF calibration, reference sediment checks, and documented protocols.
- References for methods and dating:
  - Heiri, Lotter, Lemcke (2001)
  - Appleby et al. (1986); Appleby (2001); Appleby & Oldfield (1978)

## Associated files
- Examples of core data files:
  - 28965_DERW_DEEP.csv, 28965_DERW_LITT.csv, 28965_DERW_INT.csv
  - 29166_EASE_DEEP.csv, 29166_EASE_LITT.csv, 29166_EASE_INT.csv
  - 29184_GRAS_DEEP.csv, 29184_GRAS_LITT.csv, 29184_GRAS_INT.csv
  - 29197_RYDA_DEEP.csv, 29197_RYDA_LITT.csv, 29197_RYDA_INT.csv
  - 29215_BURNMT_DEEP.csv, 29215_BURNMT_LITT.csv, 29215_BURNMT_INT.csv
  - 29321_CONI_DEEP.csv, 29321_CONI_LITT.csv, 29321_CONI_INT.csv
  - 29328_ESTH_DEEP.csv, 29328_ESTH_LITT.csv, 29328_ESTH10_INT.csv
  - 47008_WIND_DEEP.csv, 47008_WIND_LITT.csv, 47008_WIND_INT.csv

## Notes for GIS specialists
- The dataset is designed to support spatial analyses of lake sediments by core location and depth horizon, enabling age-structured layering and multi-element geochemical mapping.
- Ensure consistent handling of depth-to-age conversions and harmonize units across files for seamless GIS integration.
- Be aware of potential data gaps and provenance from multiple files; cross-reference Sub_ID and WBID when integrating datasets.