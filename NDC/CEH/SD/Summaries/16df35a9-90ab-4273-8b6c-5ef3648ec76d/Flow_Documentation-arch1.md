# Overview of data

- A dataset compiling results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, focusing on the role of lateral exchange in the seaward flux of C, N and P.
- Field data collected under the supervision of Prof. R. N. Glud and with contributions from L. Rovelli, K. M. Attard, and Assoc. Prof. H. Stahl.
- Contains 39 separate CSV files accompanying the overview, each named Flow_<SiteCode>_<Season>_<Location>.CSV (e.g., Flow_CE1_autumn_upstream.CSV).

## What the data cover

- Four field campaigns measuring in situ flow velocity transects in rivers with varying land–river connectivity in the Hampshire Avon catchment.
- Campaign periods: spring 2013 (23/04–09/05/2013), summer 2013 (31/07–16/08/2013), autumn 2013 (29/10–11/11/2013), winter 2014 (28/01–09/02/2014).
- Sites (SiteCode and location with coordinates):
  - CE1: River Ebble (51.027499 N, -1.9217089 E)
  - GA2: River Avon (51.318289 N, -1.8600020 E)
  - GN1: River Nadder (51.043849 N, -2.1118158 E)
  - CW2: River Wylye (51.142475 N, -2.2033140 E)
  - AS1 (AP): Tributary of River Sem (51.055413 N, -2.1568407 E)
  - AS: River Sem (51.045826 N, -2.1104425 E)
- Site-specific measurements include upstream vs downstream transects within each reach.

## Measurement method and instrumentation

- Instrument: Model 801 electromagnetic flow meter (Valeport, Totnes, UK); instrument details referenced via Valeport website (last access 20.09.2016).
- Sampling grid and depths:
  - Transects gridded in 0.25 m segments for stream width < 3 m; 0.5 m segments for width > 3 m.
  - Flow measured for each segment in 0.1 m depth steps starting from the riverbed; if near-surface measurements could not be 0.1 m steps, a 0.05 m step was used.
- Data points per depth: measurements correspond to average flow over 15 seconds (n = 15).
- Distance and depth metadata:
  - Distance: meters from the stream bank.
  - Water depth: depth in meters at each distance from the bank.
  - Depth: depth values (in meters) at which measurements were taken (line 2 indicates the depth; subsequent lines provide flow values).
  - Notes: contextual information on vegetation, bed features, and proximity to aquatic eddy covariance (AEC) at each distance.
- Data quality notes:
  - NaN entries indicate data not collected (e.g., gaps between grid lines or measurements too close to banks or surface for accurate readings).

## Data structure and file naming

- File naming convention: Flow_<SiteCode>_<Season>_<Location>.CSV
  - SiteCode examples: CE1 (Ebble), GA2 (Avon), GN1 (Nadder), CW2 (Wylye), AS1 (AP, Sem tributary), AS (Sem).
  - Location indicates upstream or downstream end of the studied reach.
- Each file contains:
  - A header with Distance (from bank) and Water depth readings.
  - A second line indicating Depth values (measurement depths).
  - Subsequent lines containing average flow (m/s) over 15 seconds for each depth.
  - A Date line in each set indicating measurement date (MM/DD/YYYY).

## Campaign and data coverage notes

- Notable gaps:
  - Summer 2013: AP (AS1) site data not collected due to insufficient flow.
  - Winter 2014: CE1 and GA2 not sampled due to flooding.
- The Location field specifies whether the transect point is upstream or downstream within the reach, aiding spatial interpretation.

## Provenance and data access

- Part of the NERC Macronutrients consortium project on lateral exchange and C, N, P fluxes.
- Field campaigns conducted by researchers including L. Rovelli, K. M. Attard, and Assoc. Prof. H. Stahl; project leadership by Prof. R. N. Glud; overall leadership by Prof. M. Trimmer.
- Data collection and instrument servicing coordinated with Lancaster University (Lancaster Environment Centre, Prof. Andrew Binley).
- Instrument and methodology details available via Valeport (website), with data reference last verified 2016-09-20.

## Potential analytic use and considerations

- Enables analysis of spatial flow velocity profiles across multiple rivers with varying connectivity, facilitating:
  - Comparisons of upstream vs downstream flow characteristics within reaches.
  - Seasonal comparisons across spring, summer, autumn, and winter campaigns (with caveats for missing campaigns at certain sites).
  - Integration with other measurements related to carbon, nitrogen, and phosphorus fluxes to investigate lateral exchange processes.
- Data quality considerations for analysts:
  - Gaps due to uncollected measurements (NaNs) and campaign-specific absences (e.g., summer AP, winter CE1/GA2).
  - Variable grid spacing dependent on river width requires normalisation when comparing across sites.
  - Depth lines indicate measurement depths; ensure alignment when aggregating across depths or sites.