# Supporting documentation for data

- Purpose and site context
  - Clocaenog field site is an automated manipulation experiment to project climate change effects on upland moorland over decades.
  - Uses automated roof technology powered by solar and wind; established in 1998.
  - Location: Clocaenog Forest, North East Wales; typical upland moorland with dominant Calluna vulgaris (heather) >60% biomass; Vaccinium myrtillus and Empetrum nigrum also present.
  - General site and treatments described in the supporting documentation for the data series; non-continuous measurements and methods summarized here.

- Measurements taken fortnightly
  - Rainfall (mm) at site
    - Measured with a ground-level storage rain gauge (12.7 cm funnel); two-week accumulation.
    - Holiday periods may extend to 3–4 weeks; gauge is robust to logger/power issues, preferred over AWS data when hourly data not required.
  - Plot-level rain throughfall (mm)
    - Collected bi-weekly with a 16.8 cm funnel and 3000 mL bottle per plot.
    - Throughfall data requires calculations to align with site rainfall for seasonal/annual figures.
    - Data quality: if a measurement is compromised (e.g., overflow, bottles blown, funnels off), that data point is excluded and marked 'NA'.
    - Method: compute percent difference in throughfall per treatment and apply to site rainfall to estimate plot rainfall.
  - Water table depth (cm)
    - Measured bi-weekly via water-permeable tubes installed to bedrock (installed in 2009).
    - Measurement aided by head torch; max detectable depths per plot listed (varies by plot).
  - Soil respiration (mg CO2-C m^-2 hr^-1)
    - Measured fortnightly using three opaque 20 cm diameter collars per plot (installed 5–10 cm deep) since 1999.
    - Includes both heterotrophic and autotrophic respiration; vegetation around collars often adjusted but not visually disturbed aside from a 2013 collar modification.
    - From 2014 onward, measurements used an infrared gas analyser (EGM4) with a SRC-1 chamber; 120-second sampling time.
    - Three measurements per plot averaged; unrealistic high values removed before averaging.
    - Conversion: from g CO2 m^-2 hr^-1 to mg CO2-C m^-2 hr^-1 using factor 0.272727 and ×1000.
  - Soil temperature (°C)
    - Measured with a digital thermometer near soil respiration chambers.
  - Soil moisture (Vol%)
    - Measured with a Theta Probe ML3 (Delta-T Devices).
  - Photosynthetically active radiation (PAR)
    - Measured with a pyranometer (Skye Instruments) near each respiration measurement.
  - Data capture and storage
    - Field data sheets collected in the field and transcribed to Excel; values averaged per plot.
    - Measurements linked with plot-level and site-level context (micro-meteorology and AWS data).

- Data interpretation and usage guidance
  - Use of plot-level measurements in conjunction with micro-meteorological data and AWS data recommended to interpret patterns (e.g., soil respiration) beyond site-wide averages.
  - Plot-level versus site-level information can reveal locally varying conditions in soil temperature and moisture.

- Data quality, limitations, and notes
  - Throughfall calculations require careful handling of data gaps and potential measurement failures; data points with issues are excluded.
  - Holidays or extended sampling periods can affect rainfall totals, though storage gauge capacity remains sufficient.
  - 2013 adjustments to soil respiration collars introduced potential local soil dryness effects, requiring consideration when interpreting respiration data.
  - Max detectable water table depths vary by plot, which influences interpretation of depth data.

- References and related documentation
  - Related information and detailed methodologies are in the Clocaenog_supporting_documentation_Data_series.rtf
  - This document provides a summary of methods and methodological changes for the fortnightly measurements described above.