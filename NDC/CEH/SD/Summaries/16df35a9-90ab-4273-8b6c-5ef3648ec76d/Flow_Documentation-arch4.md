# Overview of data

- Origin and purpose
  - Compilation from the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the role of lateral exchange in the seaward flux of C, N and P.
  - In-field data collected by a team including L. Rovelli, K. M. Attard, and A/Prof. H. Stahl under Prof. R. N. Glud.
  - 39 accompanying CSV data files documenting flow measurements across multiple river sites.

- Data collection and instrumentation
  - Four field campaigns conducted to measure in situ flow velocity transects in rivers with varying land–river connectivity in the Hampshire Avon catchment.
  - Instrument: Model 801 electromagnetic flow meter by Valeport; regularly serviced throughout the project.
  - Measurement grid: transects gridded to 0.25 m (width < 3 m) or 0.5 m (width > 3 m). Flow measured for each segment in 0.1 m depth steps from the riverbed; if near-surface steps could not be performed in 0.1 m, 0.05 m steps used instead.
  - Data gaps: NaN entries indicate measurements not collected (e.g., between grid lines or too near boundaries).

- File naming, structure, and site information
  - Filenames follow: Flow_'SiteCode'_'Season'_'Location'.CSV.
  - Site codes and coordinates:
    - CE1: River Ebble (51.027499°N, -1.9217089°E)
    - GA2: River Avon (51.318289°, -1.8600020°)
    - GN1: River Nadder (51.043849°, -2.1118158°)
    - CW2: River Wylye (51.142475°, -2.2033140°)
    - AS1 (AP): tributary of River Sem (51.055413°, -2.1568407°)
    - AS (Sem): River Sem (51.045826°, -2.1104425°)
  - Campaign seasons: Spring 2013 (23/04–09/05/2013), Summer 2013 (31/07–16/08/2013), Autumn 2013 (29/10–11/11/2013), Winter 2014 (28/01–09/02/2014).
  - Data gaps by site/season:
    - AP not measured in summer due to insufficient flow.
    - CE1 and GA2 not measured in winter due to flooding.
  - Location field indicates upstream or downstream position within the studied reach.

- Data content and metadata
  - Column headers (at minimum): Distance (m from stream bank), Water depth (m), Notes (vegetation, bed features, proximity to aquatic eddy covariance at each distance).
  - A second line provides the depth values (in meters) at which flow measurements were taken.
  - Subsequent lines contain the average flow values (m/s) over 15 seconds of continuous measurements (n = 15) for each segment.
  - Notes field contains contextual information (e.g., vegetation, bed features, AEC proximity).

- Temporal and spatial coverage
  - Spanning four seasonal campaigns across multiple river sites within the Hampshire Avon catchment.
  - Provides spatially resolved velocity profiles along transects at each site and season.

- Data quality, limitations, and governance considerations
  - Fragmented data across sites, seasons, and sometimes missing measurements (NaNs) due to boundary proximity or grid placement.
  - Some sites had incomplete campaigns due to environmental conditions (e.g., flooding, insufficient flow).
  - Metadata includes instrument details and measurement protocols, aiding reproducibility and reuse.
  - For discovery and reuse, data are organized by site, season, and transect location, with explicit coordinates and measurement depth context.