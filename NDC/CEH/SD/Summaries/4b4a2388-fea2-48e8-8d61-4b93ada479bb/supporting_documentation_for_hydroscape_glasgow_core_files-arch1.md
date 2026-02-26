# Headings used to record the stratigraphic data collected for each core

- Purpose and scope
  - Describes the headings used to record stratigraphic data collected for each sediment core.
  - Data are organized as a matrix of contiguous core-depth intervals; blanks indicate no measurement.

- Data structure
  - Internal ID: Sub_ID (UCL Amphora database) uniquely identifies each core slice.
  - Depths: Top_Depth_cm and Bottom_Depth_cm denote slice boundaries from the sediment–water interface.
  - Core metadata: File names encode water body identification number (WBID) and project code; associated files include multiple CSVs per lake/core location.

- Core-level and depth-level measurements
  - Mass and density
    - DW: mass of sediment as a percentage of wet weight after drying at 105°C for 24 hours.
    - wetd: mass (g) of 1 cm³ of wet sediment.
    - "Description" notes imply dry mass measurements (inferred as part of dry weight calculations).

  - Loss on ignition
    - LOI 550: carbonate content (%) via combustion at 550°C for 2 hours.
    - LOI 950: additional LOI measurement (method reference 1).

  - Chronology and accumulation
    - Date_AD: calculated year date (AD).
    - Age_yr: age of sediment using the Constant Rate of Supply (CRS) model.
    - Age_yr_err: error in CRS age.
    - SAR: sediment dry mass accumulation rate (g cm⁻² yr⁻¹).
    - SR: sedimentation rate (cm yr⁻¹); SR_err: error on SR.

  - Radioisotopes and activity
    - Pb210_Total and Pb210_Total_err: total 210Pb activity and detection error (Bq/kg).
    - Pb210_Supported and Pb210_Supported_err: supported 210Pb activity and error (Bq/kg).
    - Pb210_Unsupported and Pb210_Unsupported_err: unsupported 210Pb activity and error (Bq/kg).
    - Cum_Unsupported_Pb210 and Cum_Unsupported_Pb210_err: cumulative unsupported 210Pb and its error (Bq/kg).

  - Radiometric dating
    - Cs137 and Cs137_err: 137Cs activity (Bq/kg) and error.
    - Am241 and Am241_err: 241Am activity (Bq/kg) and error.

  - Mercury and trace elements
    - Hg µg/g: total mercury by cold vapour atomic fluorescence.
    - XRF elemental concentrations: Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%, V µg/g, Cr µg/g, Mn%, Fe%, Co µg/g, Ni µg/g, Cu µg/g, Zn µg/g, Ga µg/g, As µg/g, Br µg/g, Rb µg/g, Sr µg/g, Y µg/g, Nb µg/g, Ba µg/g, Pb µg/g.

- Data interpretation and quality
  - Data are intended to support corrosion/accumulation history, dating via 210Pb and CRS, and multi-proxy geochemical interpretation.
  - Data provenance is tracked; datasets may be uploaded with metadata to make them discoverable.

- Data limitations and challenges (context for analysts)
  - Potential gaps due to blanks indicating missing measurements.
  - Variability in data availability across cores and lakes; data may be dispersed across multiple files with local naming conventions.
  - Methods for LOI and CRS dating are based on cited references (LoI methods by Heiri et al. 2001; CRS dating by Appleby & Oldfield 1978).