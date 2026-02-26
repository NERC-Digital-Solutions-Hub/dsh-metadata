# Creation of the WATCHForcing Data and its use to assess global and regional reference crop evaporation over land during the twentieth century

## What this data covers
- WATCH Forcing Data (WFD) used to drive land surface and hydrological models across the 20th century.
- Periods: 1901–1957, 1958–2001 (with some variables analyzed for 1979–2001).
- Variables included: PET_rc (Penman-Monteith reference evapotranspiration for a reference crop), PET_PT (Priestley-Taylor), Net Radiation, Vapor Pressure Deficit (VPD), Wind, Rainfall, Snowfall, and Precipitation.
- Spatial scope: global basins including Orange, Murray-Darling, Lena, Ganges-Brahmaputra, and Lena; data are provided per basin.
- Temporal and spatial resolution: historical forcing data aligned to ERA-40, with bias corrections and diurnal/seasonal consistency preserved.

## Data contents and structure highlighted for stewardship
- Forcing variables are provided with consistent units and time steps, enabling cross-variable evaluation.
- Appendix-level table presents basin-scale statistics: averages, slopes (trend per year), minimum/maximum slopes, effective sample size (Neff), and adjusted significance (Adjusted Slope P) for:
  - PET_rc (mm/yr)
  - PET_PT (mm/yr)
  - Net Radiation (W/m^2)
  - VPD (kPa)
  - Wind (m/s)
  - Rainfall (mm/yr)
  - Snowfall (mm/yr)
  - Precipitation (mm/yr)
- Periods examined: 1901–1957, 1958–2001, and 1979–2001 (where available).

## Key basin-level findings (data interpretation guidance)
- Trends are basin- and period-specific; magnitudes are generally small to moderate and vary by variable.
- PET_rc vs PET_PT:
  - PET_rc and PET_PT show different regional trends, underscoring the importance of method choice when integrating WFD into hydrological analyses.
- Net Radiation and VPD:
  - Net Radiation and VPD exhibit noticeable inter-period changes in several basins, contributing to PET trends.
- Wind and Precipitation:
  - Wind tends to be relatively stable across periods in many basins; precipitation signals are mixed, with some basins showing clear trends and others not.
- Rainfall and Snowfall:
  - Rainfall presents both upward and downward tendencies depending on basin and period; Snowfall remains smaller in many basins but shows variation in certain regions.
- Significance indicators:
  - Adjusted Slope P values vary; many basin-period combinations are not statistically significant after adjustment, highlighting substantial uncertainty in regional decadal trends.
- Data caveats from the appendix:
  - 1901–1957 data rely on ERA-40 basis-year ordering, which introduces limitations in interpreting interannual variability and long-term trends for that period.
  - Pre-1958 data quality and bias-correction performance may differ from later periods.

## Practical considerations for data stewards
- Provenance and lineage:
  - Clearly document ERA-40 backbone, subsequent bias corrections, and the basis-year randomization used for 1901–1957.
- Metadata and definitions:
  - Provide explicit definitions for PET_rc and PET_PT, including their assumptions, units, and applicability conditions (e.g., surface resistance, aerodynamics).
  - Document variables, their units, time steps, and interpolation schemes used in WFD.
- Quality flags and uncertainty:
  - Flag basins/periods where ERA-40 limitations or randomization may degrade reliability (notably 1901–1957).
  - Report whether trends are statistically significant after adjustment (Adjusted Slope P) and highlight where results are ambiguous.
- Interoperability and reuse:
  - Ensure consistent netCDF/ALMA conventions (for applicable variables) and align with CRU-based corrections and ERA-40 references.
  - Include cross-references to the per-basin results and the methodological notes on PET_rc vs PET_PT and precipitation/radiation adjustments.
- Documentation scope for end users:
  - Provide guidance on which PET method to prefer by climate region or model type.
  - Supply validation results (e.g., Fluxnet-based comparisons) and caveats related to topography, land cover, and gauge coverage.

## Access and documentation references
- Source: WATCH Forcing Data 1901–2001, including a detailed methodological description (Watch Technical Report) and Appendix tables with basin-specific statistics.
- Appendix Table 1 (ERA-40 basis-year ordering for 1901–1957) documents the years used as ERA-40 basis years and the corresponding sequencing.

## Conclusions for data stewardship
- WATCH Forcing Data provides a comprehensive, bias-corrected meteorological forcing framework for 20th-century hydrological modeling, with explicit documentation of uncertainties and methodological choices.
- The basin-specific statistics illustrate the complexity and variability of climate signals across regions and periods, reinforcing the need for careful metadata, clear guidance on PET-method selection, and transparent uncertainty communication for end users.