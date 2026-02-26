# Historical (1950-2014) and projected (2015-2100) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP6 projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean and annual maximum river flows (m3 s-1) on a 0.1° × 0.1° grid across West Africa.
- Covers historical (1950–2014) and projected future (2015–2100) periods.
- Driven by bias-corrected CMIP6 climate data; uses a distributed hydrological model (HMF-WA).
- Includes two future water-use scenarios: (i) water use varying with projected population change (FAO, 2016) and (ii) water use equal to present-day levels (WO).

## Hydrological Modelling Framework (HMF-WA)
- Physically-based, grid-based, and spatially distributed; accounts for anthropogenic water use, wetlands, and endorheic regions.
- Domain: West Africa and Sahel (approximately 3°–26°N, -18°–25°E) on a 0.1° grid.
- Parameters are not calibrated to individual catchments; relies on physical/soil-property data to represent local hydrology, enabling estimates at ungauged locations.
- Two future water-use scenarios provide an envelope of potential impacts from different water-use trajectories.

## Climate Projections and Scenarios
- CMIP6-based bias-corrected daily climate variables (precipitation, temperature, near-surface air temperature) at ~0.5° grid used to drive HMF-WA.
- 44 ensemble members across three SSP-RCP pathways: SSP126, SSP245, SSP585 (14, 15, 15 members respectively).
- Historical period: 1950–2014; Future period: 2015–2100.
- Potential Evaporation (PE) processed via established formulation (Hargreaves/Samani and Oudin et al.).
- Compared against AQUASTAT population projections for future water use; water-use scenarios reflect population-driven change or continuation of present-day use.

## Outputs and Data Format
- Outputs: monthly mean river flows and annual maximum (AM) of daily river flows (m3 s-1).
- Resolution: 0.1° × 0.1° grid (~10 km × 10 km).
- File formats: NetCDF4 with metadata headers; data arranged as Latitude, Longitude, and time dimensions.
- Output sets include:
  - Historical (BC): HMF-WA_MMFLOW_BC_<model>_HIST_195001-201412.nc
  - Future (BC): HMF-WA_MMFLOW_BC_<model>_<SSP-RCP>_201501-210012.nc
  - Historical (WO): HMF-WA_MMFLOW_BC_WO_<model>_<SSP-RCP>_201501-210012.nc
  - AM flows: HMF-WA_AMFLOW_BC_<model>_HIST_1950-2014.nc and HMF-WA_AMFLOW_BC_<model>_<SSP-RCP>__2015-2100.nc
  - WO variants for AM flows: HMF-WA_AMFLOW_BC_WO_<model>_<SSP-RCP>_2015-2100.nc
- Calendar options per CMIP6 model can be 365/366, 365, or 360 days/year, affecting time dimension length.

## Data Coverage and Examples
- 17 historical realizations and 44 future realizations (across three SSP-RCPs) for monthly mean and AM flows.
- Example figures illustrate inter-model variability (e.g., River Niger, Station Dire, Mali) and spatial maps (e.g., September 2050 monthly mean, 2050 AM flows).

## Performance and Validation
- Validation using observed daily river discharge from GRDC (1981–2010) driven by CHIRPS precipitation and GLEAM PE.
- Across West Africa, median Nash-Sutcliffe Efficiency (NSE) is about 0.62; NSE for log-transformed flows around 0.82.
- Model not calibrated to individual catchments; performs better for large-scale, spatially consistent flows but may underperform in small or mountainous basins.
- Uncertainty arises from lack of catchment calibration, representation of future water networks, and bias-correction limitations.

## How to Use the Data
- Intended for planning floods and droughts at national and regional scales in West Africa.
- Useful for analyzing climate-change impacts on river flows under multiple SSP-RCP scenarios and population-driven water-use changes.
- For extreme events, AM flows enable flood-frequency analyses (e.g., Gringorten plotting positions, fitting distributions with L-moments).
- Guidance: treat the ensemble as a range of possible outcomes; no single ensemble member is preferred or directly comparable to observed flows.
- Spatial resolution (~10 km) means catchments smaller than ~5000 km² are not readily resolved; identify rivers by geo-referenced grid cells rather than precise river channels.

## Data Access and Interpretation Considerations
- NetCDF format supports metadata-rich reading; suitable for GIS and programming environments (Python, Fortran, etc.).
- The full CMIP6 ensemble is large; use monthly mean and AM flows for practical analyses and visualization.
- Comparisons with observed flows should be avoided at the grid level; use comparative analyses across CMIP6 members for future projections.
- Bias-corrected data are widely used for impact studies, though they can narrow uncertainty; interpret changes with consideration of potential biases.

## Data Sources and Acknowledgments
- Observed river discharge: Global Runoff Data Centre (GRDC).
- Forcing data: CHIRPS (precipitation) and GLEAM (PE); AQUASTAT and FAO population projections; UN population data.
- AMMA-2050 project context and FCFA program support.

## Related Work
- CMIP5 HMF-WA datasets exist for historical and future projections; CMIP6 results extend with SSP-RCP frameworks.
- Comparisons between CMIP5 and CMIP6 illuminate differences in projected rainfall patterns and hydrological responses.

## Acronyms (selected)
- AM: Annual Maximum
- CSP: not used here
- CFA: not used here
- CS: CMIP
- FAO AQUASTAT: Food and Agriculture Organization
- GLEAM: Global Land Evaporation Amsterdam Model
- NSE: Nash-Sutcliffe Efficiency
- PE: Potential Evaporation
- RCP/SSP: Climate forcing and socio-economic pathways
- WA: West Africa
- WC: Water use
- WO: Without future population-driven water-use change