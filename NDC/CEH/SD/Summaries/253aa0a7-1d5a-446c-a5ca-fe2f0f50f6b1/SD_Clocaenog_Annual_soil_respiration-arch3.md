# Annual soil respiration under experimental drought and warming at Clocaenog forest (1999-2016)

## Objective and scope
- Long-term measurement of soil respiration under experimental drought and warming at Clocaenog forest from 1999 to 2016.
- Purpose: understand how climate manipulations affect soil CO2 efflux and inform environmental monitoring and policy decisions.

## Monitoring design and methods
- Measurements taken fortnightly over the study period using three opaque soil collars per plot (20 cm diameter; installed 5–10 cm into soil; 3–13 cm edge above surface).
- Vegetation within collars was regularly removed; surrounding vegetation generally unaffected, though 2013 modifications introduced larger collars for automated measurements.
- Post-2013 changes: automated measurements required more space around collars and vegetation was tied back; no vegetation was cut, but the collared area appeared drier, potentially affecting respiration.
- Measurement techniques evolved:
  - 1999–2000: static chambers with a gas syringe.
  - 2001–2008: portable infrared gas analyser (EGM-2) linked to a soil respiration chamber (CIRAS-2 system).
  - Post-2008: LI-8100 Analyser with 10 cm survey chamber (vented closed system) for the same collars.
  - 2014 onward: due to a fault in the LICOR chamber, measurements with EGM4 and SRC-1 system (similar to earlier setup) were used again.
- Sampling time standardized to 120 seconds in later periods; measures converted to flux units.

## Data processing and calculation
- Raw field data converted to CO2 flux expressed as mg CO2-C m^-2 hr^-1.
- Unit conversions accounted for different instruments (CIRAS-2, LICOR 8100) using established factors and the ideal gas law.
- Annual soil respiration calculation:
  - Fortnightly measurements assumed to represent the daily maximum for each day.
  - A 2002 diurnal study established that daily average respiration is about 87% of the daily maximum.
  - Seasonal rates computed, then seasonal emissions multiplied by the number of days in each season; annual respiration is the sum of seasonal emissions.
- Team contributions:
  - 1999–2012: Maria T. Domínguez and Alwyn Sowerby.
  - 2013–2016: Sabine Reinsch.

## Data structure and site details
- Dataset: 163 rows and 4 columns.
  - Year: measurement year.
  - Plot: numeric plot identifiers (1–9).
  - Treatment: factor with levels Control, Drought, or Warming.
  - Rs_annual: annual soil respiration in g C m^-2 yr^-1.
- Measurements conducted across nine plots with three collars per plot; long-term data align measurements to assess treatment effects.

## Data quality, limitations, and governance
- Potential data quality concerns:
  - Methodological changes over time (different instruments) requiring careful cross-calibration.
  - 2013 introduction of larger collars may introduce microhabitat changes (soil drying) affecting comparability.
  - Vegetation management around collars and potential disturbance effects.
- Metadata and data governance considerations highlighted:
  - Need for detailed metadata to ensure data comparability and reuse across methods.
  - Public sharing of underlying data is a consideration and may pose barriers for some datasets.
- Overall emphasis on quality assurance, data cleaning, transformation, and clear presentation of findings.

## Related publications and usage
- Key associated papers:
  - Domínguez et al. (2015). Sustained impact of drought on wet shrublands mediated by soil physical changes. Biogeochemistry 122:151-163.
  - Domínguez et al. (2017). Inter-annual variability of soil respiration in wet shrublands: do plants modulate its sensitivity to climate? Ecosystems 20:796.
- Dataset supports evaluation of drought and warming effects on soil respiration and informs broader climate and ecosystem monitoring frameworks.