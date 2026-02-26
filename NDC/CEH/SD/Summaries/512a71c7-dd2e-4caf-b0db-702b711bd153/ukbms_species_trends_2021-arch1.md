# About the UK Butterfly Monitoring Scheme

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- Volunteers contribute data; the scheme has monitored butterfly population changes since 1976.
- Sampling framework includes:
  - Standard butterfly transects (Pollard walks) at ~2–4 km routes, weekly up to 26 times/year.
  - Wider Countryside Butterfly Survey (WCBS) in ~1 km squares, 2–3 visits/year.
  - Targeted surveys (single-species transects, timed counts, egg/larval web counts).
- Currently involves over 2,500 actively recorded sites annually.
- All sampling methods are analyzed together to inform biodiversity status and trends.

## Nature of data collected
- Data types:
  - Standard transect counts (pollard-style) recording all species along fixed routes.
  - WCBS transects in stratified-random 1 km squares.
  - Targeted surveys for single species or non-transect methods (timed counts, eggs/larval webs).
- Data capture and storage:
  - Field forms, online entry (UKBMS data site or Transect Walker), then uploaded to a central database.
- Frequency and coverage:
  - Major transects: weekly counts during spring–autumn (April–September); WCBS: 2–3 visits per year.
- Purpose:
  - Generate abundance indices to reflect relative population sizes and trends.

## Data processing and trend analysis
- Abundance indices:
  - Relative measures rather than absolute counts; reflect a constant proportion of population per site.
- Index construction:
  - Generalised Abundance Index (GAI) method (2016) with site-year weighting based on proportion of the flight period surveyed.
  - Uses counts from all methods to estimate seasonal patterns and extrapolate for gaps; observed data weighted more heavily than extrapolated data.
- Outputs:
  - Collated indices for each species.
  - Trends provided as either long-term (since 1976) or over shorter windows (last 10 or 20 years).

## Quality control
- In-field recording and online data entry with automatic checks to flag anomalies (e.g., unusually high counts, out-of-season records).
- Regional oversight:
  - Each site managed by a transect coordinator who reviews records; coordinators can review continuously during the season.
- Validation workflow:
  - Automated and manual checks for: range/out-of-distribution records, flight period alignment, new-site records, extreme or divergent counts.
- Corrections:
  - Data queries and discussions with coordinators/recorders lead to edits in the main UKBMS dataset.

## Details of this data download
- Content:
  - Long-term and short-term trends for all species with sufficient data to produce reliable trends.
- Format:
  - Comma-separated values (.csv) file.
- Timeframe:
  - Long-term trends from 1976 to the most recent year available (start year may vary per species due to data sufficiency).
- Columns (examples):
  - COMMON_NAME, SCI_NAME, NYEARS (years in series), F_LIN_B (annual slope), F_LIN_SE (SE of slope), F_LIN_P (p-value), F_TRENDETAIL (trend description), F_FULL_R (percent change over series).
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (20-year metrics and trend descriptor).
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (10-year metrics and trend descriptor).
- Note:
  - The data reflect trends for species with sufficient data; not all species may have long series.

## Licence and attribution statement
- Licence:
  - Open Government Licence (OGL) for the data download.
- Usage requirements:
  - Include the provided citation with the dataset’s DOI in any reports or publications.
  - Include the attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.
- Additional information:
  - Full licence text and attribution guidelines available via the UKBMS/open-government-licence channel.

## Offer of collaboration and contact details
- Collaboration:
  - UKBMS partners offer advice on data use and interpretation; open to co-authorship and intellectual input on publications, conference presentations, and posters resulting from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology, Marc Botham: ukbms@ceh.ac.uk
  - Butterfly Conservation, Transect coordinator: transect@butterfly-conservation.org