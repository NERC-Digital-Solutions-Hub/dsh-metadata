# This document describes the headings used to record the stratigraphic data collected for each core.

- Purpose and scope
  - Describes the headings used to record stratigraphic data for each lake sediment core.
  - Data are organized as a matrix with columns (determinands) and rows corresponding to contiguous core-depth intervals.
  - Data blanks indicate no measurement.
  - File names encode water body identification number (WBID) and project code; examples include 28965_DERW_DEEP.csv and others.
  - The document supports data discoverability, consistency, and future use across cores and lakes.

- Data structure and identifiers
  - Sub_ID: internal UCL Amphora database unique ID for each core slice.
  - Top_Depth_cm, Bottom_Depth_cm: depth range of the sliced core interval from the sediment–water interface.
  - The dataset comprises measurements across multiple cores and depth intervals (DEEP, LITT, INT groupings).

- Core composition and mass measurements
  - DW: percentage dry weight (mass of sediment after drying at 105°C for 24 hours) relative to wet weight.
  - LOI_550: loss on ignition after combustion at 550°C for 2 hours (organic matter estimation per Heiri et al. 2001).
  - LOI_950: loss on ignition after combustion at 950°C for 2 hours (carbonate content estimation per Heiri et al. 2001).
  - wetd: mean wet density measurement expressed as g per cm³ (mass of wet sediment per 1 cm³, derived from three measurements).

- XRF spectroscopy measurements
  - XRF data (percentage dry mass or concentration) for multiple elements, including Na, Al, Si, P, S, Cl, K, Ca, Ti, Fe, Mn, etc., with all elements reported in either %dry mass or µg/g as specified.
  - Specific entries include Fe_per, Al_per, Si_per, Na_per, K_per, Ca_per, Ti_per, P_per, S_per, Cl_per, Mn_per, and trace/other elements (Co_µg_g, Ni_µg_g, Cu_µg_g, Zn_µg_g, Ga_µg_g, As_µg_g, Br_µg_g, Rb_µg_g, Sr_µg_g, Y_µg_g, Nb_µg_g, Ba_µg_g, Pb_µg_g, and others).
  - XRF measurements were performed on freeze-dried, milled sediment samples in helium using EDXRF, with daily calibration and a reference sediment in each run.
  - A supporting QC documentation file is referenced for XRF quality control (supporting_documentation_for_hydroscape_lakedistrict_core_xrf_qc.docx).

- Radioisotope dating, actinides, and chronology
  - Pb210_Total, Pb210_Total_err: total 210Pb activity and its measurement error (Bq/kg).
  - Pb210_Supported, Pb210_Supported_err: supported 210Pb activity and error.
  - Pb210_Unsupported, Pb210_Unsupported_err: unsupported 210Pb activity and error.
  - Cum_Unsupported_Pb210, Cum_Unsupported_Pb210_err: cumulative unsupported 210Pb activity and error (Bq/kg).
  - Cs137, Cs137_err: 137Cs activity and error (Bq/kg).
  - Am241, Am241_err: 241Am activity and error (Bq/kg).
  - Date_AD: calculated year date (Anno Domini).
  - Age_yr, Age_yr_err: sediment age (year) estimated via the Constant Rate of Supply (CRS) model and its error.
  - SAR: sedimentation rate (g cm⁻² yr⁻¹).
  - SR, SR_err: sedimentation rate (cm⁻² yr⁻¹) and its error.

- Methodology and data generation notes
  - Loss on ignition and wet density measurements follow established protocols:
    - LOI and DW interpretations align with Heiri et al. (2001) for estimating organic and carbonate content.
    - Wet density is derived from three repeated measurements, converted to g cm⁻³.
  - XRF spectroscopy:
    - Samples prepared as ~2 g powders, measured in a helium atmosphere with calibration via reference sediments.
    - Daily re-calibration and QC procedures referenced to a dedicated QC document.
  - Lead-210 dating and 137Cs measurements:
    - Dried sediments analyzed by gamma assay at University College London using an ORTEC HPGe detector.
    - 210Pb dating conducted using the CRS model (Appleby and Oldfield 1978; Appleby 2001).
    - Cs-137 and 241Am used for recent dating markers; corrections include self-absorption adjustments.
  - References for methods include:
    - Heiri, Lotter, Lemcke (2001) for LOI methodology.
    - Appleby et al. (1986, 1992) and Appleby & Oldfield (1978, 2001) for 210Pb dating and calibration.
    - Additional methodological context in tracking environmental change using lake sediments.

- Documentation and data governance
  - The document links to a supporting documentation file for XRF quality control (QC) and references standard methodological sources.
  - Emphasizes structured, unit-consistent data recording to enable cross-core comparability and re-use.
  - Aligns with data leadership goals: providing a clear data schema, metadata, and measurement details to support data discovery, quality assessment, and iterative use by policy colleagues and data partners across networks.