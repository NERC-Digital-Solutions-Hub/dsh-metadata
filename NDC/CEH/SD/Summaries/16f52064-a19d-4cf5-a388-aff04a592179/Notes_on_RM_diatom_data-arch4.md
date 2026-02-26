# Supporting Documentation

## Overview
- Describes sediment trapping and diatom analysis at Rostherne Mere from January 2011 to January 2017.
- Aims to quantify diatom assemblages, sediment flux, and environmental drivers (temperature, wind, stratification).
- Two primary data products: temperature/wind profiles and diatom trap data.

## Data Collection and Contents
- Trap deployment:
  - Technicap PPS 4/3 automatic sequencing traps deployed at 10 m (shallow) and 25 m (deep) depths, connected to 12 × 250 ml HDPE bottles per trap.
  - Sampling period ~2 weeks per bottle; longer periods (3–4 weeks) used in January–February.
  - Traps reset about every 6 months; sediment kept cool, dark, sealed; stored frozen prior to analysis.
- Diatom analysis:
  - Freeze-dried trap sediment prepared using standard peroxide digestion (Renberg 1990; Battarbee et al. 2001).
  - Added microspheres for absolute diatom counts (Battarb ee & Kneen 1982).
  - Counting: at least 300 diatom valves per slide; valves categorized by integrity (4 classes) and dissolution (pristine/dissolved).
  - If <100 microspheres, counting continued without species ID until 100 microspheres reached.
  - Calculations:
    - Total diatom abundance from relative counts using microsphere counts (Battarbee & Kneen 1982).
    - Biovolume calculated for taxa >3% abundance (Hillebrand et al. 1999) with mean values from 25 slides.
- Environmental context:
  - Temperature: average daily air temp (2 m above water) and water temps at 12 depths (2 m increments from 2–24 m) from the UKLEON buoy.
  - Stratification: relative resistance to thermal mixing (RTRM) derived from temperature-density relationships (Wetzel 2001).
  - Wind: wind speed from Manchester Airport; adjusted for local sheltering (VRM) using UKLEON buoy data (Feb 2013–Jan 2017) with a correction factor VRM = 0.55VMA − 0.12 (R2 = 0.82, p < 0.001).

## Data Structure and Variables
- Datasets:
  - RMTemperatures: 16 columns.
  - RMTrapDiatoms: 232 columns.
- RMTemperatures content:
  - Date: DD/MM/YYYY (Column A).
  - Columns B–N: mean daily temperatures from UKLEON buoy (air temp at 2 m) and 12 water depths (2 m to 24 m, every 2 m).
  - Column O: corrected wind speed (regional, on-lake buoy).
  - Column P: RTRM value (density-based metric).
- RMTrapDiatoms content:
  - Column A: sample code.
  - Column B: trap depth (S = 10 m, D = 25 m).
  - Column C: trap type (O = Open tube, S = Automatic sequencing).
  - Columns D–G: trap dates (start, end, total days, mid-date).
  - Columns H–HH: diatom taxa data (for each taxon: % pristine, % dissolved, % total, biovolume in µm³ cm⁻²); 0 = not present.
  - Columns HI–HJ: dissolution breakdown (% pristine, % dissolved) for the whole sample.
  - Column HK: total diatom cells per gram of sediment.
  - Column HL: diatoms sedimenting per cm² per day.
  - Column HM: additional spikes of Aulacoseira per 100 diatoms.
  - Columns HN–HU: dissolution and breakage breakdown (percent undissolved, broken, and dissolved components).
  - Column HV: total biovolume per gram of sediment.
  - Column HW: total biovolume sedimenting per cm² per day.
  - Column HX: total sediment flux per cm² per day.

## Data Quality, Standards, and Provenance
- Use of established diatom preparation and quantification protocols; explicit QC steps (minimum counts, correction via microspheres, dissolution classification).
- Standard references underpin methods (Renberg 1990; Battarbee et al. 2001; Battarbee & Kneen 1982; Hillebrand et al. 1999; Ryves et al. 2003, 2006; Wetzel 2001).
- Data units and formats are specified (temperatures in °C, wind in m/s, RTRM as a numeric index; diatom abundances and biovolume with specified units).

## Data Access, Use, and Documentation
- Data delivered as two CSV files with clearly labeled columns and documented data structure.
- Missing data represented by empty cells or 0 values in applicable fields.
- Documentation provides methodological context, calculation approaches, and references to enable reproducibility and audit trails.

## Practical Implications for Data Leaders
- Clear data lineage from trap deployment through diatom analysis to final metrics (abundance, biovolume, flux).
- Comprehensive metadata supports cross-site comparisons and integration with other lake sediment records.
- Explicit QA steps and standardized methods facilitate data quality assurance, provenance tracking, and governance.
- Well-structured datasets support reuse for analyses of sedimentation rates, diatom community change, and climate-ecosystem linkages.