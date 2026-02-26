# Headers used to record the stratigraphic data collected for each core

## Overview
- Describes the headings (determinands) used to record stratigraphic data for each core.
- The data matrix uses columns as determinands and rows as contiguous core-depth intervals.
- Blanks indicate no measurement for a given interval.
- Associated files contain core-specific data (WBID and project codes).

## Core identifiers and depth information
- Sub_ID: Internal database unique ID for each core slice.
- Top_Depth_cm: Depth to the top of the sliced core section from the sediment/water interface.
- Bottom_Depth_cm: Depth to the bottom of the sliced core section from the sediment/water interface.

## Sediment properties and mass
- Mass of sediment following drying at 105°C for 24 hours (DW): percentage of wet-to-dry weight.
- LOI 550: carbonate content (%) by combustion at 550°C for 2 hours.
- LOI 950: carbonate-related measurement (description references LOI method; units as provided).
- wetd: mass (g) of 1 cm³ of wet sediment.

## Radioisotopes and dating
- Pb210_Total: activity (Bq/kg).
- Pb210_Total_err: measurement error for Pb-210 total activity.
- Pb210_Supported: activity of supported Pb-210 (Bq/kg).
- Pb210_Supported_err: error for supported Pb-210.
- Pb210_Unsupported: activity of unsupported Pb-210 (Bq/kg).
- Pb210_Unsupported_err: error for unsupported Pb-210.
- Cum_Unsupported_Pb210: cumulative unsupported Pb-210 (Bq/kg).
- Cum_Unsupported_Pb210_err: error in cumulative unsupported Pb-210.
- Cs137: activity of 137Cs (Bq/kg).
- Cs137_err: activity detection error for 137Cs.
- Am241: activity of 241Am (Bq/kg).
- Am241_err: activity detection error for 241Am.
- Date_AD: calculated year date (AD).
- Age_yr: age of sediment (years) using the Constant Rate of Supply (CRS) model.
- Age_yr_err: error in sediment age (years) from CRS model.

## Sediment accumulation and deposition
- SAR: Sediment dry mass accumulation rate (g cm⁻² yr⁻¹).
- SR: Sedimentation rate (cm⁻² yr⁻¹).
- SR_err: error on calculated sedimentation rate (cm⁻² yr⁻¹).

## Mercury measurement
- Hg µg/g: total mercury concentration measured by cold vapour atomic fluorescence spectroscopy; expressed as µg/g dry sediment.

## XRF elemental composition (percentage or µg/g as indicated)
- Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%: element concentrations expressed as % dry mass.
- V µg/g, Cr µg/g, Co µg/g, Ni µg/g, Cu µg/g, Zn µg/g, Ga µg/g, As µg/g, Br µg/g, Rb µg/g, Sr µg/g, Y µg/g, Nb µg/g, Ba µg/g, Pb µg/g: element concentrations expressed as µg/g (dry sediment) or as specified.

## Data provenance and references
- References:
  - Ref 1: Heiri, O., Lotter, A. F., & Lemcke, G. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments.
  - Ref 2: Appleby, P. G., & Oldfield, F. (1978). Calculation of Pb-210 dates assuming a constant rate of supply of unsupported Pb-210.

## Associated files
- 25855_doug_deep.csv
- 25866_bard_deep.csv
- 25866_bard_litt.csv
- 26001_possi_lit.csv
- 26145_hogg_deep.csv
- 26163_bish_deep.csv
- 26167_wode_deep.csv
- 26392_semp_deep.csv
- 26392_semp_int.csv
- 26392_semp_litt.csv
- 26535_libo_deep.csv

## Practical notes for data use (Data Support perspective)
- Use this dictionary to map core-depth intervals to measurements consistently across cores.
- Pay attention to units (e.g., % dry mass, µg/g, Bq/kg, g cm⁻² yr⁻¹) and depth references (Top_Depth_cm, Bottom_Depth_cm).
- Treat blanks as missing data; plan joins across cores carefully to avoid misinterpreting gaps.
- When combining datasets, align depth intervals and ensure consistent dating methods (CRS model for Age_yr, CRS-related assumptions).
- Reference LOI and Pb-210 methods when comparing results across cores or projects.
- Create self-serve data products (dashboards, pivot tables) that allow filtering by core, depth, determinand type (e.g., radionuclides, XRF elements), and derived metrics (e.g., Age_yr, SAR).