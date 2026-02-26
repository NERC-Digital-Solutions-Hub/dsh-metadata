# Impacts of experimental drought and plant trait diversity on floral resources and pollinator visitation.

- Overview
  - A field experiment in Wiltshire, UK (Winklebury Hill) to test how plant functional diversity and drought affect floral resources and pollinator visitation.
  - Focus on floral resources (flower numbers, diversity, nectar presence/amount/quality) and pollinator visits to experimental plots.
  - Data collected as part of the Winklebury Hill experiment (2013–2016), with links to Fry et al. 2017, 2018.

- Study design and spatial layout
  - Field site: ex-arable calcareous grassland on chalk; coordinates 50.991207° N, -2.069834° W.
  - Plot Layout: 8 m × 8 m plots arranged in a grid (7 across × 6 down) with 2 m gaps, total of 24 plots.
  - Plant communities: 7 combinations across three functional groups (FG1, FG2, FG3), implemented in each plot and replicated across blocks.
  - Subplots and treatments: Each plot contains three subplots (1 m × 1.5 m) with treatments:
    - Drought (D) – rain excluded with shelters for six weeks.
    - Control (C) – ambient rainfall.
    - Roofed control (R) – transparent roof with 5 cm holes to mimic roof effects while allowing rain.
  - Experimental blocks and replication: Six blocks, randomized allocation to control for spatial effects; includes multiple FG combinations per block.
  - Temporal aspect: Drought periods implemented in 2015 and 2016; shelters operated from early June to mid-July, simulating a once-in-100-years drought.

- Data collected and variables
  - Floral resources (NERCPropNectar.csv and NERCNectar.csv)
    - Nectar measurements on three focal species (Lathyrus pratensis, Onobrychis viciifolia, Prunella vulgaris).
    - Metrics: presence/absence of nectar, nectar volume per raceme/flower, nectar sugar concentration (converted to equivalent mg/μl), and total sugar produced per flower over 24 h.
    - Sampling: racemes randomly selected, covered for 24 h to measure standing crop and accumulation; nectar volumes and concentrations measured with microcapillaries and refractometry.
    - Linking fields: Raceme_ID, Plot_ID, Subplot_ID used to connect with other datasets.
  - Floral surveys (NERCFloralSurveys.csv)
    - Floral species identification within 1 m^2 quadrats per subplot; counts of floral units per species.
    - Functional group (FG) and FG_Diversity (1–3) per plot; survey dates; Subplot_Type and SubplotID; SurveyID.
  - Pollinator visits (NERCPollinatorSurveys.csv)
    - 10-minute pollinator surveys in each 1 m^2 quadrat; record visits by flower visitor, plant species visited, and number of floral units visited.
    - Data include Survey_ID, Plot_ID, Subplot_ID, FG/Diversity, date, Subplot_Type, and No_Visits per species.
  - Data integration
    - Datasets linked via Plot_ID, SubplotID, RacemeID, and SurveyID to allow cross-dataset joins (e.g., linking nectar with floral and pollinator data).

- Site and environmental context
  - Soil moisture: measured after drought period; results showed lower soil moisture in drought plots (approx. control 33.05 ± 0.50, roofed control 31.09 ± 0.77, drought 23.55 ± 0.93).
  - Weather and drought modeling: drought periods lasted six weeks, modeled as a 1-in-100-year event using a Gumbel distribution based on 2004–2014 rainfall data from Yeovilton (Yeovilton Weather Station).

- Data quality, ethics, and metadata
  - Protocols followed for field data; data stored in MS Access with checks for anomalies.
  - Ethics approval: CLES Penryn Research Ethics Committee (2016/1429).
  - Missing data noted in metadata (e.g., some concentration values missing; one pollinator subplot had a survey gap due to observer error).
  - Files and metadata:
    - NERCPropNectar.csv: nectar presence and counts related to plots/subplots.
    - NERCNectar.csv: nectar volume, concentration, and derived sugar metrics; concentration data with some missing values.
    - NERCFloralSurveys.csv: floral unit counts by species, FG, and survey details.
    - NERCPollinatorSurveys.csv: pollinator visits with per-species visit counts and survey metadata.
  - Linking fields: PlotID, RacemeID, SubplotID, and SurveyID are consistent across datasets to enable integration; PlotID can be used to reference Fry et al. 2017/2018.

- Practical GIS and data-product implications
  - Enables map-based visualization of how drought and plant trait diversity affect nectar resources and pollinator visitation across a spatial grid of plots.
  - Supports spatial analyses of treatment effects by FG diversity, plot location, and time (survey rounds).
  - Provides a structured dataset with robust linking keys for combining ecological metrics (nectar, floral abundance, pollinator visits) in map-based dashboards or GIS analyses.
  - Coordinates and site-level context (Wiltshire location, drought shelter implementation, soil moisture outcomes) enhance spatial interpretation and replication potential.

- References and provenance
  - Foundational methods and protocols cited (Baldock et al. 2015; Corbet 2003; Pollard & Yates 1993; Prŷs-Jones & Corbet 1991; Rodwell 1992; Yee 2010).
  - Related datasets and publications: Fry et al. 2017, 2018 (Ecosystem functions and vegetation data, Winklebury Hill); data centre links provided.