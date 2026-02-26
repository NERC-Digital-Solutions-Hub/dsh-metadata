# Headings used to record the stratigraphic data collected for each core

- Purpose and scope
  - Describes the headings used to record stratigraphic data for each lake/core core.
  - Data are stored in a matrix with columns (determinands) and rows representing contiguous core-depth intervals.
  - Blanks indicate no measurement; associated files are CSVs named with water body IDs (WBID) and project codes.

- Data structure and identifiers
  - Internal ID: Sub_ID for each core slice.
  - Depths: Top_Depth_cm and Bottom_Depth_cm define the sliced interval (distance from sediment/water interface).
  - Core slice reference: Description provides the mapping to the internal UCL Amphora database.

- Core properties and basic measurements
  - DW: Mass of sediment after drying at 105°C for 24 hours (as a percentage of wet weight).
  - LOI_550: Carbonate content (%), determined by specified combustion method.
  - LOI_950: Additional carbonate-related value (as described, relates to combustion protocols).
  - Wetd: Mass of 1 cm³ of wet sediment.

- Radiometric dating and related metrics
  - Pb210_Total and Pb210_Total_err: Total 210Pb activity and its measurement error (Bq/kg).
  - Pb210_Supported and Pb210_Supported_err: Supported 210Pb activity and error (Bq/kg).
  - Pb210_Unsupported and Pb210_Unsupported_err: Unsupported 210Pb activity and error (Bq/kg).
  - Cum_Unsupported_Pb210 and Cum_Unsupported_Pb210_err: Cumulative unsupported 210Pb and its error.
  - Cs137 and Cs137_err: 137Cs activity and its error (Bq/kg).
  - Am241 and Am241_err: 241Am activity and its error (Bq/kg).
  - Date_AD: Calculated year date (AD).

- Age modelling and sedimentation rates
  - Age_yr and Age_yr_err SAR: Age of sediment (years) using Constant Rate of Supply model; corresponding error.
  - SR and SR_err: Sedimentation rate (cm⁻² yr⁻¹) and its error.

- Mercury and elemental/geochemical data
  - Hg_µg/g: Total mercury concentration in µg/g (dry sediment), measured by Cold Vapour Atomic Fluorescence.
  - XRF elemental concentrations: Na_%, Mg_%, Al_%, Si_%, P_%, S_% (and Cl_%, with a formatting note indicating a headers issue).
  - Additional elements (µg/g): V_µg/g, Cr_µg/g, Co_µg/g, Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g, As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g, Nb_µg/g, Ba_µg/g, Pb_µg/g.
  - Mn_%, Fe_%, Ti_%, Ca_%, K_% and others listed as % of dry mass.

- Data quality, interpretation and outputs
  - Data blanks indicate measurements not taken for a given interval.
  - Outputs are designed to enable end users to self-serve (dashboards, pivot tables, reports) with guidance on tool use.
  - Potential for sharing early prototypes, gathering feedback, and promoting outputs to encourage wider use and re-use of results.

- Files and provenance
  - Associated files: 34827_FELB6.csv, 35179_WOLT1.csv, 35249_BLIC2.csv, 35738_MARS1.csv, 35852_BURF1.csv, 35977_HGB01.csv, 36043_SALG1.csv, 36202_UPTO3.csv, among others.
  - File naming convention reflects WBID and lake/project codes.

- References and methodological notes
  - Ref 1: Heiri, Lotter, & Lemcke (2001) on loss-on-ignition (LOI) as a method for estimating organic and carbonate content in sediments.
  - Ref 2: Appleby & Oldfield (1978) on calculating lead-210 dates assuming a constant rate of supply of unsupported 210Pb to sediment.

- Context for data use
  - The dataset supports broad data exploration, combination, and creation of data products to aid interpretation across topics (e.g., environmental history, pollution, sedimentation).