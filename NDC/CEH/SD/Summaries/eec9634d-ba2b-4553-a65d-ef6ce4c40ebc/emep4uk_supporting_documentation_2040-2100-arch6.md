# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 2040, 2070 and 2100 for SSP scenarios 1-5

## Overview
- Provides annual total atmospheric deposition over the UK for cadmium (Cd), copper (Cu), nickel (Ni), lead (Pb), zinc (Zn), sulphur (S), and nitrogen (N) for years 2040, 2070, and 2100 under SSP scenarios 1–5.
- Based on the EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM) with 3D meteorology from the WRF model v4.2.2.
- Model domain covers the EU at 27×27 km2 resolution with a nested UK domain at 3×3 km2; UK results are extracted.
- Meteorology uses 2018 conditions; emissions for UK components drawn from NAEI 2019 (rescaled to 2018) and CEIP 0.1° for non-UK emissions; heavy metal emissions use UK-specific SSP-based histories.
- Outputs exist as 15 NetCDF files with annual deposition fields; postprocessing only extracts the target variables; global QA/QC reports are available on request.

## Data sources and modeling approach
- ACTM: EMEP MSC-W model rv4.36; meteorology: WRF v4.2.2 with data assimilation from NCEP/NCAR GFS reanalysis.
- UK and EU domains defined; 3×3 km2 UK grid nested within 27×27 km2 EU grid.
- Emissions inputs:
  - UK: NOx, NH3, SO2, primary PM2.5, primary PM coarse, CO, NMVOC from NAEI 2019 (rescaled to 2018).
  - Non-UK: CEIP 0.1° resolution emissions for general species.
  - Metals: historical 1750–1960 from literature; 1970–2018 from UK emissions inventory (NAEI 2021); projections (2040/2070/2100) via SSP UK-specific variants.
- Outputs reflect annual totals for heavy metals, nitrogen, and sulphur in both dry and wet deposition modes, plus rainfall (WDEP_PREC).

## Data files and structure
- File set: 15 NetCDF files named EMEP4UK_met2018_emisSSP#-YYYY.nc, where SSP# is 1–5 and YYYY is the year of emissions (outputs cover 2040, 2070, 2100).
- Spatial structure:
  - Dimensions: time (unlimited, currently 1 entry), lon (240), lat (240).
  - Grid defined in WGS84 with a specific projection string.
- Variables of interest (examples):
  - WDEP_PREC(time, lat, lon): rainfall (mm)
  - WDEP_SOX(time, lat, lon): wet deposition of oxidised sulphur (mgS/m2)
  - WDEP_OXN(time, lat, lon): wet deposition of oxidised nitrogen (mgN/m2)
  - WDEP_RDN(time, lat, lon): wet deposition of reduced nitrogen (mgN/m2)
  - WDEP_CD(time, lat, lon): wet deposition of cadmium (mg/m2)
  - WDEP_CU(time, lat, lon): wet deposition of copper (mg/m2)
  - WDEP_NI(time, lat, lon): wet deposition of nickel (mg/m2)
  - WDEP_PB(time, lat, lon): wet deposition of lead (mg/m2)
  - WDEP_ZN(time, lat, lon): wet deposition of zinc (mg/m2)
  - DDEP_SOX(time, lat, lon): dry deposition of oxidised sulphur (mgS/m2)
  - DDEP_OXN(time, lat, lon): dry deposition of oxidised nitrogen (mgN/m2)
  - DDEP_RDN(time, lat, lon): dry deposition of reduced nitrogen (mgN/m2)
  - DDEP_CD(time, lat, lon): dry deposition of cadmium (mg/m2)
  - DDEP_CU(time, lat, lon): dry deposition of copper (mg/m2)
  - DDEP_NI(time, lat, lon): dry deposition of nickel (mg/m2)
  - DDEP_PB(time, lat, lon): dry deposition of lead (mg/m2)
  - DDEP_ZN(time, lat, lon): dry deposition of zinc (mg/m2)
  - Area_Grid_km2: grid area (km2)
- Metadata:
  - History attribute documents postprocessing steps.
  - Time reference is middle of the meteorological year; example time unit is days since 1900-01-01.
- Notes:
  - The dataset includes QA/QC performed for 2018; remaining years rely on model comparisons; QA reports available on request.
  - The content is provided without warranty; interpretation should consider uncertainties in emissions and model physics.

## Variables and units (summary)
- Wet deposition: WDEP_PREC (mm), WDEP_SOX (mgS/m2), WDEP_OXN (mgN/m2), WDEP_RDN (mgN/m2), WDEP_CD/CU/NI/PB/ZN (mg/m2)
- Dry deposition: DDEP_SOX, DDEP_OXN, DDEP_RDN, DDEP_CD, DDEP_CU, DDEP_NI, DDEP_PB, DDEP_ZN (all mg/m2)
- Grid area: Area_Grid_km2 (km2)

## Postprocessing and metadata
- Postprocessing restricted to extracting the listed target variables; further transformations are documented in the NetCDF global attribute 'history'.
- Example NetCDF structure is provided to illustrate variable naming and dimensions.
- The linked historical dataset and related literature provide context for model evaluation and emissions data.

## Quality assurance and limitations
- QA/QC completed for 2018 (not included in this dataset) with additional visual checks for historical and future runs.
- QA reports available on request.
- Use of the dataset is at the user’s risk; no warranty of accuracy or fitness for a specific purpose.

## Access, provenance, and references
- Related datasets and prior emissions inventories cited (NAEI, CEIP, GFS/NCEP references).
- Bibliography includes foundational papers on EMEP4UK, WRF model, and UK emissions research.
- Data produced with specific software versions (EMEP4UK rv4.36, WRF v4.2.2) and compiled on the UKCEH POLAR cluster.