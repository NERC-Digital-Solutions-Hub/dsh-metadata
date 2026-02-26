# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2021 Andrews, C., Sanzell, R., Dick, J. Dec. 2022

## Overview
- Provides supporting documentation for the ECN spider dataset collected 2004–2021.
- Spiders were collected using standard ECN pitfall-trap protocol across three habitats and identified by a single expert araneologist for consistency.
- Related report (Andrews et al., 2020) detailing methods and temporal trends is available; protocols are accessible via ECN resources.

## Location and study sites
- Allt a'Mharcaidh catchment, Cairngorms National Park, Scotland (57° 6' 28"N, 3° 50' 6"W).
- Elevation: 320–1111 m a.s.l.; area ~10 km²; includes part of Invereshie and Inchriach NNR.
- Transects focused on west-facing slopes north of the catchment (460–690 m a.s.l.), spanning three habitats:
  - Woodland transect at 460 m a.s.l. in mature Scots Pine woodland.
  - Heath transect at 690 m a.s.l. in wind-clipped Calluna-Cladonia dry heath.
  - Bog transect at 690 m a.s.l. in blanket mire (Eriophorum vaginatum and Molinia caerulea).

## Sampling protocol
- For each habitat: a 100 m transect with 10 pitfall traps 10 m apart.
- Trap specifications: polypropylene pots (75 mm × 105 mm), buried flush, filled with ethylene glycol to 30 mm depth; galvanized mesh (~20 mm²) to deter small vertebrates; 140 mm rain cover with ~30 mm gap to ground.
- Sampling frequency: fortnightly from ~April to end of October (start date depends on snow-free conditions).
- Specimens identified to species and sex (from 2006 onwards) by the same expert araneologist; all specimens stored at UKCEH Edinburgh.

## Data structure and units
- Data provided in long-format CSV with fields:
  - Year (YYYY)
  - Date (DD/MM/YYYY)
  - Month (MMM)
  - Week (2-digit)
  - Habitat (Bog, Heath, Wood)
  - Transect (e.g., T1)
  - Transect_age (Old for pre-2007, New for post-2007)
  - Family (taxonomic family)
  - Species (full species name)
  - Male (count; from 2006 onwards)
  - Female (count; from 2006 onwards)
  - Total (male + female)

## Quality control and caveats
- Transects were relocated in 2007; data labelled to distinguish pre- and post-relocation (overlap years 2007–2008 used for continuity).
- Annual sampling effort is variable due to weather, snow, or technical issues; standardisation should use the period between first and last trapping rather than raw sampling effort.
- Traps remained in place even when sampling days were missed, allowing calculation of trapping effort over the season.
- COVID-19 (2020) reduced sampling frequency to monthly during May–July; overall between-year duration for analysis remained unaffected.

## References and data access
- Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007‑2019: data analysis report. UKCEH. Available via Nora (and protocol PDFs at ECN site).