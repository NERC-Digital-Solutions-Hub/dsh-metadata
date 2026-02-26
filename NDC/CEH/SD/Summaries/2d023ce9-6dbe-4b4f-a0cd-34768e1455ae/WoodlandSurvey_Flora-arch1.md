# Woodlands Survey flora data 1971-2001

- Overview
  - In 1971, 103 broadleaved woodlands across Britain were surveyed.
  - Data collected at site level and in 16 randomly placed 200 m² plots per site.
  - Field measurements included plant species composition (canopy and ground flora), soil pH, soil organic matter, habitat management, and a wide range of other plot- and site-level descriptors.
  - Sites and, where possible, plots were revisited in 2000, 2002, and 2003 (referred to as 2001) using identical methods.
  - Analyses aimed to identify ecological changes over time and drivers of change, using both survey data and external datasets; key drivers explored include atmospheric deposition of sulfur and nitrogen, climate, canopy changes, and woodland management.
  - Foundational publications (2004–2005) detail methods and spatial drivers; users should consult these for field methods and analytical results.

- Survey design & methods
  - Stratified sampling across the surveyed area.
  - Followed Bunce & Shaw’s 1973 standardized survey methods.
  - Field handbook provided to support data collection.

- Related datasets
  - Countryside Survey (external dataset reference).
  - Steele (1968) National survey of woodlands (reprinted in related handbook form).

- Originator details
  - 1971: R.G.H. Bunce & M.W. Shaw, Woodland Ecology Section, Nature Conservancy Merlewood (initial surveys).
  - 2001–2003: Simon Smart, Helaina Black (CEH Lancaster); Keith Kirby (English Nature); Phil Corney (Applied Vegetation Dynamics Laboratory, University of Liverpool).

- Data structure
  - Site: Numeric code (1–103) identifying each woodland site.
  - Plot: Numeric (1–16) identifying 16 plots per site.
  - BRC_number: Numeric code for species (per Biological Record Centre list).
  - BRC_names: Text, scientific name corresponding to BRC_number.
  - Amalgams: Numeric codes grouping selected species into cross-specific taxa due to recording inconsistencies (e.g., Viola riviniana/reichenbachiana; Cardamine hirsuta/flexuosa).
  - Amalgam_names: Text, scientific names for amalgam groups.
  - NEST: Numeric, indicates that an inner 2x2 m nest estimate applies (not always consistently filled; often used to indicate a plot-wide estimate).
  - COV: Numeric, percentage cover for the whole plot. 0.5 means <1% cover; -1 indicates bare ground/litter/wood/rock/total bryophyte/water; nulls relate to woody species recorded as individuals (not cover).
  - YR: Numeric, year of survey (1971, 2000 pilot sites, 2002, 2003).
  - Yr_2: Numeric year code (yr 1 = 1971; yr 2 = 2000/2002/2003).
  - Bryo: Text, indicating bryophyte status (b = bryophyte; l = lichen).
  - Woody: Text, indicating woody status (w = woody species).
  - Field_sheet: Text, field sheet on which original data was recorded (e.g., 'Ground flora' plot data).

- References (selected)
  - Avery, B. W. (1973). Soil Classification in the Soil Survey of England and Wales.
  - Corney, P.M. et al. (2004). The effect of landscapescale environmental drivers on the vegetation composition of British woodlands. Biological Conservation.
  - Haines-Young, R.H. et al. (2003). Changing landscapes, habitats and vegetation diversity across Great Britain. Journal of Environmental Management.
  - Kirby, K.J. et al. (2005). Measuring Long Term Ecological Change in British woodlands (1971-2001): A re-survey and analysis of change based on the 103 sites in the Bunce 1971 woodland survey. English Nature Research Reports.

- How this data supports analysis
  - Enables long-term assessment of woodland flora, soil properties, and habitat characteristics across 103 sites with repeated measures.
  - Facilitates modeling of ecological change drivers by combining internal plot/site variables with external data (deposition, climate, canopy changes, management).
  - Supports identification of statistically significant patterns of change at site and plot scales.
  - Provides standardized methods and a clear data dictionary (fields and codes) to ensure reproducibility and comparability across years.

- Practical considerations for analysts
  - Data includes amalgamated taxa to address inconsistent recording, which requires careful interpretation or disaggregation where possible.
  - Some fields (e.g., NEST, COV) may have inconsistent or missing values; cross-check with field handbook and referenced publications.
  - Changes in recording practices over time (1971 vs. 2000/2002/2003) should be accounted for in longitudinal analyses.