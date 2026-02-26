# This document describes the headings used to record the stratigraphic data collected for each core.

## Overview
- Describes the headings (columns/determinands) used to record stratigraphic data for each core.
- Data blanks indicate no measurement.
- The data matrix comprises columns (determinands) and rows representing contiguous core-depth intervals.

## Data structure and content
- The dataset is organized as a matrix with:
  - Rows: Contiguous depth intervals within each core.
  - Columns: Determinands (measurement types).

## Core and depth definitions
- Sub_ID: Internal UCL Amphora database unique ID for each core slice.
- Top_Depth_cm: Distance to the top of the sliced core section from the sediment/water interface.
- Bottom_Depth_cm: Distance to the bottom of the sliced core section from the sediment/water interface.
- DW: Mass of sediment after drying at 105°C for 24 hours (as percentage of wet weight).
- Wetd: Mass (g) of 1 cm³ of wet sediment.
- Data blanks: Indicate missing measurements.

## Dating, age and sedimentation indicators
- Pb210_Total: Activity of total 210Pb (Bq/kg).
- Pb210_Total_err: Detection error for total 210Pb.
- Pb210_Supported: Activity of supported 210Pb (Bq/kg).
- Pb210_Supported_err: Detection error for supported 210Pb.
- Pb210_Unsupported: Activity of unsupported 210Pb (Bq/kg).
- Pb210_Unsupported_err: Detection error for unsupported 210Pb.
- Cum_Unsupported_Pb210: Cumulative unsupported 210Pb (Bq/kg).
- Cum_Unsupported_Pb210_err: Error on cumulative unsupported 210Pb.
- Cs137: Activity of 137Cs (Bq/kg).
- Cs137_err: Detection error for 137Cs.
- Am241: Activity of unsupported 241Am (Bq/kg).
- Am241_err: Detection error for 241Am.
- Date_AD: Calculated year date (AD).
- Age_yr: Age of sediment (years) using Constant Rate of Supply model.
- Age_yr_err SAR: Error in age (years) using SAR model.
- SR: Sedimentation rate (cm⁻² yr⁻¹).
- SR_err: Error on sedimentation rate.

## Geochemistry and elemental measurements
- Hg_µg/g: Concentration of total mercury (µg/g) by Cold Vapour Atomic method.
- Elements measured by XRF (percent dry mass or µg/g where indicated):
  - Na_%, Mg_%, Al_%, Si_%, P_%, S_% (and Cl_% as separate items)
  - K_%, Ca_%, Ti_%
  - V_µg/g, Cr_µg/g, Mn_%, Fe_%, Co_µg/g
  - Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g
  - As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g
  - Nb_µg/g, Ba_µg/g, Pb_µg/g

## Data quality, provenance and usage
- The headings provide a standardized schema to facilitate data integration, quality assurance, and sharing across datasets.
- The structure supports uploading to portals and cataloguing data holdings, with potential documentation of work performed on datasets.

## Associated files
- 34827_FELB6.csv
- 35179_WOLT1.csv
- 35249_BLIC2.csv
- 35738_MARS1.csv
- 35852_BURF1.csv
- 35977_HGB01.csv
- 36043_SALG1.csv
- 36202_UPTO3.csv
- Note: File names use water body identification number (WBID) and project code name of lake and core.

## References
- Ref 1. Heiri, O., Lotter, A. F., & Lemcke, G. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments: reproducibility and comparability of results.
- Ref 2. Appleby, P. G., & Oldfield, F. (1978). The calculation of lead-210 dates assuming a constant rate of supply of unsupported 210Pb to the sediment.