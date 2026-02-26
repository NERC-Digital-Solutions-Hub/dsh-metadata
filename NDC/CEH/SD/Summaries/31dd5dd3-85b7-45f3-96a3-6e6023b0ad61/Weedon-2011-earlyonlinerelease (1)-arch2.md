# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## Overview
- Documents the creation and use of WATCH Forcing Data (WFD) to drive land surface models (LSMs) and general hydrological models (GHMs) for the twentieth century.
- Provides sub-daily, globally gridded meteorological forcing at 0.5° resolution, enabling analysis of evaporation drivers and climate-change impacts on water resources.
- Compares two PET (potential evapotranspiration) estimation approaches (reference crop PET_rc via Penman-Monteith and PET_PT via Priestley–Taylor) to assess global/regional evaporation dynamics.
- Forcing variables include wind (10 m), temperature (2 m), surface pressure, specific humidity (2 m), downward longwave/shortwave radiation, rainfall, and snowfall.
- Data spans:
  - WFD 1958–2001: ERA-40-based with bias corrections and data adjustments.
  - WFD 1901–1957: ERA-40 years rearranged to preserve sub-daily variability while matching later statistics; includes year-by-year consistency and adjustments for discontinuities.

## PET estimation methods and comparison
- PET_rc (Penman–Monteith, reference crop)
  - Uses standardized surface resistances and aerodynamic resistance with six of eight WFD forcings.
  - Quantifies evaporation potential while incorporating humidity and wind effects.
- PET_PT (Priestley–Taylor)
  - Simplified, radiation-driven PET using α ≈ 1.26 and net available energy.
- Key takeaway
  - PET_rc captures humidity and wind effects and is widely used in GHMs; PET_PT tends to be more reliable in humid regions.
  - Differences between PET_rc and PET_PT can be substantial regionally, influencing hydrological interpretations.

## Basins: Selected examples (PET, forcing, and trends)

### Orange River Basin (c)
- PET_rc (mm/yr)
  - 1901–1957 average: ~1586; slope ~1.23 (per unit time)
  - 1958–2001 average: ~1604; slope ~0.65
  - 1979–2001 average: ~1623; slope negative in the later interval
- PET_PT (mm/yr)
  - 1901–1957 average: ~1115; slope ~0.25
  - 1958–2001 average: ~1123; slope ~1.10
  - 1979–2001 average: ~1131; slope ~0.73
- Net radiation (W/m2)
  - ~96 (1901–1957), ~97 (1979–2001) with small upward trend
- VPD (kPa)
  - ~1.45 (1901–1957) to ~1.53 (1979–2001) with modest increases
- Wind (m/s)
  - ~2.20 (1901–1957) to ~2.21 (1979–2001)
- Rainfall (mm/yr)
  - 1958–2001 average ~346; 1979–2001 ~338
  - Snowfall generally negligible
- Notes: Higher PET relative to rainfall indicates strong evaporative demand; regional trends show moderate increases in PET_rc vs PET_PT, with modest changes in radiation and wind drivers.

### Lena River Basin (f)
- PET_rc (mm/yr)
  - 1901–1957 average ~363; slope ~0.13
  - 1958–2001 average ~367; slope ~-0.05
  - 1979–2001 average ~366; slope ~0.54
- PET_PT (mm/yr)
  - 1901–1957 average ~332; slope ~0.20
  - 1958–2001 average ~340; slope ~0.69
  - 1979–2001 average ~346; slope ~0.39
- Net Radiation (W/m2)
  - Decline from ~79 (1901–1957) toward ~29–30 in later periods
- VPD (kPa)
  - ~0.95 (1901–1957) to ~0.96 (1958–2001) to ~0.93 (1979–2001)
- Wind (m/s)
  - ~1.97 (1901–1957) to ~1.69 (1958–2001) to ~1.68 (1979–2001)
- Rainfall (mm/yr)
  - Long-term total around 1400–1427 mm/yr (1958–2001 ~1426)
- Snowfall (mm/yr)
  - Low, ~25–26 mm/yr (1958–2001)
- Notes: PET values are moderate; PET_PT and PET_rc align closely; net radiation declines in later periods; basin shows large-scale moisture inputs with substantial runoff implications.

### Ganges–Brahmaputra River Basin (h)
- PET_rc (mm/yr)
  - 1901–1957 average ~889; slope ~0.04
  - 1958–2001 average ~870; slope ~-2.26
  - 1979–2001 average ~844; slope ~-1.84
- PET_PT (mm/yr)
  - 1901–1957 average ~799; slope ~0.10
  - 1958–2001 average ~768; slope ~-1.26
  - 1979–2001 average ~752; slope ~-0.90
- Net Radiant (W/m2)
  - ~70–69 (1901–1957 to 1958–2001) with slight declines
- VPD (kPa)
  - ~0.95 (1901–1957) to ~0.92–0.96 (1958–2001)
- Wind (m/s)
  - ~1.69 (1901–1957) to ~1.66 (1979–2001)
- Rainfall (mm/yr)
  - Long-term ~1400–1427 mm/yr; detailed periods show similar magnitudes with variability
- Snowfall (mm/yr)
  - Small, ~25 mm/yr on average (1958–2001)
- Notes: PET_rc typically higher than PET_PT; secular declines in PET_rc and PET_PT after mid-20th century reflect regional hydrometeorology and ERA-40 biases; substantial rainfall supports strong moisture delivery to the basins.

### Murray–Darling River Basin (d)
- Data present in this chunk are incomplete or not shown; no clear basin-wide statistics are provided here.

## General methodological notes and caveats
- WFD provides standardized, quality-controlled forcing data across 1901–1957 and 1958–2001, enabling long-term, cross-basin comparisons of evaporation, soil moisture, and runoff potential.
- PET method choice (PET_rc vs PET_PT) materially affects regional evaporation estimates; humid regions tend to yield more consistent PET_PT estimates relative to PET_rc, while arid/semi-arid regions show larger disparities.
- Pre-1958 data carry greater uncertainty due to sparser gauge networks and potential ERA-40 biases; later periods benefit from more robust observational constraints and bias corrections.
- Validation against flux towers shows good agreement for mean radiative and temperature fields and diurnal cycles at monthly scales; sub-daily precipitation and some regional features remain challenging.
- The approach emphasizes the value of reanalysis-based forcings, careful bias correction, and the need to consider regional variability when attributing hydrological changes.

## Data availability and usage
- WATCH Forcing Data (1958–2001) and (1901–1957) are documented in the WATCH Technical Report and accessible through the EU-WATCH platform.
- The data underpin the WATCH project's goal to assess terrestrial water cycle dynamics across the twentieth and twenty-first centuries, enabling robust, cross-study comparisons of evaporation, soil moisture, and runoff trends.