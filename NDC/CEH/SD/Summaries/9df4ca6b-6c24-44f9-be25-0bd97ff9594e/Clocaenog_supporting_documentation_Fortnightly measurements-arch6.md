# Supporting documentation for data

## Overview of the site and purpose
- Clocaenog field site in North East Wales (53°03'19"N, -03°27'55"W) is an automated manipulation experiment to study potential climate change effects on an upland moorland habitat.
- Established in 1998; uses solar and wind power; replicated drought and warming treatments.
- Vegetation dominated by Calluna vulgaris (heather) with Vaccinium myrtillus and Empetrum nigrum present.
- General site and treatment information, plus non-continuous measurements, are documented in related supporting documents.
- Fortnightly measurements cover key hydrological and soil/energy flux variables to understand ecosystem responses.

## Measurements and schedule
- Fortnightly data collected for:
  - Rainfall (mm)
  - Plot-level rain throughfall (mm)
  - Water table depth (cm)
  - Soil respiration (mg CO2-C m^-2 h^-1)
  - Soil temperature (°C)
  - Soil moisture (vol%)
  - Photosynthetically Active Radiation (PAR; µmol m^-2 s^-1)

## Methods and data handling

- Rainfall
  - Measured with a ground-level storage rain gauge (12.7 cm funnel); accumulation over two weeks (three weeks during holidays).
  - Preferred over AWS data due to robustness against logger/power issues.
  - Rainfall data used as site total unless only hourly data is required.

- Throughfall
  - Collected bi-weekly using a 16.8 cm funnel and a 3000 mL bottle per plot.
  - Data often require adjustments to be comparable with site-wide rainfall; use throughfall percent change applied to site rainfall to derive plot-level values.
  - If data are compromised (e.g., funnel/bottle issues), exclude the data point and mark as NA.

- Water table depth
  - Measured bi-weekly with water-permeable tubes from surface to bedrock (installed 2009).
  - Measurements taken with a tape measure in the field; maximum detectable depths differ by plot (plotted as listed).

- Soil respiration
  - Measured bi-weekly with three opaque collars per plot (20 cm diameter; 5–10 cm insertion).
  - In 2014, an IR gas analyser (EGM4) with SRC-1 chamber used; 120-second sampling.
  - Data conversion: g CO2 m^-2 h^-1 to mg CO2-C m^-2 h^-1 via factor 0.272727 and multiply by 1000.
  - Three measurements per plot averaged; unrealistically high values excluded.
  - In 2013, bigger collars installed for automated measurements; surrounding vegetation affected by drying near some collars.

- Soil temperature, soil moisture, PAR
  - Measured near the respiration chambers or with provided equipment.
  - Soil temperature: digital thermometer.
  - Soil moisture: Theta Probe (ML3, Delta-T Devices).
  - PAR: pyranometer (Skye Instruments); paired with micro-meteorological data and AWS data for context.
  - Hand-held measurements are encouraged to be supplemented with micro-meteorological and AWS data when interpreting patterns.

- Data recording and processing
  - Field measurements recorded on field sheets, then transcribed into Excel.
  - Measurements averaged per plot to produce plot-level data.
  - Emphasis on using site-level meteorological data and AWS data to support interpretation, while acknowledging local micro-variation at the plot level.

## Data quality, limitations, and considerations
- Data gaps and variability due to:
  - Patchy data coverage and data loss (e.g., throughfall collection issues, bottle overflow, components falling off).
  - Equipment changes (e.g., larger collars from 2013) that may affect measurements locally.
- Preferentially using longer-term, robust rainfall measurements over AWS-derived values; careful handling of NA entries where data are missing or compromised.
- Plot-level measurements can mask local heterogeneity; combining plot-level data with micro-meteorological and AWS data can improve interpretation.

## Related documentation and data series
- Supporting documentation for data series and non-continuous measurements referenced:
  - Clocaenog_supporting_documentation_Data_series.rtf
- This document summarizes methods and any changes to methods over time for fortnightly measurements at the site.