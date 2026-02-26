# Supporting information for the dataset: UK Environmental Change Network (ECN) Cairngorm Spider Data 2004-2019 Andrews, C. and Dick, J. Sept. 2021

- Purpose and scope
  - Provides supporting documentation for the ECN spider dataset collected at the Cairngorm field station.
  - Data used to analyze temporal trends in spider diversity across three habitats (pine woodland, wind-clipped heath, bog) from 2004–2019.
  - All specimens identified by the same expert araneologist to ensure consistency.

- Location and study area
  - Allt a' Mharcaidh catchment, Cairngorms National Park, Scotland (approximately 57° 6' 28"N, 3° 50' 6"W).
  - Elevation range: 320–1111 m a.s.l.; area ~10 km²; includes part of Invereshie and Inchriach NNR.
  - Transects focused on west-facing slopes north of the catchment (460–690 m a.s.l) across three habitats:
    - I. Woodland transect: mature Scots Pine woodland with Vaccinium myrtillus.
    - II. Heath transect: wind-clipped Calluna-Cladonia dry heath with bare patches.
    - III. Bog habitat: blanket mire with Eriophorum vaginatum and Molinia caerulea.

- Sampling protocol
  - For each habitat, 100 m transect with 10 pitfall traps 10 m apart.
  - Trap design: polypropylene pot (75 mm × 105 mm) buried flush with ground, filled with ethylene glycol to 30 mm depth; protective 20 mm2 galvanized mesh to exclude small vertebrates; 140 mm rain cover with ~30 mm ground gap.
  - Sampling frequency: fortnightly from ~April to end October, start date depending on snow-free conditions.
  - Specimen handling: all captured spiders identified to species and sex by the same expert araneologist; specimens stored at UKCEH Edinburgh for future work.
  - Data strategy: samples aggregated by habitat for each collection period.

- Data structure and formats
  - Data provided in a long-format CSV.
  - Key fields:
    - Year (YYYY)
    - Date (DD/MM/YYYY)
    - Month (MMM)
    - Week (2-digit)
    - Habitat (Bog, Heath, Wood)
    - Transect (e.g., T1)
    - Transect age (Old = pre-2007, New = post-2007)
    - Family (e.g., Linyphiidae)
    - Species (e.g., Hilaira frigida)
    - Male (count)
    - Female (count)
    - Total (male + female)
  - All specimens counted per species per habitat per transect and time point.

- Quality control and caveats
  - Transects were relocated in 2007; data from pre- and post-relocation should be treated with caution in long-term analyses.
  - 2007 and 2008 included an overlap where both old and new transects were sampled to aid continuity.
  - Yearly sampling effort varies due to weather and operational issues; standardization should use the period between first and last trapping dates rather than raw sampling counts.
  - Traps remained in place even if collection dates were missed, allowing calculation of trapping effort over the season.
  - Data labelled to indicate which transect belongs to old vs. new setups to support correct interpretation.

- Data availability and references
  - Specimens stored at UKCEH Edinburgh; data can be used for future research needs.
  - Related publications:
    - Andrews, C., Snazell, R., Dick, J. (2020). Temporal trends in spider communities at the UK Environmental Change Network Cairngorm field station, 2007-2019: data analysis report. UKCEH (Project no. 04404, 06953). http://nora.nerc.ac.uk/id/eprint/528208
  - Additional protocol details available at ECN website (measurements/terrestrial/i/ia).