# SoilCharacterstics.csv read me file

## Overview
- Describes the characteristics of the Orthic Podzol soil at Henfaes Research Station, North Wales.
- Collected during two seasonal field trials (spring and autumn) in 2016–2017 to monitor greenhouse gas emissions from sheep urine applied to semi-improved pasture.
- Location details: Henfaes Research Station, Abergwyngregyn, North Wales (53°13'N, 4°0'W), ~270 m above sea level, 13% slope.
- Experimental design includes 4 replicates from control plots within both spring and autumn plots.

## Data content and scope
- The dataset lists soil properties for both spring (SP) and autumn (AT) seasons.
- Depths and sample handling:
  - Bulk density (BD) at 0–5 cm depth (SP and AT), corrected for stone weight/volume.
  - Gravimetric soil moisture at 0–10 cm (Gravmoist SP and AT).
  - Organic matter (Orgmat SP and AT) as a percentage of dry soil weight.
  - pH (pH SP and AT) and electrical conductivity (EC SP and AT) at 0–10 cm.
  - Total carbon (C_SP, C_AT) and total nitrogen (N_SP, N_AT) contents at 0–10 cm (dry weight basis); includes carbon-to-nitrogen ratio (CN_SP, CN_AT).
  - Nitrogen mineralisation rate (Nmin_SP, Nmin_AT) at 0–10 cm (mg N kg-1 day-1).
  - Extractable pools (all SP vs AT) including:
    - DOC (0.5 M K2SO4 extractable dissolved organic carbon)
    - TDN (0.5 M K2SO4 extractable total dissolved nitrogen)
    - Nitrate (NO3--N)
    - Ammonium (NH4+-N)
    - Phosphate (PO43--P) via 1 M acetic acid extract
    - Na, K, Ca (1 M acetic acid extract)
- Analytical methods and instruments (summarised):
  - Bulk density: soil cores, oven-drying, stone correction.
  - Moisture: oven-drying at 105 °C.
  - Organic matter: loss-on-ignition (Ball 1964).
  - pH/EC: 1:2.5 soil-to-water suspensions with calibrated electrodes.
  - Total C/N: TruSpec® Analyzer (Leco).
  - N mineralisation: based on Waring and Bremner (1964) with NH4+ measured (Mulvaney 1996).
  - NH4+/NO3- and other extracts: standard colorimetric and extraction methods; CHCl3 fumigation for microbial biomass C/N (EC factors 0.35/0.5).
  - PO43- and cations: Murphy and Riley (1962) and flame photometry for cations.
- Quality and traceability:
  - All solutions analysed against matrix-matched certified references; procedural blanks used.
  - Data visually checked for quality assurance.

## Data structure and headers
- Key headers and meanings:
  - BD_SP, BD_AT: Bulk density (g cm-3) for spring/autumn 0–5 cm depth; corrected for stone weight/volume.
  - Gravmoist_SP, Gravmoist_AT: Gravimetric moisture content (%, 0–10 cm).
  - Orgmat_SP, Orgmat_AT: Organic matter (% of dry soil weight).
  - pH_SP, pH_AT: Soil pH (0–10 cm).
  - EC_SP, EC_AT: Electrical conductivity (µS cm-1, 0–10 cm).
  - C_SP, C_AT: Total carbon (%), dry weight, 0–10 cm.
  - N_SP, N_AT: Total nitrogen (%), dry weight, 0–10 cm.
  - CN_SP, CN_AT: Carbon-to-nitrogen ratio, 0–10 cm.
  - Nmin_SP, Nmin_AT: Nitrogen mineralisation rate (mg N kg-1 day-1), 0–10 cm.
  - DOC_SP, DOC_AT: Dissolved organic carbon (mg C kg-1 soil), 0–10 cm.
  - TDN_SP, TDN_AT: Total dissolved nitrogen (mg N kg-1 soil), 0–10 cm.
  - Nitrate_SP, Nitrate_AT: Extractable nitrate (mg NO3--N kg-1 soil).
  - Ammon_SP, Ammon_AT: Extractable ammonium (mg NH4+-N kg-1 soil).
  - Phosph_SP, Phosph_AT: Extractable phosphate (mg PO43--P kg-1 soil).
  - Na_SP, Na_AT; K_SP, K_AT; Ca_SP, Ca_AT: Extractable Na, K, Ca (mg kg-1 soil).
- All spring (SP) and autumn (AT) values correspond to the specified extraction/measurement methods and depths noted above.

## Data provenance and quality assurance
- Authors must be acknowledged if data are reused or reproduced.
- Methods and references included to enable reproducibility and cross-checking with standard soil analysis techniques.
- Data were visually checked for quality assurance and use of certified reference materials ensures traceability.

## Usage notes and references
- Primary purpose: characterize soil properties relevant to greenhouse gas emission monitoring from urine-treated pasture.
- Useful for analyses of seasonal soil property variation, nutrient status, and microbial/biotic activity indicators.
- References cited for methods:
  - Ball (1964) for loss-on-ignition.
  - Miranda et al. (2001) for nitrate/nitrite detection.
  - Mulvaney (1996) for inorganic nitrogen forms.
  - Voroney et al. (2008) for microbial biomass measurements.
  - Waring & Bremner (1964) for ammonium production index.
- Field site and study context provide baseline soil characteristics for interpreting emission measurements.