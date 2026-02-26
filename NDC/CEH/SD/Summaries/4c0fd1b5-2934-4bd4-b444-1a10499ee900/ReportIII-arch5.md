# REPORT III RESULTS FROM THE SOURHOPE FIELD EXPERIMENT: 1999-2001

- Purpose and scope
  - Large-scale field experiment under the NERC Soil Biodiversity Thematic Programme at Sourhope (Scottish Borders) to monitor context for focused studies and facilitate year-to-year comparisons.
  - Site described in Baseline Data Survey (Nov 1998); ongoing monitoring across 1999–2001 to link with other datasets.
  - Management and data collection were impacted in 2001 by Foot and Mouth Disease (FMD) restrictions and a change of site officer.

- Datasets and measurements (types and timing)
  - Automatic Weather Station (1999–2001)
    - Headline measures: rainfall, radiation, average temperatures, soil moisture at multiple depths; data regularly downloaded and transmitted.
    - 2001: rainfall near long-term average; slight reductions in temperature; higher soil moisture vs prior years.
  - Above-ground biomass (1999–2001)
    - Five mowing occasions each summer; 0.5 m2 sampling cells within sub-plots; biomass dried and summed for annual totals.
    - Treatments: Control 1/2; Nitrogen (N); Lime (L); Nitrogen + Lime (N&L); Biocide; Biomass response highest with Nitrogen and Lime; 2001 shows notable biomass increase vs 2000, partly due to personnel changes and switch to mechanical cutting.
    - Data processed via log-transformation and split-plot ANOVA; significant treatment-year interactions; no block effects.
  - Soil pH (upper 5 cm)
    - Baseline in August 1998; October 2001 shows liming raised pH to 6.19 (C1) and 6.38 (N&L); Nitrogen alone also raised pH but less so; control unchanged.
  - Botanical composition (Point Analysis, July 2001)
    - 100-point quadrat frame with 25 marked touches per plot; two surveyors swapped responsibilities with no significant inter-surveyor difference.
    - 2001: 58% more hits than 2000; shifts in dominance among species by treatment (e.g., Festuca spp. more abundant in fertilized plots; Agrostis capillaris declined across treatments).
    - Diversity: unimproved plots: 24 species; improved plots (N and/or L) fewer (18 species), suggesting diversity changes with fertility.
    - Multivariate analysis (PCA) showed clear separation of nitrogen and/or lime plots from control/biocide plots.
    - Biomass correlations: Festuca rubra and Poa pratensis positively linked to biomass; Anthoxanthum odoratum and Nardus stricta decline as biomass increases.
    - Noted increase in litter in plots receiving nitrogen and/or lime, indicating faster vegetation turnover with higher fertility.

- Experimental design and management context
  - Field layout included blocks, plots, sub-plots (S, T, U, V) with multiple treatments and controls.
  - 2001 disruptions: FMD restrictions curtailed site access (Feb–May 2001); one biocide application initially missed in May; subsequent biocide applications completed.
  - Change of site officer in May 2001; data collection continued under an updated protocol and vet supervision.

- Site heterogeneity and spatial patterns
  - Spatial heterogeneity observed: columns E and F showed more acidic plots, likely due to column-level treatment/ownership patterns.
  - Biomass tended to be higher in centrally located plots; strong positive correlation between surface soil pH and biomass.
  - No significant differences between blocks in biomass, but notable variation across site columns and plots.

- Data quality, provenance, and processing notes
  - Consistent data collection across surveyors in 2001; inter-surveyor agreement supported by statistical test (no significant difference).
  - Methodological note: transition from manual cutting to mechanical shears in 2001 impacting biomass measurements; analyses normalized to C1 to interpret treatment effects across years.
  - Data management: weather data managed by MLURI data manager; measurement schedules and dates are documented (Table 1; Figure/Table references).
  - Analyses used: Genstat 5 (ANOVA, PCA), log transformations for biomass, and cross-year comparisons (1999–2001).

- Data governance implications and recommendations for Data Stewards
  - Metadata and data dictionaries
    - Capture: site location, farm management, plot/block/sub-plot coding, treatment definitions (C1, C2, N, L, N&L, B), measurement dates, and methods (including the 2001 switch to mechanical cutting).
    - Include species codes with full taxonomic references (e.g., Ac = Agrostis capillaris; Fr = Festuca rubra; etc.) and provide a master mapping.
  - Provenance and versioning
    - Maintain versioned datasets for each data type (weather, biomass, soil pH, botanical surveys) with audit trails of management events (FMD restrictions, officer change) and protocol changes.
  - data quality assurance
    - Document QA tests (e.g., inter-surveyor comparison, method changes, outliers, normalization procedures).
    - Preserve raw vs processed data; clearly annotate transformations (e.g., ln-transforms used for biomass analyses).
  - Data interoperability and discoverability
    - Standardize units and measurement protocols; supply a data dictionary and a data description for archiving in a portal.
    - Ensure linkage across data types (plots, treatments, time points) to enable cross-study reuse and meta-analyses.
  - Accessibility and data sharing
    - Provide clear notes on data gaps due to FMD restrictions (Feb–May 2001) and other disruptions; include this in dataset documentation for users.
  - Usability for future reuse
    - Include interpretation aids: summaries of major findings by data type, guidance on comparing year-to-year trends, and cautions about methodological changes when comparing 1999–2000 with 2001.

- Key takeaways for reuse
  - Fertilizer and liming (N and/or L) consistently increased above-ground biomass and soil pH; 2001 biomass increase likely influenced by personnel changes and a switch to mechanical cutting.
  - Botanical communities shifted with treatment, showing reduced dominance by Agrostis capillaris and greater presence of Festuca spp. and Poa pratensis in fertilized plots; minor losses in overall species richness in the most improved plots.
  - Site heterogeneity is substantial and influential; biomass correlates positively with pH and central-site location, underscoring the need for careful spatial metadata in analyses.
  - FMD-related disruptions and protocol changes in 2001 are important context for cross-year comparisons and should be documented in any data package for future users.