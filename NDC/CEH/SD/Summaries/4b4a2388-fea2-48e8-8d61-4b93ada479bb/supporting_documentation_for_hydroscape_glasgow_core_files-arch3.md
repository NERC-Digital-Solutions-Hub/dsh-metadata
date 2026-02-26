# Description of the Headings Used to Record the Stratigraphic Data Collected for Each Core

- Overview
  - Defines the headings (determinands) used to record stratigraphic data for each core in a matrix format.
  - Data files are named with a water body identification number (WBID) and project code; blanks indicate no measurement.
  - The matrix comprises columns (determinands) and rows representing contiguous core-depth intervals.

- Data structure and core metadata
  - Sub_ID: Internal Amphora database ID for the core slice.
  - Top_Depth_cm / Bottom_Depth_cm: Distance to the top/bottom of the sliced core section from the sediment/water interface.
  - The depth intervals are contiguous and define the sampled slices.

- Physical and compositional measurements
  - DW: Mass of sediment after drying at 105°C for 24 hours.
  - LOI 550: Percentage of dry weight lost after combustion at 550°C for 2 hours (organic content).
  - LOI 950: Carbonate content (%) calculated by combustion at 950°C for 2 hours.
  - wetd: Mass of 1 cm^3 of wet sediment.
  - XRF- and related element concentrations (e.g., Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%, V, Cr, Mn%, Fe%, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb).
  - Hg: Total mercury concentration measured by atomic fluorescence (µg/g, dry sediment).
  - All determinands include explicit units or percent dry mass where applicable.

- Radiometric dating and age-related measurements
  - Pb210_Total / Pb210_Total_err: Total 210Pb activity (Bq/kg) and its error.
  - Pb210_Supported / Pb210_Supported_err: Supported 210Pb activity and error.
  - Pb210_Unsupported / Pb210_Unsupported_err: Unsupported 210Pb activity and error.
  - Cum_Unsupported_Pb210 / Cum_Unsupported_Pb210_er r: Cumulative unsupported 210Pb and its error.
  - Cs137 / Cs137_err: 137Cs activity and error.
  - Am241 / Am241_err: 241Am activity and error.
  - Date_AD: Calculated year date (AD).
  - Age_yr / Age_yr_err: Age of sediment (years) using the Constant Rate of Supply (CRS) model and its error.

- Sedimentation metrics
  - SAR: Sediment dry mass accumulation rate (g cm^-2 yr^-1).
  - SR / SR_err: Sedimentation rate (cm yr^-1) and its error.

- Data governance and provenance
  - Data are organized in an internal UCL Amphora database; Sub_ID provides a unique reference for each core slice.
  - Blanks indicate missing measurements for specific intervals.
  - The dataset supports cross-sample comparisons across lakes and projects, with measurement methods and units standardized where described.

- References and methodologies
  - Ref 1: Heiri, Lotter, Lemcke (2001) on loss on ignition methods (LOI) for estimating organic and carbonate content.
  - Ref 2: Appleby & Oldfield (1978) on calculating lead-210 dates assuming a constant rate of supply of unsupported 210Pb (CRS model).