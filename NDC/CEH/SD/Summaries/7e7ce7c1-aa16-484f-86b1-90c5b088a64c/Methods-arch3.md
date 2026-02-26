# EIDC dataset 3:
Short-term experiment with lighting rigs on caterpillar activity, Oxfordshire, UK, winter 2019

## Purpose and context
- Short-term experimental study to assess how Artificial Light At Night (ALAN) affects nocturnal caterpillar feeding behavior.
- Methods and framing adopt approaches from Street lighting has detrimental impacts on local insect populations (Science Advances, 2021).

## Study design
- Two arable sites with no history of lighting.
- 27 transects of 14 m each along grass margin.
- Lighting treatments at transect midpoints: LED streetlight (≈5000 K), High-pressure Sodium (HPS) streetlight (≈2200 K), and unlit control.
- Rigs powered by petrol generators placed 50 m from transect midpoint to avoid noise/fume effects.

## Sampling protocol
- Sampling period: late January to mid-February 2020 on mild nights.
- Nine sampling visits; typically three transects sampled per night.
- Sweep netting conducted 60–120 minutes after sunset (mean 89 minutes).
- Treatment order randomized; transects sampled within 5–10 minutes on each night.
- Caterpillars targeted were noctuids (e.g., Xestia xanthographa/x. sexstrigata); specimens stored at -20°C.
- Associated meteorological data included: sunset time and local temperatures.

## Data collection and quality control
- Standardised sweep-netting methodology.
- Caterpillars identified by D.H.B. using established literature; samples stored for potential verification.
- Data captured on standard forms and entered into a purpose-built Excel spreadsheet with dropdowns to minimise errors.
- Data entry completed within 24 hours of field visits; records double-checked for typographical errors.
- Summary statistics and plots produced for completeness checks; data formatted for statistical analysis.

## Data structure and contents
- Dataset file: Boyes_et_al_2021_shortterm_rigs.csv.
- Columns and meanings include:
  - Date: sampling date.
  - Sunset: sunset time for date/location (Timeanddate.com).
  - Site_Name: North Farm or Wells Farm (GPS coordinates provided).
  - TransectID: transect identifier within site.
  - Time: sampling time (24-hour clock).
  - MinsPastSunset: minutes past sunset at sampling.
  - Treatment: unlit, LED, or HPS.
  - Larvae: number of larvae sampled per transect.
  - DaysSinceStart: days since sampling began.
  - Temp_forecast_BBC: minimum forecast temperature (°C) from BBC weather app.
  - Temp_Therm_Sampling_time: thermometer temperature at sampling (°C; n/a if unavailable).

## Licensing, provenance, and data sharing
- Methods draw on a CC BY-NC licensed study; the cited paper is Science Advances 2021.
- Corresponding author contact provided for inquiries.
- Emphasizes data provenance, standardized metadata, and clear data governance practices to support reuse and transparency.