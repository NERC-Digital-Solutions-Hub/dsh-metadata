# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2014 - 2017)

## Purpose and policy relevance
- Data originate from Ballynahone Bog to assess potential ammonia (NH3) impacts on an ammonia-sensitive peatland, informing local environmental monitoring and policy decisions.
- Site managed locally by Ulster Wildlife Trust (UWT); analysis conducted by Centre for Ecology and Hydrology (CEH) Edinburgh.
- Study location forms a transect through Ballynahone National Park, an ASSI/SAC and a Ramsar site in Northern Ireland.

## Monitoring approach and methods
- Sampler type: CEH ALPHA® passive samplers with citric acid-coated filters; PTFE membrane protects the filter; deployed with the membrane facing downwards.
- Deployment: replicates attached to a shelter on a pole at about 1.5 m above ground; monthly exposure cycle at the start of each month.
- Analysis workflow: exposed samplers are extracted into deionised water and analyzed with AMFIA (Ammonia Flow Injection Analysis) to determine NH3 concentration via conductivity.
- Concentration calculation: convert sampler results to ambient air concentration using a known uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data management: raw data flagged for quality concerns (e.g., incorrect exposure, weather-related losses); data flagged accordingly.

## Data quality assurance and quality control (QA/QC)
- Replicate reliability: coefficient of variation across replicates must be under 15%; replicates exceeding 15% are evaluated for possible discards; representative averages are retained and flagged as valid (103).
- Missing data: missing samplers assigned -9999.00 and marked invalid (-1).
- Exposure duration: samplers exposed longer or shorter than the usual monthly cycle are flagged.
- Local contamination or influences: operator notes used to identify potential non-representative samples; such results may be discarded; final site data represent the average of remaining valid results.
- Final dataset: UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv containing accepted values with appropriate flags; data structured by monthly measurements per site.

## Data structure and metadata
- Dataset composition: each row corresponds to one month of data for a single site; key fields include site name, unique site identifier, network_id (UWT), parameter_id (alpha_NH3_g), exposure start/end dates and times, measured NH3 concentration (µg NH3 m-3), detection/limit flags, verification status, unit id (µg NH3 m-3), data capture percentage, validity, and EMEP status code.
- Data quality flags: extensive use of EMEP-related flags and a data status system to document verification, data issues, and validity.
- Site information: eight sites (Ballynahone bog_1 to bog_8) with start date 01/09/2014 and ongoing end date; coordinates and 1.5 m air-inlet height are provided.

## Data governance, sharing and barriers (relevant to monitoring frameworks)
- Emphasis on sharing underlying data and ensuring transparency of metadata; potential barriers include incomplete metadata and data-sharing constraints.
- Data governance considerations include ensuring data are quality assured, stored, shared, and kept up to date; standardized reporting (reports, charts, dashboards) to communicate findings clearly.
- Data standardization (including repetition, flags, and EMEP codes) supports cross-site comparability and integration into broader monitoring frameworks.

## Site information and transect details
- Ballynahone bog_1 through Ballynahone bog_8: start 01/09/2014, End = ongoing; geographic coordinates provided; air-inlet height 1.5 m.
- Transect approach supports spatial assessment of NH3: facilitating interpretation of emissions impacts along a managed peatland ecosystem.

## Key takeaways for monitoring framework authors
- Demonstrates integration of field sampling, laboratory analysis, and standardized data processing within a single monitoring framework.
- Highlights the importance of replicates, explicit QC criteria, and detailed metadata to support data verifiability and reuse.
- Illustrates practical data governance challenges, including data sharing, metadata completeness, and timely access to datasets.
- Provides a structured dataset and flagging scheme (including CV-based validity, duration flags, local contamination indicators, and EMEP/status codes) that can inform similar monitoring frameworks and data quality pipelines.