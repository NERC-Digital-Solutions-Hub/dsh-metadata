# Background information

- Countryside Survey (CS) is a long-running audit of the UK countryside, conducted at regular intervals since 1978, enabling comparison across surveys to detect gradual environmental changes.
- The CS has moved to a rolling monitoring program (UKCEH-CS) starting in 2019, with a five-year cycle visiting ~500 1km squares to track soil, vegetation, and broader landscape features on multiple scales.
- The program aims to capture ecosystem-level data and trends, integrating multiple metrics (soil, vegetation, headwater streams, habitats, landscape features) to understand the size, location, causes, and consequences of change.

- Since 2019–2023, the rolling program focused on soil and vegetation data from five plots per 1km square. From 2024, additional plots along linear features are added where appropriate: 1 boundary plot, 1 roadside plot, 1 streamside plot, and 1 hedgerow plot (dominant species recorded in England). These plots are also sampled for soil using methods aligned with adjacent field plots.

- The sample framework: 500 x 1km squares randomly selected per five-year cycle, stratified by the ITE Merlewood Land Classification of Great Britain. Approximately 100 squares are visited each year.

- Exclusion criteria: any selected square with more than 75% urban land or more than 90% sea area is excluded.

- Sample selection lineage: the 1978 squares (256) remain in the rolling program for the longest time series; additional squares from 1990 are included to extend coverage.

- First cycle began in 2019; 2024 marks the first year of the second cycle.

- The design enables robust national and subnational indicators for GB and its countries, with data collected to support policy-relevant analyses and reporting.

- Data collection is performed by trained field surveyors using standard protocols (Smart et al., 2024), with intensive pre-surveys, team supervision, and ongoing quality control. About 10% of plots are re-surveyed for quality assurance, performed by the same assessor since 1990 to ensure consistency and accurate validation of plot locations and habitat classifications.

- Data products for 2024 include vegetation data in two CSV files:
  - UKCEHCS_VEGETATION_PLOTS_2024.csv: plot-level information (location, plot type, plot ID, land classification, environmental zone, country, county, habitat data, and plot-specific measurements such as trees and canopy/shrub heights).
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2024.csv: species list per plot (species identifiers, names, nest-related data for larger plots, cover metrics, and total plot cover).

- Plot types and relevant fields:
  - Plot types: B (boundary), H (hedgerow), R (roadside), S (streamside).
  - Each plot has identifiers (SQUARE_ID, PLOT_ID), plot type, and site descriptors (land classification, environmental zone, country, county).
  - Additional fields capture vegetation structure (trees, canopy/shrub heights), and plot-specific contextual data (boundary features, road type, stream attributes, hedgerow characteristics).

- Data integration and references:
  - The CS design integrates with the Land Classification of Great Britain (ITE) and related habitat classifications (JNCC broad and priority habitats).
  - The dataset and methodologies reference the Countryside Survey field handbook (2024–2029) and related historical literature on land classification, habitat classifications, and UK biodiversity actions.

- Purpose and outputs for Analysts:
  - Produce national and subnational indicators of environmental condition and change for policy assessment.
  - Deliver outputs in clear formats (reports, maps, charts) and ensure datasets are stored and uploaded to appropriate data portals for broader access.
  - The rolling design buffers against year-to-year climate variability, enabling more stable trend detection and year-on-year change analysis.

- Key challenges and opportunities for data use:
  - Increasing the value of monitoring datasets by combining CS data with other relevant datasets (avoiding single-use analyses).
  - Ensuring accessible underlying data and metadata to support reuse by researchers, policymakers, and other stakeholders.