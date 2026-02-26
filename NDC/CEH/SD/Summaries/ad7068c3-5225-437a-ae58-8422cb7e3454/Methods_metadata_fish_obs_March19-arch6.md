# Methods, metadata and summary for fish monitoring at Akrotiri up to 22 nd March 2019 (IJW)

- Project and organisations
  - Part of Defra Darwin Initiative Plus Project DPLUS056: Assessment and monitoring of IAS in Cyprus to establish baseline data on native and non-native fish in Akrotiri.
  - Sampling conducted by Centre for Ecology & Hydrology (CEH), Joint Services Health Unit, Akrotiri Environmental Education Centre, and Water Development Board of Cyprus.

- Sampling design and field methods
  - Primary gear: baited mesh traps (55 x 24 x 24 cm; 3 mm mesh; trap type A25).
  - Bait: single halibut bait pellet.
  - Two trap configurations:
    - Submerged: placed on the water body bottom inshore at depths up to ~1 m.
    - Semi-submerged: traps span the water surface in extreme inshore locations.
  - Procedure: after deployment (~24 hours), fish were transferred in water to shallow trays, identified, sexed if obvious, and released alive.
  - Sampling schedule: 9 water bodies (6 pools P1–P6, 3 channels C1–C3) sampled in late Feb–early Mar 2018; regular monitoring at intervals of ~2 weeks at P1 and C2 until Jan 2019.
  - Site movements: P1 Bay (initial) later moved to P1 Main due to falling water levels.
  - Location and environment:
    - GPS recorded on first visit (Garmin GPSMAP 62s).
    - Measured water temperature, dissolved oxygen (% and μg/L), and conductivity (μS/cm) during visits 26 Feb 2018–25 Jan 2019.
    - Sea conductivity measured on 27 Feb 2018 for comparison; temperature measurements extended only 7 Mar 2019–22 Mar 2019.
  - Additional methods:
    - Two CEN standard survey nets (overnight at P1): monofilament nylon, ~1.5 m deep, 30 m long, 12 panels with varying bar-mesh sizes.
    - Daytime visual surveys at P1 and channels C4–C6 (26 Feb–1 Mar 2019).

- Data and metadata structure
  - Data files (CSV):
    - Akrotiri_aquatic_environment_26_2_18_22_3_19: sampling site location and environmental measurements.
    - Akrotiri_fish_26_2_18_22_3_19: all fish observations.
    - Akrotiri_traps_26_2_18_22_3_19: trap observations (some entries with zero fish).
  - Environment data (Akrotiri_aquatic_environment_26_2_18_22_3_19):
    - Columns include: Date, Time, Site_code, Site_full_name (including natural/refuge population indicator), Lat_N, Lon_E, Temp (°C), DO_per (%), DO (μg/L), Cond (μS/cm).
  - Fish observations (Akrotiri_fish_26_2_18_22_3_19):
    - Columns include: Date, Site_code, Trap_Type (SUBM or SEMI), Trap_number, Species (Aphanius fasciatus or Gambusia holbrooki), Sex (M indicated if obvious male), Length (fork length in mm).
  - Traps observations (Akrotiri_traps_26_2_18_22_3_19):
    - Columns include: Date, Site_code, Trap_Type, Trap_number, Aphanius (count), Gambusia (count), Total (sum of Aphanius and Gambusia).

- Data quality and provenance
  - Quality control/assurance: all equipment and protocols developed or led by an experienced CEH staff member (>25 years), with initial field training for local staff; data reviewed and digitised by CEH staff.
  - Missing data and gaps:
    - Missing aquatic environmental data primarily due to equipment failure after 25 Jan 2019.
    - A thermometer issue caused gaps; DO and conductivity meters generally functional, but thermometer data missing after the noted date.
    - 28 Feb 2018 data missing for P1 Main; P1 Bay was surveyed on 26 Feb 2018; given proximity to P1 Main, differences expected to be minimal.

- Practical implications for data use
  - Provides time-series environmental context (temperature, DO, conductivity) aligned with fish trap and net catches across nine water bodies, enabling analyses of species occurrence and abundance in relation to habitat conditions.
  - Rich metadata on site location, trap configuration, and survey methods facilitates data integration with similar monitoring programs.
  - Availability of both trap-based and net-based sampling, plus daytime visual surveys, supports cross-method comparisons and comprehensive fish community assessments.
  - Clear documentation of data structure and column definitions supports self-service data exploration and product creation (dashboards, pivot analyses, reports).