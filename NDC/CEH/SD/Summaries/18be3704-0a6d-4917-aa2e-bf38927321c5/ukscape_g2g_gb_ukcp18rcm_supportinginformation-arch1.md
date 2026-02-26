# Supporting information for Grid-to-Grid model estimates of river flow for Great Britain driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

- Purpose and scope
  - Provides supporting information for Grid-to-Grid (G2G) hydrological estimates of Great Britain river flow driven by UKCP18 Regional (12 km) climate projections.
  - Outputs cover 1980–2080 on a 1 km x 1 km grid across Great Britain, using a 12-member perturbed parameter ensemble (PPE) of the Hadley Centre Regional Climate Model (RCM) under RCP8.5.

- What the dataset includes
  - Grid-to-Grid river-flow estimates on a 1 km x 1 km grid for non-tidal catchments >= 50 km²:
    - Monthly mean river flow (m3 s-1)
    - Annual maxima of daily mean river flow (m3 s-1)
    - Annual minima of 7-day mean river flow (m3 s-1)
  - Temporal coverage: December 1980 to November 2080 (water-year alignment for annual statistics)
  - Spatial domain: 700 km x 1000 km GB national grid
  - Outputs provided as NetCDF4 files, one file per ensemble member per variable

- G2G model overview
  - A national-scale, 1 km grid hydrological model running at a 15-minute time-step
  - Produces spatially-consistent gridded river flows for gauged and ungauged rivers
  - Uses precipitation, potential evapotranspiration (PE), and daily min/max temperature (for optional snow module)
  - Generally uses broadly applicable (non-site-specific) parameters; accounts for urban/suburban runoff via land-cover effects
  - Performance: best in natural-flow regimes; less robust where artificial abstractions/discharges or complex subsurface hydrology dominate

- Data inputs and processing
  - Meteorological drivers: UKCP18 Regional (12 km) projections (12 PPE members)
  - Preprocessing steps:
    - Bias-correction of daily precipitation using monthly multiplicative factors
    - PE derived with Penman-Monteith scheme, aligned with MORECS-like approach
    - Downscaling:
      - Precipitation and PE downscaled from 12 km to 1 km using spatial weighting
      - Daily min/max temperature downscaled with elevation-based lapse rates; diurnal variation via sine curve
    - Time handling: 360-day calendar used in climate model data; 30-day months
  - Model inputs: time-series of precipitation, PE, daily min/max temperature
  - Outputs and format specifics:
    - Monthly mean flows (first day of the month assigned)
    - Annual maxima of daily mean flows; and dates of occurrence
    - Annual minima of 7-day mean flows; and dates of occurrence
    - Domain excludes tidal/sea areas; grid cells with catchment area < 50 km² are set to missing (-9999)

- Data structure and file naming
  - NetCDF4 files named by variable and ensemble:
    - G2G_GB_mmflow_UKCP18RCM_ensnum_1980_2080.nc (monthly mean flow)
    - G2G_GB_amaxflow_UKCP18RCM_ensnum_1980_2080.nc (annual maxima)
    - G2G_GB_aminflow_UKCP18RCM_ensnum_1980_2080.nc (annual minima)
  - Spatial grid: 700 km x 1000 km GB domain; 1 km x 1 km grid cell centers
  - Temporal units: days since 1900-01-01
  - Time alignment: annual maxima/minima assigned to the start year of the corresponding 12-month (water-year) period; dates of occurrence stored as days since 1900-01-01
  - Ancillary datasets to facilitate use:
    - UKSCAPE_G2G_GB_CatchmentAreaGrid.nc: catchment area (km²) per 1 km cell
    - UKSCAPE_GB_NRFAStationIDs.csv: NRFA gauging station IDs mapped to grid cells, plus a grid file UKSCAPE_GB_NRFAStationIDGrid.nc
  - Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 omitted)

- How to use the dataset
  - Historical vs future comparison:
    - Compare G2G outputs driven by UKCP18 Regional data to those driven by observation-based inputs or NRFA observations statistically over multi-decadal periods; avoid point-by-point time-matching
  - Ensemble-consistent comparisons:
    - When comparing periods, use the same ensemble member for baseline and future periods
  - Context and related work:
    - Results are analogous to MaRIUS-G2G-WAH2-monthly datasets (weather@home2 driving data)
  - Practical guidance:
    - Use the NRFA station grid for potential validation against observed river flows
    - Additional caveats apply for small catchments due to discretisation differences between observed catchments and 1 km grid cells

- Caveats and limitations
  - Real-world complexities:
    - Caution when interpreting in-stream flow for catchments with significant anthropogenic influence or complex subsurface hydrology
  - Data limitations:
    - Bias-corrected precipitation and downscaling introduce uncertainties; comparisons should be statistical, not pointwise
    - Some catchments may have catchment-area differences between observed NRFA areas and the discretised 1 km grid
    - Data are provided only for non-tidal river cells with catchment area ≥ 50 km²; non-compliant cells are missing
  - Calendar and timing:
    - 360-day calendar used in climate model data; 30-day months can affect precise timing interpretation
  - Potential mismatches:
    - Location and catchment area concepts may not perfectly align between NRFA observations and the discretised G2G grid

- Acknowledgements and references
  - Funded by the Natural Environment Research Council under UK-SCAPE programme (NE/R016429/1)
  - Acknowledges contributions from researchers including Kay, Bell, Davies, Lane, and others
  - Key references listed for G2G methodology, bias correction, and related hydrological modeling and climate projections

- Summary of the dataset’s purpose for decision-making
  - Enables high-resolution, climate-change-informed estimates of river flows across Britain
  - Supports assessment of potential climate-change impacts on water quantity and hydrological extremes at the grid-cell level, informing policy and management decisions in water resources and environmental planning