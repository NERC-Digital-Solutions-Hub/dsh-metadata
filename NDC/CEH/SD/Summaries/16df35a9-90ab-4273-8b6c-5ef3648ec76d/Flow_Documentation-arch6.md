# Overview of data

- A compilation of results from the stream metabolism component of the NERC Macronutrients consortium, focusing on the role of lateral exchange in the seaward flux of C, N and P, led by Prof. Mark Trimmer (Queen Mary University of London).
- Contains 39 accompanying CSV data files from four field campaigns across Hampshire Avon catchment using in situ flow measurements.

## Data files and structure

- File naming: Flow_'SiteCode'_'Season'_'Location'.CSV (e.g., Flow_CE1_autumn_upstream.CSV).
- Site codes and locations:
  - CE1: River Ebble (51.027499 N, -1.9217089 E)
  - GA2: River Avon (51.318289, -1.8600020)
  - GN1: River Nadder (51.043849, -2.1118158)
  - CW2: River Wylye (51.142475, -2.2033140)
  - AS1 (aka AP): tributary of River Sem (51.055413, -2.1568407)
  - AS: River Sem (AS2) (51.045826, -2.1104425)
- Campaign seasons: Spring 2013, Summer 2013, Autumn 2013, Winter 2014.
- Data gaps: Some campaigns not conducted at certain sites (e.g., AP in summer; CE1 and GA2 in winter due to flooding).

## Field campaigns and sites

- Four campaigns:
  - Spring 2013 (23/04 – 09/05/2013)
  - Summer 2013 (31/07 – 16/08/2013)
  - Autumn 2013 (29/10 – 11/11/2013)
  - Winter 2014 (28/01 – 09/02/2014)
- Location indicates upstream or downstream reach position.
- Data not collected at AP in summer 2013; CE1 and GA2 not collected in winter 2014 due to flooding.

## Measurement methodology

- Instrument: Model 801 electromagnetic flow meter by Valeport; regularly serviced at Lancaster University.
- Transect grid: 0.25 m spacing (streams < 3 m wide) or 0.5 m spacing (width > 3 m).
- Depth sampling: measurements at 0.1 m depth steps from riverbed; if near-surface 0.1 m steps not possible, 0.05 m steps used.
- Data date references: each line begins with the date in MM/DD/YYYY; subsequent lines contain measurements.
- Data values: average flow in m/s over 15 seconds (n = 15) per grid segment.

## Data fields and metadata

- Distance: meters from the stream bank (0 at bank inward).
- Water depth: meters at each distance from bank.
- Depth: depth levels (in meters) at which flow was measured (varies by site/campaign).
- Notes: contextual information (vegetation, streambed features, proximity to aquatic eddy covariance, AEC).
- NaN values: indicate data not collected due to grid alignment issues or proximity to boundaries (banks or surface).

## Data quality and usage notes

- Data are patchy and distributed across multiple sites and seasons.
- Measurements are grid-based with explicit depth stepping; surface or near-boundary readings may be missing.
- Useful for cross-site, multi-season analysis of flow velocity profiles and their relation to stream morphology and ecodynamics.
- Metadata provides coordinates, site context, and campaign timing to support data integration and reproducibility.

## Access and references

- Instrument details and data provenance linked to Valeport current meters (URL provided in dataset).
- Study leadership and data origin credited to Prof. Mark Trimmer and collaborators (Queen Mary University of London).