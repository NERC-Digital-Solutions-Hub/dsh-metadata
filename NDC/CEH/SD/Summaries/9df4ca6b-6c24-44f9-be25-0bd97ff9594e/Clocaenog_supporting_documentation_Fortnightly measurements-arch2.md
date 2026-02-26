# Supporting documentation for data

- This document describes the Clocaenog field site, an automated manipulation experimental site in upland moorland, designed to simulate potential climate change effects (warming and drought) over coming decades.
- Location and context:
  - Located in Clocaenog Forest, North East Wales (coordinates provided).
  - Established in 1998; uses solar and wind power; replicated drought and warming treatments.
  - Vegetation dominated by Calluna vulgaris (heather), with Vaccinium myrtillus and Empetrum nigrum present.
- Purpose in data monitoring:
  - Provides methods and changes to methods for fortnightly ecological measurements.
  - Supports consistent, standardized data collection to enable environmental health assessment over time.

- Measurements and data collection (fortnightly unless noted otherwise)

  - Rainfall (mm)
    - Measured with a ground-level storage rain gauge (funnel 12.7 cm) accumulating over two weeks.
    - Holiday periods may extend accumulation to 3–4 weeks; gauge capacity sufficient.
    - Preferred over AWS data due to robustness against logger outages and power loss.

  - Plot-level throughfall (mm)
    - Collected bi-weekly using a 16.8 cm funnel and 3000 mL bottle for each plot.
    - Data require adjustments to be comparable with site rainfall; throughfall percent difference applied to site rainfall.
    - Data issues (overflow, bottles blown/cracked, etc.) lead to plot data being marked as NA when compromised.

  - Water table depth (cm)
    - Measured bi-weekly via perforated tubes extending to bedrock (installed 2009).
    - Measurements taken with tape measure and head torch; raw depths entered into field sheets and then a master file.
    - Maximum detectable depths specified per plot.

  - Soil respiration (mg CO2-C m-2 hr-1)
    - Measured fortnightly with three opaque 20 cm diameter collars per plot (installed 1999).
    - Includes both heterotrophic and autotrophic respiration; vegetation around collars managed to minimize disturbance.
    - Since 2014, measurement with infrared gas analyser (EGM4) and SRC-1 chamber; sampling time ~120 seconds.
    - Three measurements per plot averaged; data converted to mg CO2-C m-2 hr-1 with unit conversions; high outliers removed.

  - Soil temperature (°C), Soil moisture (vol%), Photosynthetically Active Radiation (PAR, µmol m-2 s-1)
    - Measured near soil respiration chambers with handheld devices.
    - Also collected with plot-level micro-meteorological data and AWS PAR data; recommended to prefer micro-meteorological/AWS data for analysis.
    - Data recorded on field sheets, transferred to Excel, and averaged per plot.

- Data quality, handling, and processing notes

  - Raw data handling:
    - Field data sheets direct into Excel; raw data consolidated into a master file post-fieldwork.
    - Data series and methods are documented separately (Clocaenog_supporting_documentation_Data_series.rtf).

  - Data quality considerations and decisions
    - Rainfall data: storage gauge preferred for robustness; occasional holiday accumulation acknowledged.
    throughfall data: data loss or sampling issues lead to NA for affected plots; percent-difference method used to align with site rainfall.
    Water table depth: plot-specific maximum measurable depths defined to ensure data validity.
    Soil respiration: collar changes (2013) and potential microclimate effects (drier soil around larger collars) noted as potential bias.
    Temperature, moisture, and PAR: local measurements may mask micro-variability; supplementary micro-meteorological and AWS data recommended for thorough analysis.

- Data storage and accessibility

  - Primary data sources include field data sheets and Excel-based master files.
  - Supporting documentation for the data series is provided separately to detail methods and any non-continuous measurements or methodological changes.

- Ecological and monitoring context

  - The site provides long-term, standardized environmental measurements to assess upland moorland responses to warming and drought.
  - Data support analyses of environmental health and the effectiveness of climate manipulation treatments in a sensitive UK upland ecosystem.