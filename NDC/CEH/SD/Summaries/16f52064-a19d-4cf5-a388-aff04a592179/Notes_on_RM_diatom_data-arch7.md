# Supporting Documentation

## Overview
- Sediment trapping using sequencing traps conducted at Rostherne Mere from January 2011 to January 2017.
- Deployment: Technicap PPS 4/3 automatic sequencing traps placed at 10 m (shallow) and 25 m (deep) water depths, opening into 12 bottles per trap representing ~2-week collection periods (longer 3–4 week periods used in January and February).
- Trap maintenance: Traps reset roughly every 6 months; trap sediment kept cool, dark, sealed during transport; stored frozen prior to analysis.
- Samples were freeze-dried and weighed for total trap sediment flux prior to diatom analysis.

## Sample processing and diatom analysis
- Diatom preparation: Freeze-dried sediment treated with concentrated H2O2 at room temperature; microspheres added before slide preparation for absolute counts.
- Counting: Minimum 300 diatom valves counted per slide; if fewer than 100 microspheres were reached, counting continued without species identification until 100 microspheres were reached.
- Quality metrics: Valve breakage categorized into four classes; dissolution recorded using a pristine/dissolved binary scheme (F index).
- Abundance and biovolume: Total diatom abundance calculated from relative counts to known microsphere abundances; diatom biovolume calculated for taxa with >3% abundance.
- Biovolume methodology: Following Hillebrand et al. (1999); mean biovolume derived from 25 representative slides per taxon.

## Environmental data
- Temperature and wind: Average daily air temperature (2 m above water) and water temperatures at 12 depths (2 m to 24 m, every 2 m) obtained from the UKLEON buoy.
- Stratification: Relative resistance to thermal mixing (RTRM) calculated from temperature-density profiles; strong stratification defined by the density difference between epilimnion and hypolimnion.
- Wind correction: Wind speed data from Manchester Airport corrected for sheltering using comparisons with the UKLEON buoy data (VRM correction).

## Data types and values
- Temperature data: Air and water temperatures (°C).
- Wind data: Wind speed (m/s) corrected to local conditions.
- RTRM: Numeric resistance value indicating stratification strength.
- Sediment trap data: Trap type, collection dates, collection duration, diatom taxa abundances (pristine and dissolved), diatom biovolume (µm³ cm⁻²), total diatom cells/sediment, dissolution and breakage metrics, total biovolume, and flux metrics.

## Data structure and files
- Two CSV files: RMTemperatures and RMTrapDiatoms.
- RMTemperatures (16 columns, A–P):
  - A: Date (DD/MM/YYYY)
  - B–N: Temperature data (mean daily air temperature at 2 m and 12 water depths at 2 m intervals)
  - O: Wind speed (corrected regional)
  - P: RTRM (calculated from temperature profiles)
- RMTrapDiatoms (232 columns, A–HX/HX–HZ as specified):
  - A: Sample code
  - B: Trap depth (S = shallow 10 m, D = deep 25 m)
  - C: Trap type (O = Open tube, S = automatic sequencing)
  - D–G: Dates (start, end, total days, mid-date)
  - H–HH: Diatom taxa data (for each taxon: pristine %, dissolved %, total %, biovolume)
  - HI–HJ: Overall sample dissolution (pristine and dissolved %)
  - HK: Total diatom cells per gram of sediment
  - HL: Total diatoms sedimenting per cm² per day
  - HM: Number of additional spikes of Aulacoseira per 100 diatoms
  - HN–HU: Dissolution and breakage breakdown (undissolved, broken, dissolved per taxon)
  - HV: Total biovolume per gram of sediment
  - HW: Total biovolume sedimenting per cm² per day
  - HX: Total sediment flux per cm² per day
  - Note: 0 values indicate none present; empty cells denote missing data.

## References and methodological context
- Diatom analysis and standard methods (Renberg 1990; Battarbee et al. 2001).
- Use of microspheres for absolute diatom counts (Battarbee & Kneen 1982).
- Biovolume calculations (Hillebrand et al. 1999).
- Diatom dissolution predictors and relationships (Ryves et al. 2003; 2006).
- Relationship between planktonic assemblages and sedimentary records (Ryves et al. 2003; Baikal studies).
- General limnology framework (Wetzel 2001).

## GIS and data integration notes for use
- The dataset provides time-stamped, depth-specific diatom and environmental measurements suitable for GIS-based temporal analyses and layered mapping.
- Data can be linked with spatial basemaps of Rostherne Mere deployment sites (10 m and 25 m depths) for visualization of diatom assemblage changes over time and depth.
- Potential integration with additional environmental layers (water temperature, wind, stratification proxies) to examine spatial-temporal drivers of sedimentation and diatom dissolution.