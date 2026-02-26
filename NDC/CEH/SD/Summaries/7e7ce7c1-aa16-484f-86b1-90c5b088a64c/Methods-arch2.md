# EIDC dataset 3: Short-term experiment with lighting rigs on caterpillar activity, Oxfordshire, UK, winter 2019

- Purpose and context
  - Describes a short-term experiment examining the impact of Artificial Light At Night (ALAN) on nocturnal caterpillar feeding behavior.
  - Builds on methods from the Science Advances study on street lighting and insect populations (2021), reproduced under CC BY-NC.

- Study design and setup
  - Sites: two arable sites with no history of lighting.
  - Transects: 27 transects of 14 m established along long grass margins (550 m and 320 m strips).
  - Treatments: lighting rigs at transect midpoints delivering LED (approx. 5000 K), HPS (approx. 2200 K), or unlit control; rigs positioned to ensure each night had three active transects (LED, HPS, unlit) at least 60 m apart.
  - Sampling window: late January to mid-February 2020, on mild nights, sweep netting conducted 60–120 minutes after sunset (mean ~89 minutes).
  - Replication: typically three transects sampled per night; sampling order randomized by transect location.
  - Equipment and safety: petrol-powered generators placed ~50 m from transects to minimize noise/vibration/fume effects.

- Data collection and quality assurance
  - Sampling method: standardised sweep-netting; caterpillars identified in-field by the lead author using existing literature.
  - Specimen handling: caterpillars stored at -20°C.
  - Recording tools: standardized data collection forms; entries transcribed into a purpose-designed Excel spreadsheet with dropdown menus and rules to ensure consistency.
  - Timeliness and accuracy: data entered within 24 hours of field visits; records double-checked to remove typos; summary statistics and plots produced for final completeness checks; data exported for analysis.

- Data structure and variables
  - Primary dataset: Boyes_et_al_2021_shortterm_rigs.csv.
  - Key columns and descriptions:
    - Date: sampling date.
    - Sunset: sunset time for date/location (from timeanddate.com).
    - Site_Name: sampling site (North Farm or Wells Farm) with approximate coordinates.
    - TransectID: transect identifier within site.
    - Time: sampling time in 24-hour format.
    - MinsPastSunset: minutes after sunset when sampling occurred.
    - Treatment: lighting condition (unlit, LED, or HPS).
    - Larvae: number of larvae sampled on the transect.
    - DaysSinceStart: days since sampling began.
    - Temp_forecast_BBC: forecasted minimum temperature (°C) from BBC weather app.
    - Temp_Therm_Sampling_time: thermometer reading at sampling time (°C); n/a if not available.

- Data provenance and accessibility
  - Methodologies directly align with established ALAN research and provide a reproducible data collection and QA workflow.
  - Data are structured for statistical analysis and potential integration with broader environmental datasets.
  - Metadata and explicit data fields support understanding of sampling context, enabling others to access and reuse the underlying data.