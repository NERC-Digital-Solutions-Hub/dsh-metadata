# West Halladale wildfire burn severity and peat core analysis

- Study area and wildfire context:
  - Wildfire in Flow Country peatlands, Caithness and Sutherland, Scotland, burning ~60 km2 of wet heath and blanket bog within a 4000 km2 blanket bog area.
  - Fire originated between Melvich and Strathy along the A836 and spread southwards toward the RSPB Forsinard Flows NNR.
  - Burn severity mapped by NatureScot; plots categorized as low, medium, or high severity. High severity mainly in drained peatland areas; no high severity in near-natural southern end.

- Sampling design and plot coding:
  - 34 short cores (50 cm) collected within the wildfire footprint.
  - Plots selected across severity x drainage combinations using a quarter-BNG area; plots coded by severity (H, M, L) and drainage (N for near-natural when applicable) plus a 1–15 index.
  - Drained areas distributed across northern and mid-west regions; near-natural (M/L) plots located in the southern near-natural zones (Uair and Dyke within Forsinard Flows NNR).

- Field sampling logistics:
  - Five field visits between late February and mid-March 2020; final core count: 34 due to accessibility constraints (steep slopes, peat depth, deer stalking, etc.).
  - Core collection criteria: depth >40 cm and suitable for coring; bottom-left plot coordinates recorded with GPS.
  - Equipment: GPS, printed maps, Russian corer, PVC half-pipes, saran wrap, measuring tape, camera; cores labelled with codename.

- Sample handling and storage:
  - Field notes captured (date, observer, severity, codename, depth, coordinates, elevation, vegetation); field photos taken.
  - Data transcribed to “Peat_core_coordinate.csv” and stored in the ERI server with quality checks.
  - Cores returned to cold storage for laboratory analysis; some cores held during Covid-related restrictions in July 2020.

- Instruments and calibration:
  - Field tools: GPS, maps, Russian corer, PVC half-pipes, measuring tape, camera.
  - Laboratory tools: balances (five- and four-decimal), 100 mL graduated cylinder for volume via water displacement, oven (105°C), muffle furnace (550°C), desiccator, crucibles, Milli-Q water.
  - Balances calibrated per manufacturer instructions using standard weights.

- Data structure and metadata:
  - Field metadata (dataset: Peat_core_coordinate.csv):
    - COREID: unique ID (letters H/M/L, N-M, N-L) plus number.
    - Depth: 40–50 cm.
    - Lat_(Y)_OSGB, Long_(X)_OSGB: OSGB coordinates.
    - Grid_Reference: British Grid Reference.
    - Alt_masl: altitude above sea level.
    - Exposure: slope aspect/angle.
    - Vegetation: surrounding vegetation description.
  - Laboratory measurements (dataset: Peat_core_data.csv) for each 5 cm sub-section:
    - SEVERITY: LOW, MEDIUM, HIGH.
    - TYPE: DRAINED or UNDRAINED.
    - COREID, DEPTH (cm): 0–50 cm sub-samples.
    - VOL (cm3): volume from water displacement (3–10 cm3).
    - WET_PEAT (g), DRY_PEAT (g): weights for LOI calculations.
    - BD (g cm-3): bulk density.
    - MOIST%: moisture percentage.
    - vonPOST: humification index (1–10).
    - WET_PEAT10, DRY_PEAT10 (g): LOI at 10 g sample basis.
    - ASHg (g): ash weight after LOI.
    - OM%: organic matter percentage.
    - ASH%: inorganic residue percentage.
    - OC%: organic carbon percentage (OC% = OM%/2).
  - Range expectations and units are specified for each parameter to ensure unambiguous interpretation.

- Analytical methods and calculations:
  - Bulk density (BD): dry peat mass divided by water-displacement volume; BD in g cm-3.
  - Moisture content (MOIST%): [(Wet − Dry)/Wet] × 100.
  - Organic matter (OM) and LOI: LOI at 550°C for 4 h; OM% = LOI / md(105°C) × 100.
  - Ash content (ASH%): (md(550°C) / md(105°C)) × 100; or 100 − OM%.
  - Organic carbon (OC%): OC% = OM% / 2 (Beilman et al., 2009).
  - Von Post Scale: qualitative peat humification classification (H1–H10) based on squeezing tests and colour/texture changes.
  - Protocols followed (adapted from Chambers et al. 2011; Heiri et al. 2001; Ekono 1981; Beilman et al. 2009).
  - Sub-sample data screened for errors; three sub-samples with weighing errors removed to prevent spurious results.

- Data management and provenance:
  - Data generated from 34 cores across 5 field visits; most analyses completed shortly after collection; pandemic-related delays for some cores.
  - Datasets intended to be discoverable and usable via metadata; stored on ERI server with versioned files and explicit documentation.
  - Analytical references provided for methodological validation (Beilman et al. 2009; Chambers et al. 2011; Ekono 1981; Heiri et al. 2001; Melling et al. 2006; Ratcliffe et al. 2018a,b).

- Key references:
  - Beilman, Beilman et al. (2009)
  - Chambers, Beilman, Yu (2011)
  - Ekono (1981)
  - Heiri, Lotter, Lemcke (2001)
  - Melling, Lau, Goh, et al. (2006)
  - Ratcliffe, Payne, Sloan, et al. (2018a, 2018b)

- Data utility for analysts:
  - Provides a structured, multi-scale peat core dataset across burn severity and drainage types, enabling correlations between burn severity, peat properties (bulk density, moisture, organic matter, carbon), and decomposition (von Post) across 0–50 cm depth intervals.
  - Facilitates reconstruction of post-fire carbon dynamics and peatland recovery trajectories with clearly defined metadata and transparent laboratory protocols.