# Annual soil respiration under experimental drought and warming at Clocaenog forest (1999-2016)

- A long-term dataset of fortnightly soil respiration measurements across nine plots under drought and warming treatments at Clocaenog Forest, spanning 1999–2016.
- Aims to quantify annual soil respiration (Rs) and its change under experimental climate manipulations, with data converted to standardized units for comparability.

## Measurements and experimental setup

- Collars and plots
  - Three opaque soil collars (20 cm diameter) per plot, installed 5–10 cm into the soil; vegetation inside collars regularly cleared.
  - In 2013, larger collars used for automated measurements on one long-term collar; surrounding vegetation tied back.
  - Potential issue: collar-adjacent soil around automated collars appears drier, which may affect measurements.
- Measurement methods (temporal changes reflecting technology advances)
  - 1999–2000: static chambers with gas syringe.
  - 2001–2008: portable IR gas analyser (CIRAS-2) with a closed, non-vented chamber.
  - 2008–2013: LI-8100 with a 10 cm survey chamber (vented closed system).
  - 2014 onward: due to a LI-COR fault, measurements with an EGM4 IRGA linked to an SRC-1 chamber.
  - Sampling duration per measurement: 40–120 seconds (shortened in cold periods).
- Data handling and conversions
  - Field data are converted to CO2 flux in mg CO2-C m^-2 h^-1.
  - Unit conversions documented for CIRAS-2 and LI-COR 8100 outputs.
  - Conversion details rely on the ideal gas law to standardize across instruments.

## Calculation of annual soil respiration

- Measurement strategy
  - Fortnightly measurements used to estimate annual respiration.
  - Afternoon measurements assumed to represent daily maximum rates; a 2002 diurnal study found daily averages are about 87% of the daily maximum.
  - Seasonal rates computed, then multiplied by the number of days per season to obtain seasonal emissions.
  - Annual Rs is the sum of the four seasonal emissions.
- Data processing and personnel
  - Rs calculations performed by Maria T. Dominguez and Alwyn Sowerby (1999–2012); Sabine Reinsch (2013–2016).

## Data structure and contents

- Dataset characteristics
  - 163 rows and 4 columns.
  - Columns:
    - Year: measurement year.
    - Plot: plot number (1–9).
    - Treatment: experimental condition (Control, drought, or warming).
    - Rs_annual: annual soil respiration, in g C m^-2 yr^-1.
- Documentation
  - Includes detailed descriptions for each column and the measurement/processing steps.
  - Related journal publications documenting experimental findings and variability.

## Quality considerations and caveats

- Disturbance and environmental changes
  - 2013 collar expansion for automation may have influenced local soil moisture and respiration measurements.
  - Instrument changes across the study period require careful cross-year comparability and rely on stated conversion factors.
- Assumptions and scaling
  - Use of afternoon measurements as daily maximum introduces an assumption that is adjusted with a 2002 diurnal study (daily average ≈ 0.87 × max).
  - Seasonal aggregation assumes consistent seasonal lengths and conversion factors across years.

## Related publications

- Dominguez, M.T., et al. (2015) Sustained impact of drought on wet shrublands mediated by soil physical changes. Biogeochemistry 122:151–163. DOI: 10.1007/s10533-014-0059-y.
- Dominguez, M.T., Smith, A.R., Reinsch, S., Emmett, B.A. (2017) Inter-annual variability of soil respiration in wet shrublands: do plants modulate its sensitivity to climate? Ecosystems 20:796. DOI: 10.1007/s10021-016-0062-3.