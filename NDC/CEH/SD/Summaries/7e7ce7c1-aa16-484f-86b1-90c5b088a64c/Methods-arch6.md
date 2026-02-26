# EIDC dataset 3: Short-term experiment with lighting rigs on caterpillar activity, Oxfordshire, UK, winter 2019

## Objective
- Assess impacts of Artificial Light At Night (ALAN) on the feeding behavior of nocturnal caterpillars.

## Experimental design
- Two arable sites with no prior lighting history; long grass-margin strips (27 transects of 14 m).
- Lighting rigs installed at transect midpoints to create three treatments on given nights: LED (approx. 5000 K), HPS (approx. 2200 K), and unlit control.
- Nightly sampling (late Jan–mid Feb 2020) on mild nights; typically three transects sampled per night across nine visits.
- Treatment assignment arranged haphazardly to ensure separation (minimum 60 m) between LED, HPS, and unlit transects on a given night.
- Rigs powered by petrol generators placed ~50 m from transect midpoint to minimize noise, vibrations, or fumes effects.
- Sampling method: sweep-netting conducted 60–120 minutes after sunset (mean 89 minutes); transects sampled within 5–10 minutes per night.

## Data collection and quality assurance
- Caterpillars identified by D.H.B. using prior knowledge and literature; specimens stored at -20°C.
- Data captured with standardized forms and entered into a purpose-built Excel spreadsheet with dropdowns to ensure consistency.
- Data entry completed within 24 hours of field visits; records double-checked to remove typing errors.
- Summary statistics and plots generated for completeness checks and outlier assessment; data exported for statistical analysis.

## Data structure and dataset contents
- Dataset file: Boyes_et_al_2021_shortterm_rigs.csv.
- Column definitions:
  - Date: sampling date.
  - Sunset: printed sunset time for that date/location (from timeanddate.com).
  - Site_Name: sampling site (North Farm or Wells Farm) with coordinates.
  - TransectID: transect identifier within the site.
  - Time: sampling time (24-hour clock).
  - MinsPastSunset: minutes past sunset at sampling time.
  - Treatment: unlit, LED, or HPS.
  - Larvae: number of larvae sampled per transect.
  - DaysSinceStart: days since the start of sampling.
  - Temp_forecast_BBC: minimum forecast temperature (°C) from BBC weather app.
  - Temp_Therm_Sampling_time: thermometer reading at sampling time (°C); n/a if not available.
- Data are organized to support analysis of treatment effects on caterpillar activity, alongside temporal and environmental covariates.

## Context, provenance, and accessibility
- Methods follow those described in Street lighting has detrimental impacts on local insect populations (Science Advances, 2021), reproduced under CC BY-NC.
- Authors and affiliations: UK Centre for Ecology & Hydrology; Newcastle University; Butterfly Conservation. Corresponding author: Douglas H. Boyes.
- Data intended for use in statistical analyses of ALAN effects on nocturnal caterpillars, with explicit documentation of data collection and QA steps to facilitate reuse.