# FADOE_pollution.csv

## Overview
- Dataset of air pollutant concentrations collected in the Free-Air Diesel and Ozone Enrichment (FADOE) experiment.
- Measures NOx, NO, NO2, and O3 at the centre of eight 8 m-diameter rings under four treatments, plus surrounding wind data.
- Time-resolved data (sampling every 60 seconds) across 2018 and 2019 in a field of wheat near London.

## Experimental design and data collection
- Eight rings arranged with two rings per treatment (D = diesel exhaust, O3 = ozone, D+O3 = diesel exhaust + ozone, CON = natural air control).
- Treatments: D, O3, D+O3, CON; each with two rings.
- Pollutants measured at ring centers every 60 seconds using:
  - O3 analyzer: Model 49i (Thermo Scientific)
  - NOx analyzer: Model 42C (Thermo Scientific)
- Gases tracked: Nitrogen oxide (NO), nitrogen dioxide (NO2), nitrogen oxide (NOx), and ozone (O3) in ppb.
- Wind data collected from four directions around the field:
  - South: ws1/wd1 (Columns F/K)
  - West: ws2/wd2 (Columns G/L)
  - North: ws3/wd3 (Columns H/M)
  - East: ws4/wd4 (Columns I/N)
- Time references: Year (A), Date (B), Time (C)
- Field context: wheat field; coordinates provided (2018: ~51.482853, -0.897749; 2019: ~51.482374, -0.895855)

## Variables and data structure
- Pollutants (ppb):
  - NOx (Column S)
  - NO (Column Q)
  - NO2 (Column R)
  - O3 (Column P)
- Treatment (Column E): D, O3, D+O3, CON
- Time: Year (A), Date (B), Time (C)
- Wind (direction and speed):
  - South: ws1, wd1 (Columns F, K)
  - West: ws2, wd2 (Columns G, L)
  - North: ws3, wd3 (Columns H, M)
  - East: ws4, wd4 (Columns I, N)
- Instrumentation:
  - O3 analyzer: Model 49i
  - NOx analyzer: Model 42C
- Location context: annual coordinates provided for 2018 and 2019

## Temporal and spatial context
- Temporal resolution: 60-second sampling interval for gas concentrations.
- Spatial context: measurements taken at centers of eight rings arranged around a field, with wind and location data captured to assess dispersion patterns.

## Data quality and cleaning considerations
- Possible incomplete data across rings or treatments; assess for missing timestamps or sensor outages.
- Ensure unit consistency (ppb) across all pollutant variables.
- Align time stamps across gas data and wind data; handle any drift or synchronization issues.
- Consider data gaps when aggregating (e.g., per-minute to per-hour summaries).

## Potential analyses and outputs for end users
- By-treatment comparisons of pollutant levels (D, O3, D+O3, CON) over time.
- Temporal trends and peak exposure analysis for NOx, NO, NO2, and O3.
- Dispersion analysis by wind direction/speed to understand transport effects.
- Summary statistics (mean, median, max, variance) per treatment and per ring.
- Dashboards and self-serve reports linking gas concentrations to wind conditions.
- Exportable charts and tables for stakeholder communication and policy discussion.

## Data reuse and integration notes
- Ideal for combining with external meteorological datasets to model pollutant dispersion.
- Normalize across rings and years to enable cross-treatment comparisons.
- Create pivotable views (e.g., pollutant by time of day, by wind direction) and derive exposure metrics.
- Metadata and column mappings should be preserved when loading into analysis tools to maintain traceability.