# Vegetation change at whim Moss (2002 -2016) Materials and methods

## Overview
- Study of nitrogen deposition effects on vegetation at Whim bog, Scottish Borders, using controlled dry (NH3) and wet (NH4+/NO3−) deposition.
- Data collected include spatially explicit deposition treatments, soil moisture/chemistry, and vegetation composition over time, suitable for GIS-based visualization and analysis.

## Field site
- Location: Whim bog, transitioning between lowland raised bog and blanket bog; 3–6 m peat depth.
- Climate: Mean air and soil temperatures around 7.9°C and 7.6°C (2002–2016); annual rainfall ~1141 mm.
- Hydrology: Water table typically ~10 cm below surface (drier in 2013 drought, ~24 cm).
- Soils and vegetation: Very acidic peat (pH ~3.4); vegetation dominated by Calluna vulgaris with mosaic of Sphagnum species and ericaceous shrubs.

## Experimental design and treatments
- Two nitrogen deposition systems:
  - Dry deposition: Free-air NH3 release using a 10 m pipe; emissions occur when wind direction is SW (180–215°), temps > freezing, wind > 2.5 m/s; NH3 concentration measured with passive samplers at multiple distances from source.
  - Wet deposition: Sprayed NH4+ and NO3− solutions via a rainwater collection and distribution system; three N-dose levels plus ambient control; PK (phosphorus and potassium) added at low and high N levels to maintain a P:N ratio.
- Treatment structure:
  - Four blocks, 11 treatment combinations per block, total 44 plots (including controls).
  - Treatments designed to yield total N deposition rates of roughly 0.8 (ambient), 1.6, 3.2, and 6.4 g N ha−1 y−1.
  - Frequency: ~120 deposition applications per year, evenly distributed throughout the year except mid-winter.
- Measurements per treatment:
  - Dry NH3: deposition estimated from concentration gradients; ordinary kriging used to interpolate deposition at permanent quadrats.
  - Wet NH4+/NO3−: solution fluxes per plot recorded; soil chemistry monitored.

## Vegetation survey
- Plot layout: In each experimental plot, three permanent quadrats (40 × 40 cm) subdivided into 16 sub-quadrats (10 × 10 cm).
- Survey cadence: Vegetation recorded usually every two years.
- Data captured: Percent cover for each species in each sub-quadrat; species list is bespoke to the study.
- Data aggregation: Sub-quadrat covers averaged to obtain mean cover for each quadrat.

## Data and variables
- Primary dataset: Whim_veg_2002-2006.csv (vegetation data).
- Key variables (examples):
  - year, PLOT, QUADRAT, ASSESSMENT.DATE
  - SPECIES.LIST.NUMBER, SPECIES.LIST.NAME
  - SUB.SQUARE.1-16 (percent cover per sub-square)
  - distance_m (distance from NH3 source for transect plots)
  - Expt (Wet or Dry), PK (PLUSPK or not)
  - BLOCK, TREATMENT, FORM (Ammonia, Nitrate, or Ammonium)
  - Fnh3, Fnh4, Fno3 (fluxes of NH3, NH4+, NO3−)
  - DOSE (total N deposition per plot)
- Data collection and processing:
  - Soil water sampling monthly from 2006 onwards; ion chromatography for ions with detection limits ~0.014 mg L−1 for NH4+-N and ~0.062 mg L−1 for NO3−-N.

## Spatial data considerations
- NH3 deposition gradient captured along transects downwind from the source; downwind deposition interpolated across plots using ordinary kriging.
- Spatial layout includes blocks, plots, quadrats, and sub-quadrats enabling fine-scale mapping of vegetation responses.
- Data supports creating map-based representations of deposition intensity, vegetation composition by location, and changes over time.

## Data quality and limitations
- Data are collected across multiple years with variable survey intervals; mineral deposition fluxes are estimated rather than measured at every location in real time.
- Interpolation assumes spatially homogeneous deposition velocity for NH3; real-world heterogeneity may introduce uncertainty.

## Practical GIS applications
- Create deposition gradient maps (dry and wet) across the 44 plots.
- Map species composition at quadrat and sub-quadrat scales; generate time-series vegetation maps by plot.
- Integrate deposition data with soil chemistry layers to analyze spatial correlations.
- Use the dataset to explore spatial patterns of vegetation change in response to nitrogen deposition over 2002–2016.