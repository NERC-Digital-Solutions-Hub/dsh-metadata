# Supporting documentation

- The dataset provides model outputs from an agricultural land-use model at a 2 km grid resolution over Great Britain, covering 2000–2089, under four scenario combinations (climate change with/without a tipping point and with/without widespread irrigation).
- Core output: yearly arable area per grid cell (in hectares, up to 400 ha per cell) across GB. Files come with a grid cell identifier and corresponding 2 km grid coordinates.

## Scenarios and time frame

- Four scenarios:
  - Climate tipping point: No / Irrigation: No
  - Climate tipping point: No / Irrigation: Yes
  - Climate tipping point: Yes / Irrigation: No
  - Climate tipping point: Yes / Irrigation: Yes
- Time period: 2000–2089
- Climate tipping point modeled as AMOC (Atlantic Meridional Overturning Circulation) collapse, implemented with a progressive 2030–2050 strength decline.

## Climate data and driving inputs

- Driving climate data:
  - Met Office Hadley Centre Regional Model Perturbed Physics Ensemble (HadRM3-PPE-UK) for UKCP09 projections.
  - Baseline and historical context span 1950–2100 with 30-year means used for growing seasons (April–September).
  - Bias correction applied by aligning future projections to 1960–1989 observations.
- AMOC collapse scenario:
  - Derived from HadGEM3 GC2 simulations with freshwater perturbation and a subsequent relaxation period.
  - Seasonal means used for temperature and rainfall 50–80 years after perturbation; a linear weighting function models progressive collapse (2030–2050).
- Irrigation representation:
  - Modeled as a threshold rainfall condition, effectively granting irrigation when grid cells fall below the optimal historical rainfall for GB arable farming.

## Model method and data provenance

- Methodology linked to Fezzi & Bateman (2011, 2014) and UK National Ecosystem Assessment work, forming the core agricultural land-use modeling approach.
- Input data sources:
  - GB land-use data from the June Agricultural Census, on a 2 km grid across GB for ten years between 1972–2010.
  - Model outputs calibrated and validated in related studies.

## Data structure and files

- Four CSV files: Ag_model_sc{1..4}.csv
  - Each file corresponds to a scenario:
    - 1: Climate tipping point = No; Irrigation = No
    - 2: Climate tipping point = No; Irrigation = Yes
    - 3: Climate tipping point = Yes; Irrigation = No
    - 4: Climate tipping point = Yes; Irrigation = Yes
  - Contents: grid cell identifier and arable land area (hectares) per cell (max 400 ha).
- Coordinate file: Ag_model_grid_2km.csv
  - Provides easting/northing centers and corner bounds for each grid cell, linked by the unique grid cell identifiers.

## Quality control and documentation

- The data production follows established approaches used in the UK National Ecosystem Assessment and related studies (Fezzi & Bateman; NEA and follow-ons).
- The dataset is described with references to multiple peer-reviewed sources, ensuring transparency and traceability of methods, inputs, and calibration.

## Use considerations and limitations

- Spatial scale and local-level applicability may be constrained by a 2 km grid resolution and reliance on modeled projections.
- AMOC collapse is a simplification with assumed speed and linearity; actual tipping dynamics may differ.
- Irrigation is represented as a rainfall-threshold proxy rather than explicit irrigation water use.
- Historical census data span only ten years within 1972–2010, which may influence calibration relative to longer-term trends.
- Data coverage is GB-wide; extrapolation to non-GB contexts would require caution.

## References

- Bateman, I. et al., 2014. UK National Ecosystem Assessment Follow-on. Work Package Report 3: Economic value of ecosystem services.
- Bateman, I. J. et al., 2013. Bringing ecosystem services into economic decision-making: land use in the United Kingdom. Science.
- Fezzi, C. et al., 2014. Valuing provisioning ecosystem services in agriculture: the impact of climate change on food production in the United Kingdom. Env. & Resource Econ.
- Fezzi, C. & Bateman, I. J., 2011. Structural agricultural land use modeling for spatial agroenvironmental policy analysis. Am. J. Agr. Econ.
- Fezzi, C. et al., 2015. The environmental impact of climate change adaptation on land use and water quality. Nature Climate Change.
- Jackson, L. et al., 2015. Global and European climate impacts of a slowdown of the AMOC in a high-resolution GCM. Climate Dynamics.
- Jenkins, G., 2009. UK climate projections: briefing report. Met Office Hadley Centre.
- Mecking, J. et al., 2016. Stable AMOC off state in an eddy-permitting coupled climate model. Climate Dynamics.
- Nakicenovic, N. et al., 2000. Special report on emissions scenarios (SRES). Cambridge University Press.
- NEA, U., 2011. The UK national ecosystem assessment technical report. UNEP-WCMC.
- Safta, C. et al., 2015. Global sensitivity analysis, probabilistic calibration, and predictive assessment for the data assimilation linked ecosystem carbon model. Geosci. Model Dev.
- UKCP09, 2014. Hadley Centre UK climate projections. UK Atmos. Data Centre.