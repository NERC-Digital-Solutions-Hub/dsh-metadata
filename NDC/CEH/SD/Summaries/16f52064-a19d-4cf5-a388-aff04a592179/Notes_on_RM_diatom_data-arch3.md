# Sediment trapping using sequencing traps at Rostherne Mere (January 2011 – January 2017)

## Overview
- Long-term sediment trapping study conducted at Rostherne Mere to collect and analyse diatom assemblages and environmental context.
- Two trap depths (10 m and 25 m) with sequential 250 ml bottles representing ~2-week collection periods, extended to 3–4 weeks during January–February.
- Traps reset approximately every six months; samples were kept cool, dark, and sealed during transport and stored frozen prior to analysis.
- Data include diatom-based measures from trap sediments and concurrent environmental variables (air and water temperatures, wind).

## Methods

- Sediment trapping and sample preparation
  - Traps: Technicap PPS 4/3 automatic sequencing traps deployed at central lake location at 10 m and 25 m depths; 12 bottles per trap.
  - Sample handling: trap sediment freeze-dried and weighed for total dry sediment flux.
  - Diatom analysis: diatoms prepared with H2O2 digestion (room temperature, overnight), microspheres added for absolute counts, slides prepared for microscopy.
  - Counting: minimum of 300 diatom valves counted per slide; if fewer than 100 microspheres reached, counting continued without species IDs until 100 microspheres were reached.
  - Quality metrics: valve breakage categorized into four classes; dissolution recorded with pristine/dissolved binary scheme (F index).
  - Abundance and biovolume: total diatom abundance derived from relative counts; biovolume calculated for taxa >3% abundance using standard methods; 25 slides used to derive mean biovolume per taxon.

- Environmental data collection
  - Temperature: average daily air temperature (2 m above water) and water temperatures at 12 depths (2 m to 24 m, every 2 m) from the UKLEON buoy.
  - Stratification: Relative resistance to thermal mixing (RTRM) calculated from temperature-density profiles (epilimnion vs. hypolimnion).
  - Wind: wind speed from Manchester Airport station; corrected for local sheltering using a relationship with UKLEON buoy data (VRM correction).

## Data collected

- Temperature and wind data
  - Variables: daily mean air temperature, twelve water-depth temperatures, corrected wind speed, RTRM value.
  - Source: UKLEON buoy (for temperature) and Manchester Airport wind data (with site-specific correction).

- Sediment trap diatoms
  - Variables: trap type (open tube vs sequencing), trap depth (shallow 10 m vs deep 25 m), trap collection dates (start, end, duration, mid-date).
  - Diatom data: abundances and dissolution percentages for taxa, biovolume per taxa, total diatom cells per gram of sediment, diatoms sinking per cm² per day, diatom dissolution/breakage metrics, and biovolume totals per sample.
  - Additional metrics: spikes of Aulacoseira per 100 diatoms identified, overall sample dissolution (pristine vs dissolved fractions), and empty/missing data indicators.

## Data structure

- RMTemperatures (16 columns)
  - A: Date (DD/MM/YYYY)
  - B–N: Mean daily temperature data (air at 2 m, plus 12 water depths at 2 m intervals)
  - O: Wind speed (corrected regional wind speed)
  - P: RTRM (relative resistance to thermal mixing)

- RMTrapDiatoms (232 columns)
  - A: sample code
  - B: Trap depth (S = shallow at 10 m, D = deep at 25 m)
  - C: Trap type (O = Open tube, S = Automatic sequencing)
  - D–G: Dates (collection window: start, end, total days, mid-date)
  - H–HH: Taxa-specific data (for each taxon: percentage pristine, percentage dissolved, total percentage, biovolume)
  - HI–HJ: Overall sample dissolution metrics (pristine and dissolved)
  - HK: Total diatom cells per gram of sediment
  - HL: Total diatoms per cm² per day
  - HM: Additional spikes of Aulacoseira per 100 diatoms
  - HN–HU: Dissolution and breakage breakdown (undissolved, broken, dissolved, broken as percentages of whole diatom)
  - HV: Total biovolume per gram of sediment
  - HW: Total biovolume per cm² per day
  - HX: Total sediment flux per cm² per day
  - Notes: Empty cells indicate missing data; 0 values indicate true absence

## Data quality, metadata and governance

- Documentation provides explicit data fields, units, and calculation methods (e.g., RTRM calculations from density profiles, biovolume standards, and diatom counting conventions).
- Clear separation of environmental and diatom dataset components, enabling independent quality checks and integration.
- Data appear to be structured for transfer to CSV-based repositories with extensive column-level metadata, supporting traceability and reuse.
- Potential data sharing considerations noted in broader monitoring context include the need for transparent metadata and data governance to support reuse and comparability.

## References

- Battarb ee et al. (2001) Diatoms. In: Tracking Environmental Change Using Lake Sediments.
- Battarb ee & Kneen (1982). Use of microspheres in diatom analysis.
- Hillebrand et al. (1999). Biovolume calculations for microalgae.
- Renberg (1990). Diatom slide preparation procedures.
- Ryves et al. (2003, 2006). Diatom assemblage relationships and dissolution predictors.
- Wetzel (2001). Limnology: lake and river ecosystems.