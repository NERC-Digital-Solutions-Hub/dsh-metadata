# Headings used to record stratigraphic data collected for each core

- Purpose: Describes the data headings (determinands) used to record stratigraphic data for lake sediment cores, with blanks indicating no measurement. The data make up a matrix of determinands (columns) across contiguous core-depth intervals (rows).

## Data structure and file naming

- Files: Associated CSVs named with WBID (water body identification) and project code, e.g., 28965_DERW_DEEP.csv, 29166_EASE_LITT.csv, etc.
- Structure: Each row represents a core-depth interval; each column is a determinand (measurements or metadata) for that interval.
- Key identifiers:
  - Sub_ID: internal Amphora database unique ID for the core slice.
  - Top_Depth_cm / Bottom_Depth_cm: depth range within the core from the sediment–water interface.
- Recording and accessibility: Data are intended to be tracked, made discoverable, and uploaded with metadata to portals; datasets may be part of an internal database (Amphora).

## Determinands and measurements recorded

- Sediment mass and composition
  - DW: Mass of sediment after drying at 105°C for 24 h (percentage of wet weight).
  - LOI_550: Mass loss after combustion at 550°C for 2 h (organic content), per Heiri et al. 2001.
  - LOI_950: Carbonate content after combustion at 950°C for 2 h (per Heiri et al. 2001).
  - wetd: Mass of 1 cm³ of wet sediment (g), measured three times; mean used and divided by 2 to yield g cm⁻³.
- XRF (X-ray fluorescence) measurements
  - Concentrations of major and trace elements (e.g., Na, Al, Si, P, S, Cl, K, Ca, Ti, V, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Br, Rb, Sr, Y, Nb, Ba, Pb, etc.) expressed as %dry mass or µg/g as specified.
  - Notes: Samples are freeze-dried, milled, weighed (~2 g), and measured in a helium atmosphere with reference standards; daily re-calibration and QC references described.
- Radiometric dating and related measurements
  - Pb210_Total / Pb210_Total_err: Total 210Pb activity and its measurement error (Bq/kg).
  - Pb210_Supported / Pb210_Supported_err: Supported 210Pb activity and error.
  - Pb210_Unsupported / Pb210_Unsupported_err: Unsupported 210Pb activity and error.
  - Cum_Unsupported_Pb210 / Cum_Unsupported_Pb210_err: Cumulative unsupported 210Pb and its error.
  - Cs137 / Cs137_err: 137Cs activity and error (Bq/kg).
  - Am241 / Am241_err: 241Am activity and error (Bq/kg).
  - Date_AD: Calculated year date (AD).
  - Age_yr / Age_yr_err: Sediment age (years) using a Constant Rate of Supply (CRS) model and its error.
  - SAR: Sediment dry mass accumulation rate (g cm⁻² yr⁻¹).
  - SR / SR_err: Sedimentation rate (cm yr⁻¹) and its error.
- Additional notes: The presence of blanks indicates unavailable measurements for a given interval.

## Measurements and analytical methods

- Loss on ignition and density
  - LOI measurements follow Heiri et al. 2001 to estimate organic and carbonate content.
  - Wet density (wetd) is derived from triplicate wet sediment masses in a 2 cm³ vessel, averaged, and converted to g cm⁻³.
- XRF spectroscopy
  - Freeze-dried sediments milled and packed into vessels; measured by energy-dispersive XRF (EDXRF) in helium.
  - Calibration: Daily re-calibration with a fused bead reference; comparison with published reference sediment values.
  - QC documentation: Supported by a dedicated QC document (supporting_documentation_for_hydroscape_lakedistrict_core_xrf_qc.docx).
- Radiometric dating and radionuclides
  - 210Pb dating (half-life ~22.3 years) determined via gamma emissions; 226Ra via its daughter 214Pb gamma lines after equilibration.
  - 137Cs and 241Am measured by their gamma emissions (662 keV and 59.5 keV, respectively).
  - Corrections for self-absorption of low-energy gammas applied.
  - Chronologies calculated using the CRS dating model (Appleby & Oldfield 1978; Appleby 2001).

## Chronology and interpretation

- 210Pb dating framework: Uses unsupported 210Pb to establish recent sediment chronology; CRS model applied to derive ages and age uncertainties.
- Age interpretations: Age_yr and Age_yr_err accompany depth intervals to facilitate chronological reconstruction of sediment deposition.

## Data provenance, quality, and references

- Provenance: Data described as part of lake sediment core analyses; datasets are stored and annotated with metadata, and links to supporting QC and methodological documentation are provided.
- Quality control and references:
  - Heiri, Lotter, & Lemcke (2001): LOI methodology.
  - Appleby et al. (1986), Appleby & Oldfield (1978, 1992, 2001): 210Pb dating principles, CRS model, gamma counting corrections.
  - Appleby (2001): Chronostratigraphic techniques in recent sediments.
- Supporting materials: A QC document for XRF data accompanies the dataset (supporting_documentation_for_hydroscape_lakedistrict_core_xrf_qc.docx).