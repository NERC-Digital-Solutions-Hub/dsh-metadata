# Amazon Fertilization Experiment (AFEX)

- Study area and context
  - Conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil (41 km along the ZF-3 road of BR-174; coordinates around 02 24'S, 59 52'W).
  - Soils: clay-rich Ferrasols (~30% of the Amazon Basin). Climate: 1,900–2,500 mm annual rainfall with a pronounced dry season (June–October).
  - Forest baseline: above-ground biomass (AGB) 322 ± 54 Mg ha-1 (≥10 cm dbh); mean wood density ~0.67 g cm-3; ~280 species per hectare (≥10 cm dbh).

- Amazon Fertilization Experiment (AFEX) design
  - Start: March 2017; full factorial design with eight treatments and four replicates per treatment (32 plots total) across four independent blocks (≥200 m apart).
  - Treatments (eight total): Control; nitrogen (N); phosphorus (P); cations; N + P; N + cations; P + cations; N + P + cations.
  - Plot layout: each plot 50 × 50 m, with at least 50 m separation; all plots located in areas with similar soil, vegetation, and topography.
  - Fertilization regime: annual application divided into three injections to mitigate nutrient leaching and runoff.
  - Fertilizer specifics:
    - N: 125 kg N ha^-1 year^-1 as urea
    - P: 50 kg P ha^-1 year^-1 as triple superphosphate
    - Cations: 50 kg K ha^-1 year^-1 as KCl; 160 kg Ca ha^-1 year^-1 as dolomitic limestone; 160 kg Mg ha^-1 year^-1 as dolomitic limestone

- Data collection methods (LAI measurements)
  - Instrument: LAI-2200 C; 36 sampling points per plot (LAI_5_rings, LAI_4_rings, LAI_3_rings) to capture foliage area index at different zenith angles.
  - Procedure: measurements from 6:00–17:00, avoiding 12:00–14:00; optical sensor above canopy reference and below-canopy readings logged with a fixed clearing setup; sensors oriented west in the morning and east in the afternoon; 45° view cap; sensor cross-calibration performed before data collection.
  - Data processing: LAI calculated using FV2200 software with 5, 4, and 3 rings.
  - Sampling timeline: October 2017, March 2018, August 2018, and October 2018.
  - Data collection context: implemented within the AFEX fertilization experiment in Central Amazon ( Amazonas, Manaus region).

- Data spreadsheet and data management
  - Contents and structure (example fields):
    - CENSO: PlotID (combination of block and plot codes)
    - B_Obs: the 36 sampling points
    - Time: time of measurement (hours, minutes, seconds) for each LAI_5_rings, LAI_4_rings, LAI_3_rings series
    - LAI_5_rings; LAI_4_rings; LAI_3_rings: LAI values (one per ring configuration)
    - Date: campaign date (YYYY_Month)
    - coord x; coord y: planimetric coordinates (0, 10, 20, 30, 40, 50 m) within plots
  - Data provenance: spreadsheets deposited in the EIDC system with metadata; column descriptions explain the ring configurations and time stamps for each LAI measure.
  - Purpose: enables analysis of LAI responses to fertilization treatments and interactions, with precise plot, time, and spatial referencing for downstream statistical modeling.

- References (related foundational work)
  - Duque et al. 2017; De Oliveira & Mori 1999; Quesada et al. 2011; Rankin de Merona et al. 1992 (provide context on forest structure, soil types, and regional Amazonian patterns).