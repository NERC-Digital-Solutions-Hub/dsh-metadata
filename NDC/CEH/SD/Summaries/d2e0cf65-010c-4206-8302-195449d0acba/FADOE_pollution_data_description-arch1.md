# FADOE_pollution.csv

## Overview
- Data from eight 8 m-diameter Free-Air Diesel and Ozone Enrichment (FADOE) rings, with two rings per treatment across four treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and a control (CON; natural air).
- Pollutant concentrations measured at the centre of each ring: NOx (NOx), NO, NO2, and O3.
- Measurements collected sequentially every 60 seconds using an automated switching system linked to:
  - O3 analyzer (Model 49i, Thermo Scientific)
  - NOx analyzer (Model 42C, Thermo Scientific)
- Field conditions recorded around the rings via wind speed and direction from four surrounding positions (south, west, north, east).

## Experimental Design
- Eight rings total; two rings per treatment, four treatments total.
- Treatments:
  - D: diesel exhaust
  - O3: ozone
  - D+O3: diesel exhaust and ozone combined
  - CON: natural air (control)

## Variables and Measurements
- Pollutants (center-of-ring concentrations):
  - NOx (Column S)
  - NO (Column Q)
  - NO2 (Column R)
  - Ozone (Column P)
- Treatment assignment (Column E): D, O3, D+O3, CON
- Temporal data (Periodicity indicators):
  - Year (Column A)
  - Date (Column B)
  - Time (Column C)
- Wind environment (surrounding ring measurements):
  - South ring: ws1, wd1 (Columns F, K)
  - West ring: ws2, wd2 (Columns G, L)
  - North ring: ws3, wd3 (Columns H, M)
  - East ring: ws4, wd4 (Columns I, N)

## Temporal and Spatial Context
- Location details:
  - Field of wheat
  - Coordinates for 2018: latitude 51.482853, longitude -0.897749
  - Coordinates for 2019: latitude 51.482374, longitude -0.895855
- Sampling period spans two years (2018 and 2019) with high-frequency (1-minute) recordings.

## Data Collection and Instrumentation
- Center-ring concentrations monitored with automated switching to the appropriate analyzer.
- O3 and NOx concentrations captured with specified Thermo Scientific models.
- Wind data captured from four cardinal directions around the field to contextualize dispersion.

## Potential Analyses and Uses
- Assess treatment effects on NOx, NO, NO2, and O3 concentrations via within-ring comparisons and treatment contrasts (D, O3, D+O3 vs. CON).
- Explore temporal patterns and potential diurnal effects using Year, Date, and Time.
- Evaluate dispersion and exposure in relation to wind speed and direction (ws1/wd1, ws2/wd2, ws3/wd3, ws4/wd4).
- Model pollutant dynamics using time-series approaches and possibly mixed-effects models with ring and treatment as factors.
- Support ecological or agricultural impact assessments for crops under different pollution scenarios.

## Data Quality and Access Considerations
- Data are centered on each ring with high temporal resolution; potential for gaps or alignment issues when integrating wind and pollutant data.
- Requires careful handling of multi-source data (pollutants, wind, time stamps) and verification of unit consistency across columns.
- Metadata and dataset discoverability considerations highlighted in the broader data-handling context (e.g., provenance, sources, and documentation).