# Overview of data

- What the dataset is
  - A compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the role of lateral exchange in the seaward flux of carbon, nitrogen, and phosphorus.
  - Field data collected by Dr. L. Rovelli, Dr. K. M. Attard, and Assoc. Prof. H. Stahl under Prof. R. N. Glud; four field campaigns produced in situ flow-velocity transects across Hampshire Avon catchment.
  - 39 accompanying CSV data files (e.g., Flow_AP_autumn_upstream.CSV, Flow_GA2_summer_downstream.CSV, etc.).

- Dataset scope and sites
  - Rivers with varying land-river connectivity in the Hampshire Avon catchment.
  - Site codes and coordinates:
    - CE1: River Ebble (51.027499 N, -1.9217089 E)
    - GA2: River Avon (51.318289, -1.8600020)
    - GN1: River Nadder (51.043849, -2.1118158)
    - CW2: River Wylye (51.142475, -2.2033140)
    - AS1 (AP): tributary of River Sem (51.055413, -2.1568407)
    - AS (AS2): River Sem (51.045826, -2.1104425)

- Field methodology
  - Instrument: Model 801 electromagnetic flow meter (Valeport, UK). Instrument serviced at Lancaster University during the project.
  - Transect/grid setup: For each transect, river was gridded:
    - 0.25 m spacing if stream width < 3 m
    - 0.5 m spacing if width > 3 m
  - Depth measurements: Flow measured at each grid segment in 0.1 m depth steps from the riverbed; if near-surface readings could not be taken at 0.1 m steps, 0.05 m steps were used.
  - Data gaps: Columns marked NaN indicate data not collected (e.g., between grid lines, too close to banks or surface for accurate readings).

- Data structure and naming
  - File naming convention: Flow_'SiteCode'_'Season'_'Location'.CSV
  - Location indicates upstream or downstream end of the reach.
  - Data columns:
    - Distance: distance in meters from stream bank
    - Water depth: measured depth in meters at each distance from the bank
    - Depth [m]: depth(s) at which flow measurements were taken (variable by site/campaign)
    - Notes: additional information on vegetation, streambed features, proximity to aquatic eddy covariance (AEC)
  - Measurement data: subsequent lines provide the average flow in meters per second (m/s) over 15 seconds of continuous measurements (n=15)
  - Date line: format MM/DD/YYYY indicating when measurements were taken

- Campaign details and data coverage
  - Campaign seasons and years:
    - Spring 2013 (04/23–05/09/2013)
    - Summer 2013 (07/31–08/16/2013)
    - Autumn 2013 (10/29–11/11/2013)
    - Winter 2014 (01/28–02/09/2014)
  - Data collection notes:
    - AP (AS1) had no measurements in summer due to insufficient flow
    - CE1 and GA2 had no measurements in winter due to flooding

- Provenance and access
  - Data produced as part of the environmental monitoring and analysis for understanding lateral nutrient fluxes in river systems.
  - Instrument and data collection details referenced with external sources (Valeport product page; data last accessed date 20.09.2016).