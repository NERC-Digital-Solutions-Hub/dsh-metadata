# Annual soil respiration under experimental drought and warming at Clocaenog forest (1999-2016)

- Summary of dataset purpose
  - Long-term records of soil respiration (CO2 flux) under drought and warming treatments at Clocaenog forest, 1999–2016.
  - Aims to quantify how soil CO2 efflux responds to experimental climate manipulations across multiple years.

- Data collection and experimental design
  - Fortnightly measurements over the same soil area per plot, using collars installed in December 1999.
  - Three opaque soil collars per plot (20 cm diameter), installed 5–10 cm deep; 3–13 cm above-ground edge.
  - Vegetation inside collars regularly removed; surrounding vegetation not visibly affected.
  - In summer 2013, larger collars were installed over one long-term collar to enable automated measurements; space required around collars caused local drying, potentially affecting measurements.
  - Measurements methods evolved over time:
    - 1999–2000: static chambers with a gas syringe.
    - 2001–2008: portable IR gas analyser (CIRAS-2) with a non-vented chamber.
    - 2008 onward: LI-8100 analyser with a 10 cm survey chamber (vented system), plus a fault leading to 2014 onward use of EGM4 with SRC-1 as a backup.
  - Typical measurement duration: 40–120 seconds (adjusted for cold weather, when respiration is lower); 120 seconds used in later periods.
  - Measurements represented both heterotrophic and autotrophic soil respiration within the measured collars.

- Data processing and unit conversions
  - Raw field data are converted to CO2 flux in mg CO2-C m^-2 h^-1.
  - Instrument-specific conversions:
    - CIRAS-2: from g CO2 m^-2 h^-1.
    - LICOR 8100: from µmol m^-2 s^-1.
  - Conversion formulas provided to harmonize units across instruments (based on the ideal gas law).
  - Data quality notes include handling of measurement timing to avoid CO2 build-up.

- Calculation of annual soil respiration
  - Fortnightly measurements used to estimate annual soil respiration.
  - Daily maximum rate from measurements approximated by assuming afternoon measurements represented the daily maximum.
  - 2002 diurnal study used to adjust daily average as 87% of the daily maximum.
  - Seasonal rates calculated and then summed to yield seasonal CO2 emissions; annual respiration is the sum of seasonal emissions.
  - Calculations performed by:
    - Maria T. Dominguez and Alwyn Sowerby (1999–2012)
    - Sabine Reinsch (2013–2016)

- Data structure and accessibility
  - Dataset comprises 163 rows and 4 columns:
    - A: Year (Entry = Year; Description = year of measurement)
    - B: Plot (Numeric; Description = plot numbers 1 to 9)
    - C: Treatment (Factor; Description = Control, drought or warming)
    - D: Rs_annual (g carbon m^-2 yr^-1; Description = Estimate of annual soil respiration)

- Related publications
  - Dominguez MT, et al. (2015) Sustained impact of drought on wet shrublands mediated by soil physical changes. Biogeochemistry 122:151–163. DOI: 10.1007/s10533-014-0059-y.
  - Dominguez MT, et al. (2017) Inter-annual variability of soil respiration in wet shrublands: do plants modulate its sensitivity to climate? Ecosystems 20:796. DOI: 10.1007/s10021-016-0062-3.

- Data governance and quality considerations for stewards
  - Documentation should capture instrument changes, measurement durations, and any collar alterations (e.g., 2013 automated collar upgrade) that may affect comparability over time.
  - Metadata should include details on installation depth, collar dimensions, and vegetation status within collars.
  - Transparency about data processing steps (unit conversions, diurnal adjustment factor of 0.87, seasonal aggregation) to ensure reproducibility.
  - Note potential methodological effects: drying around larger automated collars and long repair times for LICOR affecting continuity.
  - Ensure clear provenance: assign data creators (Dominguez, Sowerby, Reinsch, Emmett, etc.) and update history for the 1999–2016 dataset.
  - Provide explicit data access notes and citations to related publications to contextualize the data within broader research.