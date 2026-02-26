# Headings used to record the stratigraphic data collected for each core

- Overview
  - Document describes the headings used to record stratigraphic data for each lake core.
  - File naming uses water body identification numbers (WBID) and project code names; associated files include multiple cores across lakes (DEEP, LITT, INT).
  - Data are organized as a matrix of columns (determinands) and rows representing contiguous core-depth intervals; blanks indicate no measurement.
  - Internal ID (Sub_ID) uniquely identifies each core slice; Top_Depth_cm and Bottom_Depth_cm define the sliced interval depth from the sediment–water interface.

- Data structure and core identifiers
  - Core-level identifiers:
    - Sub_ID: Amphora internal unique ID for core slice.
    - Top_Depth_cm, Bottom_Depth_cm: interval boundaries in centimeters from the sediment/water interface.
  - Depth-interval data model: rows correspond to depth intervals; columns represent determinands (measurements and metadata).

- Determinands and measurements
  - Physical/chemical mass and content indicators:
    - DW (dry weight percentage), LOI_550 (loss on ignition at 550°C for 2 h), LOI_950 (loss on ignition at 950°C for 2 h)
    - wetd (wet density; g per cm3)
  - Radiometric dating and activity measurements:
    - Pb210_Total, Pb210_Total_err, Pb210_Supported, Pb210_Supported_err, Pb210_Unsupported, Pb210_Unsupported_err
    - Cum_Unsupported_Pb210, Cum_Unsupported_Pb210_err
    - Cs137, Cs137_err, Am241, Am241_err
    - Date_AD (calculated year date, AD)
    - Age_yr, Age_yr_err (age of sediment, Constant Rate of Supply model)
    - SAR (sediment accumulation rate, g cm-2 yr-1), SR (sedimentation rate, cm-2 yr-1), SR_err
  - XRF elemental and compositional data:
    - Hg_µg_g (total mercury by fluorescence spectroscopy)
    - Na_per, Al_per, Si_per, P_per, S_per, Cl_per, K_per, Ca_per, Ti_per, V_µg_g, Mn_per, Fe_per
    - Co_µg_g, Ni_µg_g, Cu_µg_g, Zn_µg_g, Ga_µg_g, As_µg_g, Br_µg_g, Rb_µg_g, Sr_µg_g, Y_µg_g, Nb_µg_g, Ba_µg_g, Pb_µg_g
    - All XRF concentrations expressed as % dry mass or µg/g as indicated in the determinant labels
  - Notes on data types and units:
    - LOI, DW, and mass-related metrics reflect mass-loss measurements following standard Heiri et al. (2001) procedures.
    - XRF data collected via energy-dispersive XRF (EDXRF) in a helium atmosphere; measurements calibrated with reference sediments; daily re-calibration and cross-checks described.
    - 210Pb dating relies on gamma assay with specific energy lines and correction for self-absorption; 210Pb chronology modeled with CRS (Appleby & Oldfield, 1978; Appleby, 2001).

- Preparation, measurement methods, and quality control
  - Sample preparation:
    - Freeze-dried sediments milled to ~2 g portions (for XRF measurement) and loaded into vessels.
  - Measurement and calibration:
    - EDXRF measurements performed in helium; daily calibration using multi-element fused bead reference standards.
    - Reference sediments used for cross-checking element concentrations; QC documentation referenced (supporting_documentation_for_hydroscape_lakedistrict_core_xrf_qc.docx).
  - Dating and analytical procedures:
    - 210Pb, 226Ra, 137Cs, and 241Am measured via direct gamma assay using low-background HPGe detector at UCL.
    - 210Pb determined from 46.5 keV gamma emissions; corrections for self-absorption applied; CRS model used for age dating.
  - Data quality notes:
    - Data gaps indicate measurements not performed on certain intervals.
    - Uncertainties provided for key radionuclide measurements (e.g., Pb210_Total_err, Cs137_err, Am241_err).
    - Method references included for reproducibility and traceability.

- Dating and chronology details
  - 210Pb dating:
    - Based on unsupported (atmospheric) 210Pb activity; CRS dating model applied.
    - Gamma energies and measurement approach described; equilibrium considerations after storage in sealed containers.
  - Additional radionuclide tracers:
    - 226Ra, 137Cs, and 241Am used to support recent sediment chronology and dating accuracy.
  - Chronology reporting:
    - Age_yr and Age_yr_err provide year-based age estimates with associated uncertainty.
    - SAR and SR values provide sediment accumulation and sedimentation rates with error margins.

- Data management and governance considerations for Data Stewards
  - Metadata and provenance:
    - Clear core-level identifiers (Sub_ID, Top/Bottom_Depth_cm) and sequence of depth intervals.
    - Detailed measurement methods and references embedded (Heiri et al. 2001; Appleby et al.; CRS dating references) to support reproducibility.
    - Documents and QC files referenced for XRF calibration and measurement QC.
  - Data integrity and interoperability:
    - Multiple associated files per lake core (DEEP, LITT, INT) requiring consistent data schemas across files.
    - Use of standardized units (e.g., cm for depths, g cm-3 for density, % dry mass for concentrations, Bq/kg for radioisotopes) to enable cross-dataset comparisons.
  - Data governance actions:
    - Maintain mapping between WBID/project codes and corresponding core files.
    - Track blanks and missing values to avoid misinterpretation of incomplete data.
    - Preserve links to methodological references and QC documentation to ensure methodological transparency.
    - Establish update and versioning practices for dataset improvements and correction of any measurement discrepancies.
  - Accessibility and sharing:
    - Ensure core datasets (with explicit determinands and units) are discoverable via catalogue portals; maintain clear documentation for end users about measurement context, detection limits, and uncertainties.
    - Include provenance notes and references to the supporting documentation for XRF QC and dating methods to support reuse.

- References
  - Heiri, O., Lotter, A. F., & Lemcke, G. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments.
  - Appleby, P. G. (2001); Appleby, P. G. et al. (1986); Appleby, P. G. & Oldfield, F. (1978). Chronostratigraphic techniques in recent sediments; 210Pb dating methods; CRS dating model.
  - Appleby, P. G., Nolan, P. J., Gifford, D. W., et al. (1986). 210Pb dating by low background gamma counting.

- Supporting documents
  - supporting_documentation_for_hydroscape_lakedistrict_core_xrf_qc.docx (XRF QC procedures and calibration references)