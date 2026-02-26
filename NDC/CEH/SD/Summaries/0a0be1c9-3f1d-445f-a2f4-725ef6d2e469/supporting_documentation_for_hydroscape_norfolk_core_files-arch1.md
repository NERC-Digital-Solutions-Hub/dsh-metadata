# This document describes the headings used to record the stratigraphic data collected for each core

## Associated files
- 34827_FELB6.csv
- 35179_WOLT1.csv
- 35249_BLIC2.csv
- 35738_MARS1.csv
- 35852_BURF1.csv
- 35977_HGB01.csv
- 36043_SALG1.csv
- 36202_UPTO3.csv

## Purpose and scope
- Describes the column headers (determinands) used to record stratigraphic data for each core.
- The data are stored as a matrix with columns representing measurements and rows representing contiguous core-depth intervals.
- Data blanks indicate no measurement.
- Data are linked to an internal UCL Amphora database (Sub_ID).

## Core and depth information
- Sub_ID: Internal unique ID for a core slice.
- Top_Depth_cm: Distance from the sediment/water interface to the top of the sliced core section.
- Bottom_Depth_cm: Distance from the sediment/water interface to the bottom of the sliced core section.
- DW: Mass of sediment after drying at 105°C for 24 hours (reported as a percentage of wet weight).

## Loss on ignition and related measurements
- LOI_550: Loss on ignition at 550°C (percentage change; described as related to carbonate content in the text, though traditionally LOI_550 estimates organic content).
- LOI_950: Carbonate content (%), calculated by combustion at 950°C for 2 hours.
- Wetd: Mass of 1 cm³ of wet sediment.

## Radioisotope dating and related ages
- Pb210_Total: Activity of total 210Pb (Bq/kg).
- Pb210_Total_err: Detection error for Pb210_Total.
- Pb210_Supported: Activity of supported 210Pb (Bq/kg).
- Pb210_Supported_err: Detection error for Pb210_Supported.
- Pb210_Unsupported: Activity of unsupported 210Pb (Bq/kg).
- Pb210_Unsupported_err: Detection error for Pb210_Unsupported.
- Cum_Unsupported_Pb210: Cumulative unsupported 210Pb (Bq/kg).
- Cum_Unsupported_Pb210_err: Error on cumulative unsupported 210Pb.
- Cs137: Activity of 137Cs (Bq/kg).
- Cs137_err: Detection error for Cs137.
- Am241: Activity of 241Am (Bq/kg).
- Am241_err: Detection error for Am241.
- Date_AD: Calculated year date (AD).

## Age modelling and sedimentation rates
- Age_yr: Age of sediment (years) using the Constant Rate of Supply (CRS) model.
- Age_yr_err SAR: Error in age estimation using CRS.
- SR: Sedimentation rate (g cm⁻² yr⁻¹) – sediment dry mass accumulation rate.
- SR_err: Error on sedimentation rate.

## Mercury and XRF geochemistry
- Hg_µg/g: Mercury concentration measured by Cold Vapour Atomic Fluorescence Spectroscopy (µg/g) on dry sediment.
- Elements measured by XRF (listed individually): Na_%, Mg_%, Al_%, Si_%, P_%, S_% (Cl_% appears to be misformatted in the source), K_%, Ca_%, Ti_%, V_µg/g, Cr_µg/g, Mn_%, Fe_%, Co_µg/g, Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g, As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g, Nb_µg/g, Ba_µg/g, Pb_µg/g.

## References
- Ref 1. Heiri, O., Lotter, A. F., & Lemcke, G. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments: reproducibility and comparability of results.
- Ref 2. Appleby, P. G., & Oldfield, F. (1978). The calculation of lead-210 dates assuming a constant rate of supply of unsupported 210Pb to the sediment.