# Annual soil respiration under experimental drought and warming at Clocaenog forest (1999-2016)

## Overview
- Long-term dataset of fortnightly soil respiration measurements (1999–2016) from 9 plots within Clocaenog forest.
- Measurements capture both heterotrophic and autotrophic soil respiration within fixed collars (three 20 cm diameter collars per plot).
- Data used to calculate annual soil respiration per plot and treatment (Control, drought, warming).
- One plot received automated measurements in 2013, which affected vegetation around two collars and may influence results.
- Final dataset summarizes annual soil respiration in g carbon m^-2 yr^-1 across year, plot, and treatment.

## Measurements and methods by period
- 1999–2000: Static chambers with gas syringe for CO2 flux.
- 2001–2008: Portable infrared gas analyzer (EGM-2, CIRAS-2) with a closed chamber system (SRC-1).
  - Chamber placement on collars; CO2 buildup monitored; measurement duration 40–120 seconds (shortened in cold weather).
- 2008 onward: LI-8100 Analyser with 10 cm survey chamber (vented closed system).
- 2014 onward: Due to a LICOR fault, measurements used EGM-4 with SRC-1 system (similar to earlier setup).
- Sampling time standardized at 120 seconds across periods (with adjustments for conditions).
- Measurements converted to mg CO2-C m^-2 h^-1 with specified unit conversions.

## Data collection design
- Fortnightly measurements conducted in each plot; the three collars per plot are averaged to yield a single plot value per measurement occasion.
- Vegetation around collars managed to minimize disturbance; in 2013, automation required vegetation to be tied away and collars around area became drier, potentially affecting results.
- Seasonal aggregation: seasonal rates calculated from diurnal assumptions; daily maximum rates scaled to daily averages (87% of maximum) based on a 2002 diurnal study.
- Annual soil respiration derived by summing seasonal emissions.

## Data structure and units
- Dataset structure: 163 rows x 4 columns.
- Columns:
  - Year (A): numeric year of measurement.
  - Plot (B): numeric plot identifier (1–9).
  - Treatment (C): factor with levels Control, drought, or warming.
  - Rs_annual (D): numeric annual soil respiration in g carbon m^-2 yr^-1.
- Interpretations:
  - Rs_annual represents the estimated annual soil respiration for each year-plot-treatment combination.

## Data provenance and authorship
- Calculations of annual soil respiration performed by:
  - Maria T. Dominguez and Alwyn Sowerby (1999–2012)
  - Sabine Reinsch (2013–2016)
- Related publications describing findings and climatic sensitivity:
  - Dominguez et al. 2015 (Biogeochemistry)
  - Dominguez et al. 2017 (Ecosystems)

## Considerations for GIS use
- Spatial scope limited to 9 plots within a single forest site; data suitable for plot-level GIS visualizations and temporal trend analyses.
- Instrumentation changes over time introduce potential measurement biases that should be accounted for in GIS-based analyses (e.g., sensor type, chamber configuration, and the 2013 automated collar changes).
- Data can be joined with environmental covariates (season, year, treatment) to explore spatial-temporal patterns in soil respiration under drought and warming scenarios.