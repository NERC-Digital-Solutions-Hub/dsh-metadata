# EIDC dataset 3: Short-term experiment with lighting rigs on caterpillar activity, Oxfordshire, UK, winter 2019

- Purpose and scope
  - Short-term experiment to test the impacts of Artificial Light At Night (ALAN) on the feeding behavior of nocturnal caterpillars.
  - Two arable sites with no history of lighting; transects across long grass margins; lighting treatments included LED (approx. 5000 K), HPS (approx. 2200 K), and unlit control.
  - Sampling conducted between late January and mid-February 2020 during mild nights to maximize caterpillar activity.

- Study design and data collection
  - 27 transects of 14 m established across two sites; four-metre-high lighting rigs erected at transect midpoints.
  - Treatments assigned across transects (LED, HPS, unlit) with at least 60 m separation between active treatments on a given night.
  - Nine field visits; typically three transects sampled per night; sampling window 60–120 minutes after sunset (mean 89 minutes).
  - Generators positioned 50 m from transects to minimize noise, vibration, or fumes effects.
  - Sampling method: standardized sweep-netting; caterpillars identified to species/level by study author; samples retained at -20°C.

- Data management and quality control
  - Standardized data collection forms and a purpose-designed Excel spreadsheet with dropdown menus to ensure accurate entry.
  - Data entry conducted within 24 hours of field visits; automated calculations implemented via Excel formulas.
  - Records double-checked to remove typing errors; summary statistics and plots used to assess completeness and identify outliers.
  - Data exported in current format to facilitate later statistical analysis.

- Data structure and metadata
  - Primary dataset: Boyes_et_al_2021_shortterm_rigs.csv.
  - Key columns and definitions:
    - Date: sampling date
    - Sunset: sunset time (from timeanddate.com)
    - Site_Name: sampling site (North Farm or Wells Farm) with approximate coordinates
    - TransectID: transect location identifier within the site
    - Time: sampling time (24-hour clock)
    - MinsPastSunset: minutes since sunset at sampling
    - Treatment: lighting condition (unlit, LED, HPS)
    - Larvae: number of larvae sampled per transect
    - DaysSinceStart: days since the sampling began
    - Temp_forecast_BBC: forecast minimum temperature for the site/date (°C)
    - Temp_Therm_Sampling_time: thermometer reading at sampling time (°C)
  - Data structure captures temporal (date, time, sunset), spatial (site coordinates, transect), experimental (treatment), ecological (larvae counts), and environmental context (temperature) for reproducibility and analysis.

- Reproducibility and openness
  - Methods are aligned with and draw on the referenced Science Advances study on the impacts of street lighting on local insect populations (CC BY-NC).
  - Data are organized to support repeat analyses and cross-study comparisons, with explicit variable definitions and recording procedures to enable reuse.

- Implications for data leadership and governance
  - Demonstrates end-to-end data lifecycle management: standardized collection, clear metadata, quality checks, and ready-to-analyze data format.
  - Enables data discoverability and reuse through explicit field definitions, documentation of collection timing, and accessible CSV dataset.
  - Highlights value of documenting data provenance and collection context (lighting treatments, sampling schedule, temperature context) to support interpretation and cross-study integration.