# Annual soil respiration under experimental drought and warming at Clocaenog forest (1999-2016)

## Overview
- Long-term dataset of soil respiration measurements at Clocaenog forest, spanning 1999–2016, under drought and warming treatments.
- Fortnightly measurements across plots, reflecting methodological changes over time and the combined CO2 flux from heterotrophic and autotrophic soil respiration.
- Data are processed to produce annual soil respiration (Rs_annual) values per plot and treatment.

## Data collection and measurement methods
- Three opaque soil collars per plot (20 cm diameter) installed 5–10 cm deep; vegetation inside collars regularly removed; collars mark the same soil area across years.
- 2013: larger collars installed for automated measurements; surrounding vegetation tied back, potentially causing soil around collars to dry and affect measurements.
- Measurements by period:
  - 1999–2000: static chambers with a gas syringe.
  - 2001–2008: portable infrared gas analyser (EGM-2, CIRAS-2) with a closed chamber (headspace ~1171 cm3).
  - 2008–2013/14: LI-8100 (10 cm survey chamber) with a vented closed system; long-term collar measurements continued on the same plots.
  - 2014 onward: LICOR fault led to use of EGM4 with SRC-1 chamber (system similar to earlier setups).
- Measurement duration: 40–120 seconds (shortened in cold weather when respiration is low).
- Data units and conversions:
  - Raw data units: g CO2 m^-2 h^-1 (CIRAS-2) or µmol m^-2 s^-1 (LI-8100).
  - Conversions to mg CO2-C m^-2 h^-1:
    - From g CO2 m^-2 h^-1: multiply by 0.272727, then by 1000.
    - From µmol m^-2 s^-1: divide by 1,000,000 × 3600 × 44.0096 × 0.272727 × 1000.
- Measurements represented the CO2 flux from a fixed soil area, encompassing both root and microbial respiration.

## Calculation of annual soil respiration
- Fortnightly measurements used to estimate annual soil respiration.
- Assumption: afternoon measurements represent daily maximum rates.
- 2002 diurnal study used to establish that daily average ≈ 87% of the daily maximum.
- Seasonal rates computed (Spring Mar–May, Summer Jun–Aug, Autumn Sep–Nov, Winter Dec–Feb) and summed to yield annual emissions.
- Rs_annual values are the sum of seasonal emissions for each plot and year.
- Calculations performed by Maria T. Dominguez and Alwyn Sowerby (1999–2012) and Sabine Reinsch (2013–2016).

## Data structure and accessibility
- Dataset size: 163 rows and 4 columns.
- Columns:
  - Year: Numeric year of measurement.
  - Plot: Numeric plot identifier (1–9).
  - Treatment: Factor with values Control, drought, or warming.
  - Rs_annual: Numeric annual soil respiration in g carbon m^-2 yr^-1.
- Column descriptions provide the meaning and units for each field.

## Data quality, limitations and notes
- Habitat disturbance minimal at installation; 2013 collar expansion introduced conditions (vegetation tied back) that may influence measurements through drier surrounding soil.
- Instrument transitions over time required cross-calibration via specified conversion factors; potential comparability issues across different measurement systems.
- 2014 onward measurements used an alternative system due to LICOR fault; careful consideration needed when comparing with earlier data.
- Diurnal adjustment relies on a single 2002 study (87% factor), introducing an assumption for daily maximum vs. average rates.

## Related publications and usage
- Dominguez MT et al. (2015) Sustained impact of drought on wet shrublands mediated by soil physical changes. Biogeochemistry 122:151-163.
- Dominguez MT et al. (2017) Inter-annual variability of soil respiration in wet shrublands: do plants modulate its sensitivity to climate? Ecosystems 20:796.
- Data support interpretation of drought and warming effects on soil respiration, with methodological details and long-term context.