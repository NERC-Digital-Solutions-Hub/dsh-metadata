# Historical (1950-2014) and projected (2015-2100) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP6 projected climate data

- Purpose: Provides ensemble hydrological model estimates of river flows across West Africa for historical and future periods to support climate impact planning (floods and droughts) and water resource assessment.
- Scope: Monthly mean flows and annual maximum daily flows on a 0.1° × 0.1° grid (approx. 10 km × 10 km) covering West Africa, including the Sahel, for 1950-2014 (historical) and 2015-2100 (projected).
- Driving data: Bias-corrected CMIP6 climate model output (daily precipitation and near-surface temperature; daily max/min temperatures; potential evaporation estimated with temperature-based methods).
- Hydrological model: HMF-WA, a physically-based, grid-based model that incorporates anthropogenic water use, wetlands, and local hydrological features; not calibrated to individual catchments to ensure spatial consistency across ungauged locations.
- Water-use scenarios: Two future scenarios of water use considered
  - Variant tied to projected population changes (FAO AQUASTAT + UN population projections)
  - Variant with water use equal to present-day
- Output ensemble: 17 historical realizations and 44 future realizations (CMIP6 ensemble members) across three SSP-RCPs (SSP126, SSP245, SSP585).
- File formats and content: NetCDF4 files containing monthly mean flows (MM) and annual maximum flows (AM) for both historical and future periods; BC indicates bias-corrected climate input; WO indicates simulations without population-driven water-use changes.
- Model domain and resolution: West Africa grid from 3°–26° N and -18°–25° E; 0.1° × 0.1° resolution; designed to cover ungauged locations but not to reproduce holds for individual small catchments.
- Performance and caveats: Model performance evaluated against GRDC observed data (1981-2010); median NSE = 0.62 and NSE log = 0.82 across West Africa; calibration not performed at catchment level, which may affect some catchments (smaller/uphill, flashy regimes). Climate historical runs are based on climate model realizations rather than observed records.
- Data usage guidance: Use the full ensemble to explore uncertainty; individual CMIP6 members cannot be treated as preferred; comparisons should be made within the same CMIP6 model across historical vs. future runs (and with/without population-driven water use). Data are suitable for exploring broad regional and national-scale river flow changes and for flood-frequency analysis when applying appropriate statistical methods.
- Applications: Support planning for future floods and droughts, assessment of climate-change impact on river flows, and development of flood-frequency curves (e.g., Gringorten plotting positions, L-moment fits) at grid cells; compare CMIP5 and CMIP6 projections to assess differences in hydrological outcomes.
- Data access and tools: Data provided in NetCDF format; accessible with GIS and programming tools (ArcGIS, NCView, Xconv, Fortran, Python); NetCDF can be converted to ASCII if needed, noting large file sizes.
- Related data: CMIP5 HMF-WA datasets available for historical and future realizations; provides a basis for comparing CMIP5 vs CMIP6 projections.

- Data sources: Observed daily river discharge data from the Global Runoff Data Centre (GRDC); current water use estimates from FAO AQUASTAT; population projections from UN.
- Context and scope: Part of AMMA-2050 and FCFA initiatives to understand monsoon changes and climate impacts on water resources in West Africa; acknowledges limitations of bias correction and model domain assumptions.

- Suggested applications and analyses: 
  - Regional and national-scale analyses of how future climate and water use scenarios affect river flows.
  - Flood frequency curve estimation at grid cells using AM-flow data.
  - Comparative analyses of CMIP5 vs CMIP6 projections to identify differences in hydrological responses.