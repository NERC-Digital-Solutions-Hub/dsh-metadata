# This document describes the headings used to record the stratigraphic data collected for each core

- Purpose and scope
  - Describes how stratigraphic data for lake sediment cores are recorded.
  - Each core slice is captured as a row in a matrix of contiguous depth intervals; blanks indicate no measurement.
  - File names encode water body identification (WBID) and project code for each lake/core location.

- Data structure and content
  - Core identifiers and depth
    - Sub_ID: internal unique ID for a core slice.
    - Top_Depth_cm / Bottom_Depth_cm: depth range of the sliced core interval.
    - Description: additional notes about the interval.
  - Sediment properties and basic geochemistry
    - DW: dry weight mass percentage of wet weight after drying at 105°C for 24 hours.
    - LOI_550: organic matter content after combustion at 550°C for 2 hours.
    - LOI_950: carbonate content after combustion at 950°C for 2 hours.
    - wetd: wet density (g per cm^3) inferred from mass in a 2 cm^3 vessel.
  - Radiometric dating and age models
    - Pb210_Total / Pb210_Total_err, Pb210_Supported / Pb210_Supported_err, Pb210_Unsupported / Pb210_Unsupported_err: activities and uncertainties for total, supported, and unsupported Pb-210.
    - Cum_Unsupported_Pb210 / Cum_Unsupported_Pb210_err: cumulative unsupported Pb-210 and its error.
    - Cs137 / Cs137_err: Cs-137 activity and error.
    - Am241 / Am241_err: Am-241 activity and error.
    - Date_AD: calculated year date.
    - Age_yr / Age_yr_err: sediment age (year) and error from the Constant Rate of Supply (CRS) model.
    - SAR: sediment dry mass accumulation rate.
    - SR / SR_err: sedimentation rate and its error.
  - XRF and elemental composition
    - Concentrations of various elements measured by XRF (expressed as % dry mass or µg/g, depending on element and measurement method).
    - Examples include Al, Si, Na, K, Ca, Ti, Fe, Mn, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb, etc.
    - Some entries are reported as % of dry mass; others as µg/g.
  - Method-specific notes
    - Wet density measurements are obtained from three measurements per sample; mean used.
    - XRF methods: freeze-dried sediments milled, ~2 g aliquots placed in XRF vessels, measured in helium with calibration against reference sediments; daily re-calibration and QC against reference standards.
    - Supporting documentation for XRF QA/QC is provided (supporting_documentation_for_hydroscape_lakedistrict_core_xrf_qc.docx).

- Methodologies and references
  - Loss on ignition and organic/carbonate content
    - LOI procedures follow Heiri et al. (2001) for reproducibility and comparability.
  - XRF spectroscopy
    - EdXRF analysis (Bruker) in helium; reference sediments and factory standards used for calibration; cross-checks against published reference values.
    - QC documentation referenced for calibration/verification.
  - Radiometric dating and chronology
    - Pb-210 dating via gamma counting (half-life ~22.3 years); 226Ra via 214Pb descendants; storage to allow secular equilibrium.
    - 137Cs and 241Am measured by gamma emissions (662 keV and 59.5 keV) for dating support.
    - CRS (Constant Rate of Supply) model used for Pb-210 chronologies (Appleby & Oldfield 1978; Appleby 2001).

- Data provenance and governance
  - Data are collected and recorded with explicit core and depth intervals, ensuring traceability to unique core IDs.
  - Use of standardized methods and calibration against reference standards supports comparability across cores and projects.
  - Public sharing of underlying data is acknowledged as a potential barrier in broader monitoring contexts; emphasis on data quality, cleaning, and clear presentation (reports, charts, dashboards) aligns with monitoring framework aims.

- Supporting references
  - Heiri, O., Lotter, A. F., & Lemcke, G. (2001). LOI method in sediments.
  - Appleby, P. G. (2001); Appleby, P. G. et al. (1986, 1992); Appleby & Oldfield (1978) for CRS dating.
  - Appleby et al. various works on Pb-210 dating techniques and corrections.

- Associated files and data context
  - Multiple CSV files corresponding to different WBIDs and project codes (e.g., 28965_DERW_DEEP.csv, 29166_EASE_INT.csv, etc.).
  - The dataset includes a descriptive “text” layer elaborating measurement procedures, QA/QC, and methodology for the Hydroscape Lake District cores.