# Overview of data

- What this dataset is
  - A compilation of results from the stream metabolism component of the NERC Macronutrients consortium, titled “The role of lateral exchange in the seaward flux of C, N and P.”
  - Data were generated in the field by multiple researchers and accompany 39 CSV data files.

- What was measured
  - In situ flow velocity transects in rivers with varying land–river connectivity in the Hampshire Avon catchment.
  - Measurements taken with a Model 801 electromagnetic flow meter by Valeport.

- Where and when
  - Rivers/sites (site codes and locations):
    - CE1: River Ebble (Ebble) [Latitude 51.027499 N, Longitude -1.9217089 E]
    - GA2: River Avon (Avon) [51.318289, -1.8600020]
    - GN1: River Nadder (Nadder) [51.043849, -2.1118158]
    - CW2: River Wylye (Wylye) [51.142475, -2.2033140]
    - AS1 (AP): Tributary of the River Sem (AP/AS1) [51.055413, -2.1568407]
    - AS (AS2): River Sem (AS2) [51.045826, -2.1104425]
  - Campaign periods:
    - Spring 2013 (23/04–09/05/2013)
    - Summer 2013 (31/07–16/08/2013)
    - Autumn 2013 (29/10–11/11/2013)
    - Winter 2014 (28/01–09/02/2014)
  - Notes on data collection:
    - Some campaigns did not include certain sites (e.g., AP in summer; CE1 and GA2 in winter due to flooding).

- How it was measured and structured
  - For each transect, the stream was gridded:
    - 0.25 m segmentation for stream width < 3 m; 0.5 m segmentation for width > 3 m.
    - Flow measured at each grid segment in 0.1 m depth steps from the riverbed; if near-surface measurements could not be 0.1 m, 0.05 m steps used instead.
    - NaN entries indicate data not collected (e.g., between grid lines or too close to banks/surface for accurate readings).
  - File naming convention: Flow_'SiteCode'_'Season'_'Location'.CSV
  - Heightened data context:
    - Distance: meters from the stream bank.
    - Water depth: measured depth in meters at each distance from the bank.
    - Notes: vegetation, bed features, proximity to aquatic eddy co-variance (AEC) at each distance.
    - Date: line 2 indicates the measurement date (MM/DD/YYYY).
    - Depth [m]: line indicating the depth at which the flow measurements were taken.
    - Data values: subsequent lines contain the average flow in m/s over 15 seconds of continuous measurements (n=15).

- Data quality, limitations, and considerations for GIS
  - 39 data files cover multiple sites and seasons with some intentional omissions due to field conditions.
  - Depth and spacing vary by site and campaign, requiring harmonization for cross-site GIS analyses.
  - NaN values reflect missing readings due to grid alignment or near-boundary limitations.
  - The dataset provides precise spatial references (site coordinates) enabling integration into GIS workflows and spatial analyses of river flow profiles.

- Provenance and context
  - Associated with Prof. Mark Trimmer and the NERC Macronutrients project; instrument details and service history noted.
  - Raw data are intended for use in analyses of lateral exchange and seaward fluxes of nutrients, with potential visualization as map-based representations of velocity profiles along transects.