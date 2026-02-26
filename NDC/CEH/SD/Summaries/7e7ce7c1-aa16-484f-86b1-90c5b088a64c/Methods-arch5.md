# EIDC dataset 3: Short-term experiment with lighting rigs on caterpillar activity, Oxfordshire, UK, winter 2019

## Overview
- Short-term field experiment examining the effects of Artificial Light At Night (ALAN) on feeding behaviour of nocturnal caterpillars.
- Two arable sites with no history of lighting; 27 transects of 14 m on long grass margins.
- Lighting treatments: LED (approx. 5000 K), HPS (approx. 2200 K), and unlit control; rigs placed at transect midpoints and separated by at least 60 m between active transects on a given night.
- Sampling occurred across nine visits, typically sampling three transects per night, between late January and mid-February 2020.
- Caterpillar assemblages were similar to those at main study sites (notably Xestia xanthographa/X. sexstrigata).

## Provenance and licensing
- Methods are drawn from and aligned with Street lighting has detrimental impacts on local insect populations (Science Advances, 2021).
- Reproduced here under CC BY-NC license.
- Authors and affiliations: Douglas H. Boyes et al., with affiliations to UK Centre for Ecology & Hydrology, Newcastle University, and Butterfly Conservation.

## Experimental design and field setup
- Sites: North Farm and Wells Farm (arable fields) with no prior lighting exposure.
- Transects: 27 total, each 14 m; lighting rigs (4 m high) deployed at transect midpoints.
- Treatments: unlit control, LED, and HPS; on each sampling night, three active transects per treatment arranged with at least 60 m separation.
- Power: rigs powered by petrol generators located ~50 m from transects to minimize noise/fume effects.
- Target organisms: night-active noctuids; focus on larval counts via sweep-netting.

## Data collection and quality control
- Sampling method: standardized sweep-netting; caterpillars identified by D.H.B. using prior knowledge and literature.
- Specimens: retained and stored at -20°C.
- Data capture: standardized forms and a purpose-designed Excel spreadsheet with dropdown menus and rules to ensure consistent data entry.
- Timeliness and validation: data entry within 24 hours of field visits; records double-checked to remove typing errors; summary statistics and plots produced as part of completeness checks; data exported in current format for statistical analysis.

## Data structure and file format
- Data file: Boyes_et_al_2021_shortterm_rigs.csv.
- Columns and descriptions:
  - Date: sampling date.
  - Sunset: sunset time for date and location (from timeanddate.com).
  - Site_Name: sampling site (North Farm or Wells Farm) with coordinates.
  - TransectID: transect identifier within the site.
  - Time: sampling time in 24-hour format.
  - MinsPastSunset: minutes past sunset when sampling occurred.
  - Treatment: lighting treatment (unlit, LED, HPS).
  - Larvae: number of larvae sampled on the transect.
  - DaysSinceStart: days since the sampling began.
  - Temp_forecast_BBC: minimum forecasted temperature from BBC weather app (°C).
  - Temp_Therm_Sampling_time: thermometer temperature at sampling (°C) or n/a if unavailable.
- Site coordinates:
  - North Farm: approximately 51.623475, -1.1557505.
  - Wells Farm: approximately 51.702280, -1.0968035.

## Location, timing, and reuse considerations
- Sampling period: late January to mid-February 2020.
- Temporal alignment with mild nights (min temp > 6°C) selected to maximize detectable caterpillar activity.
- Data prepared for integration with broader analyses on ALAN impacts on caterpillar activity and insect populations, with careful documentation to support reuse and reproducibility.
- Governance: dataset is designed with standardized fields, explicit metadata, and a clear licensing framework via CC BY-NC, enabling reuse under that license while acknowledging source methods.