# Annual soil respiration under experimental drought and warming at Clocaenog forest (1999-2016)

## Overview
- Long-term fortnightly soil respiration measurements (1999–2016) at Clocaenog forest under drought and warming treatments.
- Measurements taken over the same soil area using three collars per plot; captures both heterotrophic and autotrophic respiration.
- Collar modification in 2013 for automated measurements; surrounding vegetation tied back, with possible drying around automated collars affecting results.
- Data processing includes unit conversions, seasonal aggregation, and annual synthesis.

## Measurement methods and instrumentation
- Collars: three 20 cm diameter collars per plot, installed 5–10 cm deep; vegetation around collars managed to minimize disturbance.
- 2013 change: larger collars added for automated measurements, creating drier soil conditions around one collar per plot.
- Measurement systems over time:
  - 1999–2000: static chambers with gas syringe.
  - 2001–2008: portable infrared gas analyser (EGM-2, CIRAS-2) with a closed chamber (1171 cm3).
  - 2008 onward: LI-8100 with a 10 cm survey chamber (vented closed system).
  - 2014 onward: due to LI-COR fault, switched to EGM4 with SRC-1 chamber (similar system) for continuity.
- Time on collar: 40–120 seconds per measurement; 120 seconds used from 2014 onward.
- Coverage: measurements taken on the same collars across years.

## Data conversion and annual calculations
- Raw data converted to flux units: mg CO2-C m^-2 h^-1 (specific conversions dependent on instrument).
- Unit conversions documented:
  - CIRAS-2 raw: g CO2 m^-2 h^-1 → mg CO2-C m^-2 h^-1 (via factors including 0.272727 and 1000).
  - LICOR 8100 raw: µmol m^-2 s^-1 → mg CO2-C m^-2 h^-1 (via a detailed divisor involving 1,000,000, 3600, 44.0096, 0.272727, 1000).
- Annual calculation approach:
  - Fortnightly measurements treated as daily maxima; daily mean is ~87% of maximum based on a 2002 diurnal study.
  - Seasonal rates computed and scaled by the number of days in each season; annual soil respiration is the sum of seasonal emissions.
  - Calculations performed by Maria T. Dominguez and Alwyn Sowerby (1999–2012) and Sabine Reinsch (2013–2016).

## Data structure
- Dataset composition: 163 rows and 4 columns.
- Columns:
  - Year: year of measurement (description: year).
  - Plot: numeric plot identifier (1–9).
  - Treatment: factor with levels Control, drought, or warming.
  - Rs_annual: annual soil respiration estimate (g carbon m^-2 yr^-1).

## Data provenance and related publications
- Primary dataset created by researchers including Dominguez, Sowerby, Smith, Robinson, Emmett, and colleagues (1999–2016 timeline).
- Related publications:
  - Dominguez et al. (2015) Sustained impact of drought on wet shrublands mediated by soil physical changes. Biogeochemistry 122:151–163. DOI: 10.1007/s10533-014-0059-y.
  - Dominguez et al. (2017) Inter-annual variability of soil respiration in wet shrublands: do plants modulate its sensitivity to climate? Ecosystems 20:796. DOI: 10.1007/s10021-016-0062-3.