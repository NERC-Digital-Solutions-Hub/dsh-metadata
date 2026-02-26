# EIDC dataset 3: Short-term experiment with lighting rigs on caterpillar activity, Oxfordshire, UK, winter 2019

## Aim
- Investigate how Artificial Light At Night (ALAN) affects nocturnal caterpillar feeding behaviour.
- Use controlled, short-term field experiments on grass-margin transects with different lighting treatments.

## Experimental design
- Sites: two arable grass margins with no history of lighting (North Farm and Wells Farm).
- Transects: 27 transects of 14 m; four-metre high lighting rigs placed at transect midpoints.
- Treatments: LED streetlight (≈5000 K), High-pressure sodium streetlight (≈2200 K), and unlit control.
- Setup: on each sampling night, three active transects (LED, HPS, unlit) separated by at least 60 m.
- Timing: sampling between late January and mid-February 2020 during mild nights (min temp > 6°C) to boost caterpillar activity.
- Sampling method: sweep-netting, conducted 60–120 minutes after sunset (mean ~89 minutes); nine sampling visits with typically three transects per night.
- Lighting logistics: rigs powered by petrol generators placed 50 m from transects to avoid noise/vibration/fumes effects on activity.
- Target organisms: mainly overwintering grass-feeding noctuids, especially Xestia xanthographa and X. sexstrigata.
- Sample handling: caterpillars identified in the field, samples kept at -20°C.

## Data collection and quality control
- Standardised sweep-netting; identifications by the lead author using literature.
- Data capture: standardized forms and a purpose-built Excel spreadsheet with dropdowns; entry within 24 hours of sampling.
- Quality checks: double data-entry review to remove errors; summary statistics and plots to assess completeness and detect outliers.
- Data preparation: data exported in current format for statistical analysis.

## Data structure and key variables
- Primary dataset: Boyes_et_al_2021_shortterm_rigs.csv.
- Key columns and meanings:
  - Date: date of sampling.
  - Sunset: sunset time for date/location (from timeanddate.com).
  - Site_Name: North Farm or Wells Farm.
  - TransectID: transect identifier within the site.
  - Time: sampling time (24-hour clock).
  - MinsPastSunset: minutes after sunset when sampling occurred.
  - Treatment: unlit, LED, or HPS.
  - Larvae: number of larvae sampled per transect.
  - DaysSinceStart: days since the sampling began.
  - Temp_forecast_BBC: minimum forecast temperature from BBC weather app for the date/site.
  - Temp_Therm_Sampling_time: thermometer temperature at sampling time (degrees C; n/a if unavailable).

## Relevance and context
- Methods are adapted from the Science Advances study on street lighting and insect populations (Boyes et al., 2021).
- Provides a concise, controlled field assessment of ALAN effects at local scale, with explicit data collection and QA procedures suitable for downstream statistical modeling and cross-study comparisons.