# Annual soil respiration under experimental drought and warming at Clocaenog forest (1999-2016)

## Overview
- Long-term study measuring fortnightly soil respiration (Rs) under drought and warming treatments at Clocaenog forest from 1999 to 2016.
- 3 soil collars per plot (opaque, 20 cm diameter) installed 5–10 cm into soil; vegetation within collars regularly managed.
- Measurements combine heterotrophic and autotrophic respiration; data converted to annual soil respiration (Rs_annual) in g C m-2 yr-1.
- 9 plots with three treatments: Control, Drought, and Warming; data structured by year, plot, and treatment.

## Methods and instrumentation (measurement evolution)
- 1999–2000: Static chambers with gas syringe.
- 2001–2008: Portable infra-red gas analyser (CIRAS-2) linked to a non-vented soil respiration chamber.
- Post-2008: LI-8100 analyser with a 10 cm survey chamber (vented system); later replaced by an infra-red gas analyser (EGM4) with SRC-1 chamber from 2014 due to LICOR fault.
- Measurement timing: chamber placement on collar for 40–120 seconds to minimize CO2 build-up; adjusted duration in cold weather.
- Summer 2013: Larger collars installed for automated measurements; surrounding vegetation tied back; potential local drying around collars noted.
- Unit conversions: raw flux units converted to mg CO2-C m-2 h-1 or equivalent, using specified conversion factors and the ideal gas law.

## Calculation of annual soil respiration
- Fortnightly measurements used to estimate annual Rs.
- Daily maximum assumed from afternoon measurements; daily average scaled to 87% of the maximum based on a 2002 diurnal study.
- Seasonal rates calculated, then seasonal emissions multiplied by the number of days in each season.
- Annual Rs = sum of all seasonal emissions.
- Calculations performed by:
  - Maria T. Dominguez and Alwyn Sowerby (1999–2012)
  - Sabine Reinsch (2013–2016)

## Data structure and contents
- Dataset: 163 rows, 4 columns.
- Columns:
  - A: Year (Description: year of measurement)
  - B: Plot (Description: plot numbers 1 to 9)
  - C: Treatment (Description: Control, drought or warming)
  - D: Rs_annual (Description: Estimate of annual soil respiration; Unit: g carbon m-2 yr-1)

## Data quality, limitations, and caveats
- Equipment and collar changes over time (e.g., 2013 larger collars) may affect comparability across years.
- A dry microenvironment around new collars could bias measurements locally.
- Post-2008 instrumentation changes and a LICOR chamber fault necessitated alternative measurement setups, potentially impacting consistency.
- Assumptions in diurnal scaling (87% of daily maximum) and seasonal aggregation introduce potential uncertainty.
- Data capture and harmonization across multiple measurement systems require careful interpretation when comparing across years.

## Data provenance and related publications
- Related journal articles:
  - 2015 Biogeochemistry: Sustained impact of drought on wet shrublands mediated by soil physical changes
  - 2017 Ecosystems: Inter-annual variability of soil respiration in wet shrublands: do plants modulate its sensitivity to climate?
- The dataset records and calculations are linked to these publications, illustrating the broader context and application of the Rs_annual measurements.