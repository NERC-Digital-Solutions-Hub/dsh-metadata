# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Data accessibility
  - Available under the Open Government Licence at the provided DOI.
  - Must be cited as Kay et al. (2021) with full dataset reference.

- Brief summary of the dataset
  - UK-SCAPE programme provides research on climate change impacts on water quantity across Britain.
  - Grid-to-Grid (G2G) hydrological model outputs for Northern Ireland (NI) at 1 km x 1 km grid, driven by UKCP18 Regional (12 km) projections.
  - Outputs include:
    - Monthly mean river flow (m3 s-1)
    - Annual maxima of daily mean river flow (m3 s-1) for water years (Oct-Sep)
    - Annual minima of 7-day mean river flow (m3 s-1) for Dec-Nov years
  - Driven by a 12-member perturbed parameter ensemble (PPE) of the Hadley Centre Regional Climate Model (RCM), covering Dec 1980 to Nov 2080 under RCP 8.5.
  - Comparisons with observation-based data and observed river flow are possible but should be statistical, not point-by-point.

- Hydrological model overview (Grid-to-Grid)
  - National-scale hydrological model run on a 1 km x 1 km grid with 15-minute time steps.
  - Provides spatially consistent gridded river-flow estimates for gauged and ungauged rivers.
  - Uses standardized (non-site-calibrated) parameters; accounts for urban/land-cover effects on runoff.
  - Performance: generally good across NI, with caveat near flood-regulated areas like downstream of Lough Neagh.

- Model input data and configuration
  - Meteorological drivers derived from UKCP18 Regional (12 km) projections:
    - Daily precipitation
    - Daily min/max temperature
    - Daily potential evapotranspiration (PE)
  - 12 ensemble PPE members on both native model grid and a 12 km GB-aligned grid; used here on the 12 km grid transformed to 1 km resolution.
  - Calendar: 360-day year (12 x 30-day months) used by the climate model data.
  - Bias correction: simple monthly multiplicative bias correction applied to precipitation.
  - PE: computed via Penman-Monteith, aligned with MORECS methodology, with adjustments for future CO2 effects.
  - Downscaling:
    - Precipitation: downscaled from 12 km to 1 km using spatial weighting from 1 km rainfall patterns; temporally downscaled by equal distribution over model time-steps.
    - PE: downscaled to 1 km grid as per precipitation downscaling.
    - Temperature: downscaled from 12 km to 1 km using elevation-based lapse rates; temporal downscaling within day using a sine curve.

- How to use the dataset
  - Historical period comparisons can be made against observation-based inputs or NRFA data, but only statistically over multi-decadal periods.
  - Baseline and future period comparisons can be made to assess potential climate-change impacts on river flows.
  - Ensure ensemble-member consistency when comparing periods (use the same PPE member for both baseline and future).

- Ensemble and data coverage
  - Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 omitted).
  - NI domain: 1 km x 1 km grid cells with non-tidal rivers and catchment area >= 50 km².
  - Time period: December 1980 to November 2080 (water years and Dec-Nov definitions align with outputs).

- Format and structure of the gridded datasets
  - NetCDF4 files, one per ensemble member and per variable:
    - Monthly mean river flow: G2G_NI_mmflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual maxima of daily mean river flow (and dates of occurrence): G2G_NI_amaxflow_UKCP18RCM_ensnum_1980_2080.nc
    - Annual minima of 7-day mean river flow (and dates of occurrence): G2G_NI_aminflow_UKCP18RCM_ensnum_1980_2080.nc
  - Domain and grid:
    - NI on GB National Grid: 187 km x 170 km domain, 1 km resolution
    - Data available for non-tidal river cells with catchment area >= 50 km²; missing (-9999) elsewhere
    - 30-day months due to 360-day calendar; time stamps are days since 1900-01-01
    - Monthly flows nominally assigned to the first day of the month
    - Annual maxima assigned to the start of the 12-month period; annual minima assigned to the start year of the 12-month Dec-Nov period
  - Supporting grids:
    - Catchment Area grid (km²) draining to each 1 km cell
    - Lake grid indicating majority lake cells
    - NRFA station grid mapping 1 km cells to NRFA gauging stations (45 stations mapped to NI domain)

- Additional data and resources included
  - Flow gauging station locations mapped to 1 km grid cells for comparison with observed flows
  - Observationally-driven NI dataset for comparison (complementary to G2G NI outputs)
  - Similar G2G outputs exist for Great Britain (GB) with linked documentation

- Acknowledgements and references
  - Supported by Natural Environment Research Council under UK-SCAPE National Capability (NE/R016429/1)
  - Key methodological references listed (including Bell et al., Kay et al., Davies & Bell, and others) for model structure, bias correction, and downscaling approaches

- Practical considerations and limitations
  - Lake and reservoir storage effects not included; lakes treated as rivers in the model outputs
  - Potential discrepancies in catchment areas due to 1 km discretisation, especially for small catchments
  - Some downstream flows (e.g., near Lough Neagh) may be affected by flood regulation, influencing model performance
  - Direct point-for-point comparisons with observed weather are not appropriate; rely on statistical, multi-decadal analyses for interpretation

- Citation reminder
  - When using the dataset, cite Kay, A.L.; Rudd, A.C.; Davies, H.N.; Lane, R.A.; Bell, V.A. (2021) and the Environmental Information Data Centre dataset DOI.