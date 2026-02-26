# Description of the Headings Used to Record Stratigraphic Data Collected for Each Core

- Associated files
  - 34827_FELB6.csv
  - 35179_WOLT1.csv
  - 35249_BLIC2.csv
  - 35738_MARS1.csv
  - 35852_BURF1.csv
  - 35977_HGB01.csv
  - 36043_SALG1.csv
  - 36202_UPTO3.csv
  - File names encode water body identification number (WBID) and lake/core project code.

- Purpose and structure
  - Describes the headings used to record stratigraphic data for each core.
  - Data are organized as a matrix with columns (determinands) and rows representing contiguous core-depth intervals.
  - Blanks indicate no measurement.

- Key fields (determinands)
  - Sub_ID: Internal Amphora database unique ID for a core slice.
  - Top_Depth_cm / Bottom_Depth_cm: Depth range of the sliced core section (cm from sediment/water interface).
  - DW: Dry-weight mass of sediment after drying at 105°C for 24 hours, as a percentage of wet weight.
  - LOI_550 / LOI_950: Mass loss on ignition at 550°C (dry-weight basis) and carbonate content (%), respectively (measured by combustion at specified temperatures).
  - Wetd: Wet density (g per cm³) of sediment.
  - Pb210_Total / Pb210_Total_err: Total 210Pb activity (Bq/kg) and its measurement error.
  - Pb210_Supported / Pb210_Supported_err: Supported 210Pb activity and error.
  - Pb210_Unsupported / Pb210_Unsupported_err: Unsupported 210Pb activity and error.
  - Cum_Unsupported_Pb210 / Cum_Unsupported_Pb210_err: Cumulative unsupported 210Pb and error.
  - Cs137 / Cs137_err: 137Cs activity and error.
  - Am241 / Am241_err: 241Am activity and error.
  - Date_AD: Calculated year date (AD).
  - Age_yr / Age_yr_err SAR: Sediment age (years) via Constant Rate of Supply model and its error.
  - SR / SR_err: Sedimentation rate (g cm⁻² yr⁻¹) and its error.
  - Hg_µg/g: Mercury concentration (µg/g, dry sediment).
  - XRF element concentrations: Na_%, Mg_%, Al_%, Si_%, P_%, S_%/Cl_% (note an apparent formatting gap), K_%, Ca_%, Ti_%, V_µg/g, Cr_µg/g, Mn_%, Fe_%, Co_µg/g, Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g, As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g, Nb_µg/g, Ba_µg/g, Pb_µg/g.
  - Note: one placeholder field appears as ", 1 = Concentration of element expressed as %dry mass of sediment" which may indicate a formatting issue in the original list.

- References (methodology)
  - Ref 1: Heiri, O., Lotter, A. F., & Lemcke, G. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments.
  - Ref 2: Appleby, P. G., & Oldfield, F. (1978). Calculation of lead-210 dates assuming a constant rate of supply of unsupported 210Pb.

- Data quality and scope
  - Data represent segmented core intervals with measurements across radiometric dating, loss-on-ignition, density, and multi-element geochemistry (XRF).
  - Data gaps indicate absent measurements for specific intervals or determinands.
  - Suitable for creating GIS-ready layers of age, accumulation rate, and geochemical distributions across lakes when linked to core locations.