# Seasonal abundance of Culex pipiens at CEH Wallingford (2015)

- Overview
  - Dataset details the seasonal abundance of Culex pipiens across life stages (eggs, larvae, pupae, and adults) at the Centre for Ecology & Hydrology (CEH) Wallingford field site in 2015.
  - Immature stages were monitored March–October 2015; adults were sampled April–October 2015.
  - Data are organized to support analysis of spatial (butt/trap) and temporal (sampling date) patterns, and to enable self-serve exploration of mosquito dynamics.

- Experimental design and data collection
  - Immature sampling
    - Four 450 L circular water butts located close together with varying exposure to sun and vegetation.
    - Butts were prepared with hay infusion (January–March) and equipped with HOBO surface water temperature loggers recording hourly.
    - Eggs counted as egg rafts at 10 am on Mon/Wed/Fri.
    - A 500 ml dip sample was collected from the north, south, east, and west edges of each butt; dips from the middle were avoided due to edge concentrations of larvae/pupae.
    - Counts of 1st/2nd instar and 3rd/4th instar larvae and pupae were done in the field when feasible; otherwise photographs were taken and counted on a computer.
    - Monthly sampling included removing 20 fourth instar larvae per butt for morphological identification to species level (Becker et al., 2003) via microscopy; larvae were killed by boiling water before examination.
  - Adult sampling
    - Four John W. Hock Miniature Downdraft Blacklight (UV) traps baited with dry ice operated nightly from Apr 14 to Oct 2 (5 consecutive empty collections triggered cessation), located at two tree-line locations and near the butts.
    - Traps run 1700–0900; adult females identified to species in the lab; males not recorded.
    - Data include counts of adult female Cx. pipiens and other species identified.

- Fieldwork and laboratory instrumentation
  - UV light traps used for adult sampling; specimens identified in the laboratory using standard dissection and light microscopy techniques.

- Nature and units of recorded values
  - Egg abundance: counts of egg rafts per butt.
  - Larval and pupal abundance: counts per sampling occasion, split by butt and life stage (larvae vs. pupae; instar stages L1/2 and L3/4).
  - Adult abundance: number of adult female Cx. pipiens (and other species) per trap per sampling occasion.
  - Temperature: surface water temperature in degrees Celsius (hourly measurements per butt).

- Quality control
  - Counting validation by comparing counts from photographs with direct counts on the first two days; results were consistent, supporting the use of photo-based counting for larger samples.

- Details of data structure
  - Six CSV files:
    - Egg_abundance_2015_Wallingford.csv: date, butt number, egg raft counts.
    - Larval_abundance_2015_Wallingford.csv: date, quadrant-oriented columns per butt (N, E, S, W) with L1/2 and L3/4 larval counts.
    - Pupal_abundance_2015_Wallingford.csv: date, butt-specific pupal counts (structured similarly to larval data).
    - Adult_abundance_2015_Wallingford.csv: date, trap location, counts of adult female Cx. pipiens and other species; NA indicates missing data due to issues.
    - Larval_identification_2015_Wallingford.csv: dates and numbers of 4th instar larvae identified, species assignments (Cx. pipiens and others), and butt origin.
    - Water_temperatures_2015_Wallingford.csv: date, time, butt, and corresponding surface water temperature.
  - Each file is organized to enable per-site (butt/trap) and per-date analyses, with clear separation between immature and adult data streams and accompanying temperature data.

- Considerations for data support and reuse
  - Data are suitable for time-series analyses, cross-site or butt-based comparisons, and associations between temperature and mosquito abundance.
  - Some gaps exist (e.g., NA entries in adult trap data due to staff or dry ice delivery issues) that should be accounted for during analysis.
  - The dataset supports building dashboards or self-serve analyses that visualize seasonal dynamics, stage-specific abundances, and environmental correlates.