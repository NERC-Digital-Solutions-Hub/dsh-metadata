# Methods, metadata and summary for fish monitoring at Akrotiri up to 22 nd March 2019 (IJW)

- Project context
  - Part of Defra Darwin Initiative Plus Project DPLUS056: Assessment and monitoring of current and future IAS in Cyprus to establish baseline data on native and non-native fish populations in the Sovereign Base Area of Akrotiri.

- Organisations involved
  - Centre for Ecology & Hydrology (CEH)
  - Joint Services Health Unit
  - Akrotiri Environmental Education Centre
  - Water Development Board of Cyprus

- Sampling methods
  - Primary gear: baited mesh traps (A25) measuring 55 x 24 x 24 cm with 3 mm mesh; baited with halibut pellet.
  - Trap configurations:
    - Submerged: traps placed on the water body bottom inshore at ~1 m depth.
    - Semi-submerged: traps positioned near the water surface with openings spanning the surface.
  - Deployment: two configurations at each time/place, fished for ~24 hours; fish collected in water-filled trays, identified, sexed, and returned.
  - Study sites: 9 water bodies (6 pools P1–P6; 3 channels C1–C3) sampled Feb–Mar 2018; regular monitoring ~every 2 weeks at one pool (P1) and one channel (C2) through Jan 2019; relocation from P1 Bay to P1 Main due to water level changes.
  - Additional surveys:
    - Two CEN standard bottom-set nets at the largest pool (P1) on 27 Feb 2019, left overnight; nets ~1.5 m deep, 30 m long, 12 panels with varying bar-mesh sizes (5–55 mm).
    - Day-time visual fish surveys at P1 and channels C4–C6 between 26 Feb and 1 Mar 2019.

- Data collection and measurements
  - Location data: site GPS position recorded with a Garmin GPSMAP 62s on first visit.
  - Environmental measurements (26 Feb 2018 – 25 Jan 2019): water temperature (°C), dissolved oxygen (% and μg/L), conductivity (μS/cm).
  - Sea comparison: conductivity measured in adjacent sea on 27 Feb 2018.
  - Additional temperature measurements: 7 Mar 2019 – 22 Mar 2019.
  - Biological data:
    - Species detected: Aphanius fasciatus (Mediterranean killifish) and Gambusia holbrooki (Eastern mosquitofish).
    - Sex recorded when obvious (M for male); fork length (mm) recorded where available.
    - Trap data: counts per trap type (SUBM = Submerged, SEMI = Semi-submerged) and per species; total per trap set.

- Metadata and data structure
  - Data files (CSV) and descriptions:
    - Akrotiri_aquatic_environment_26_2_18_22_3_19: sampling site locations and environmental measurements.
    - Akrotiri_fish_26_2_18_22_3_19: all fish observations.
    - Akrotiri_traps_26_2_18_22_3_19: trap observations (including counts per species).
  - Column details (examples):
    - Date, Site_code, Site_full_name, Lat_(N), Lon_(E)
    - Temp, DO_per, DO, Cond
    - Trap_Type, Trap_number, Aphanius, Gambusia, Sex, Length, Total
  - Site coding: P1–P6 (pools) and C1–C3 (channels); additional surveys include C4–C6.

- Data quality and limitations
  - QA/QC performed by experienced CEH staff; data reviewed and digitised by CEH staff; training provided to local partner.
  - Missing data/issues:
    - Equipment failure caused gaps after 25 Jan 2019 (some aquatic environmental data missing).
    - Thermometer missing after 7 Mar 2019 (DO and conductivity data still available from other equipment where applicable).
    - Missing data on 28 Feb 2018 for P1 Main; P1 Bay and P1 Main considered broadly comparable due to proximity.

- GIS-relevant notes
  - Georeferenced, time-stamped environmental and biological data suitable for map-based analyses and temporal GIS visualizations.
  - Clear site coding and standardized data schemas facilitate spatial joins, trend analyses, and cross-site comparisons of species presence, abundance, and environmental conditions.