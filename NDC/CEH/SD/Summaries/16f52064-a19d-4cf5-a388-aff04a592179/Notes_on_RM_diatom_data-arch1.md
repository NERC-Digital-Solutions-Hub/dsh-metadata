# Supporting Documentation

## Overview
- Document describes a sediment-trapping and diatom-analysis study at Rostherne Mere (Jan 2011 – Jan 2017).
- Two main data streams: sediment trap flux data and diatom-assemblage data, plus environmental context (air/water temperature, wind, and stratification measures).
- Data are organized into two CSV files: RMTemperatures and RMTrapDiatoms, enabling analyses of sediment flux, diatom preservation, community composition, and mixing dynamics.

## Sampling design and sample processing
- Sediment traps: Technicap PPS 4/3 sequencing traps deployed at central lake location at 10 m (shallow) and 25 m (deep) depths.
- Collection intervals: ~2 weeks per bottle, with longer (3–4 weeks) collections in January–February; traps reset ~every 6 months.
- Sample handling: trap sediment freeze-dried, weighed for total dry sediment flux; processed for diatoms after H2O2 digestion; microspheres added for absolute quantification; slides prepared and diatoms counted.
- Diatom analysis: identify at least 300 diatom valves per slide; record valve integrity (pristine, dissolved) and dissolution using F index; continue counting until 100 microspheres achieved if necessary.
- Biovolume: calculated for taxa with >3% abundance using standard biovolume methods; mean taxon biovolume derived from 25 slides.
- Auxiliary data: temperature and wind data sourced from UKLEON buoy and Manchester Airport, with wind correction to account for local sheltering.

## Data products and structure
- RMTemperatures (16 columns)
  - Date (DD/MM/YYYY).
  - Temperature data: mean daily air temperature (2 m above lake) and temperatures at 12 water depths (2–24 m, every 2 m).
  - Wind speed: corrected regional wind speed.
  - RTRM: relative resistance to thermal mixing derived from temperature-density relationships.
- RMTrapDiatoms (232 columns)
  - Sample metadata: sample code, trap depth (S = 10 m, D = 25 m), trap type (O = Open tube, S = Sequencing).
  - Dates: begin, end, total collection days, mid-date.
  - Diatom taxa data: for each taxon, four values (pristine %, dissolved %, total % presence, biovolume in µm3 per sample).
  - Overall dissolution metrics: total pristine and total dissolved percentages.
  - Totals: diatoms per gram of sediment; diatoms per cm2 per day; Aulacoseira spikes per 100 diatoms (where present).
  - Dissolution and breakage: dissolution/breakage breakdown by undissolved and dissolved fractions.
  - Biovolume metrics: total biovolume per gram of sediment; biovolume per cm2 per day; sediment flux per cm2 per day.
  - Data completeness: empty cells indicate missing data; 0 values reflect true absence for taxa data.
- Referenced standards: diatom identification and analysis follow Battarbee et al. and related methodological works; biovolume calculations follow Hillebrand et al.

## Key measurements, units, and data quality
- Temperature: degrees Celsius (°C).
- Wind: meters per second (m/s).
- RTRM: numeric index (relative resistance to thermal mixing).
- Diatom counts and biovolume: percent abundances, biovolume in µm3, per gram of sediment or per cm2 per day.
- Data quality notes:
  - Sample handling ensured cold, dark, and sealed transport; sediments freeze-dried prior to analysis.
  - Minimum counts: requires at least 100 microspheres; otherwise counting continues without species IDs.
  - Some columns may be empty to indicate missing data; true zeros indicate absence.
  - Wind correction uses a regression-based factor to align airport wind data with on-lake conditions.

## Temporal and spatial scope
- Timeframe: January 2011 – January 2017.
- Spatial scope: Rostherne Mere, central lake location with two depths sampled (10 m and 25 m).

## References and methodology context
- Diatom processing and microsphere quantification: Battarbee et al. 1982; Battarbee et al. 2001.
- Biovolume calculations: Hillebrand et al. 1999.
- Diatom slide preparation and diatom dissolution: Renberg 1990; Ryves et al. 2003, 2006.
- General limnology methodology: Wetzel 2001.

## Potential uses
- Correlate sediment trap flux with diatom community structure and dissolution patterns.
- Explore links between RTRM, stratification strength, wind forcing, and diatom preservation.
- Model temporal changes in diatom assemblages and sedimentation under varying climatic conditions.
- Integrate with other datasets to support environmental-change inferences and policy-relevant decisions.