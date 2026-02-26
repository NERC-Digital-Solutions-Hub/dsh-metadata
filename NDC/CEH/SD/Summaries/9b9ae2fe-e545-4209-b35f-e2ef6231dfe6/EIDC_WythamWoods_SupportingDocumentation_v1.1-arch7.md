# Turbulent fluxes of sensible heat and momentum at an ancient deciduous broadleaved forest in southern England

## Overview of dataset
- Time series of turbulent exchanges of sensible heat (H) and momentum (τ) measured above a forest canopy using eddy covariance (EC) at Wytham Woods, Oxfordshire, UK.
- Sampling period: 2014-06-13 13:00 to 2016-01-04 22:00.
- Includes ancillary weather and soil data, plus variables describing turbulence, footprint, and QC.
- Data are prepared for GIS-style mapping and spatial-temporal analysis, with quality indicators and uncertainty estimates.

## Study site
- Location: Wytham Woods flux observation site (approximately 51.7667°N, -1.3333°W), within ~400 ha of ancient broadleaved forest, ~5 km NW of Oxford.
- Climate: temperate maritime; mean annual air temperature ~10.1°C and precipitation ~730 mm.
- Topography and soils: hilltop site with a canopy ~20 m high; soils range from poorly to well-drained clays over sandstone.
- Vegetation: ancient woodland (W8 Fraxinus excelsior - Acer campestre-Mercurialis perennis) with canopy dominated by Pedunculate Oak, Ash, and Sycamore.

## Sampling regime
- Flux measurements conducted from a 27 m tall flux tower above the canopy.
- Automated 30-minute flux averaging periods for H and τ.
- Raw measurements include 20 Hz EC data; meteorological variables (Ta, RH) at 0.1 Hz, both logged as 30-minute means.

## Flux data acquisition
- Instrumentation: Windmaster sonic anemometer thermometer (Gill Instruments) and CR3000 Micrologger.
- Variables: horizontal/vertical wind components, sonic temperature, air temperature, relative humidity.
- Data granularity: 20 Hz raw EC data; 0.1 Hz meteorological data; all summarized to 30-minute means.

## Ancillary data acquisition
- Co-located COSMOS-UK station data merged with EC data.
- Measurements: net radiation (Rnet) and components (SWin, SWout, LWin, LWout), soil heat flux (G) at two locations, soil moisture content (VWC) and soil temperatures (Ts) at two depths, precipitation (Pluvio 2).
- Temporal resolution: 30-minute means (and precipitation sums).

## Data processing
- Processing software: EddyPRO v6.1.
- Computation: 30-minute block-averaged fluxes; corrections for instrument and atmospheric effects (boost-bug, angle of attack, tilt, co-spectral attenuation, humidity effects).
- Uncertainty and QC: random uncertainties for H and τ calculated; QC flags (0 = high quality, 1 = acceptable, 2 = poor).
- Additional outputs: wind speed/direction, friction velocity (u*), Turbulent Kinetic Energy (TKE), temperature scaling parameter (T*), Obukhov length (L), stability parameter (z/L), and flux footprint estimates.

## Quality control
- Outlier removal for H via median absolute deviation; QC flag >1 fluxes removed.
- H fluxes outside -200 to 600 W m^-2 range removed.
- Weekly plots used for manual checks; final user decision on excluding flagged data or applying footprint/u* criteria.

## Data structure and access
- Single CSV file: WythamWoodsMicromet_v1.0.csv containing 30-minute time series.
- Time span: 201406-13 13:00 to 2016-01-04 22:00.
- Missing data: denoted by -9999.
- Variables covered include H, random error estimates, QC flags, τ, wind metrics, u*, TKE, T*, L, z/L, footprint metrics, radiative fluxes (SWin/SWout/LWin/LWout/Rnet), soil heat flux, Ta, RH, pressure, soil temperatures, VWC, and precipitation. Units and variable naming align with Li-COR conventions where applicable.
- Footprint and upwind-distance metrics (X_peak, X_10 through X_90) provided for linking fluxes to source areas.

## Spatial and temporal relevance for GIS work
- Clear geospatial context: site coordinates, canopy height, surrounding land use.
- Rich ancillary data enable spatially-resolved analyses and mapping of surface energy exchanges and soil–atmosphere interactions.
- QC flags and footprint estimates support reliability assessments for map-based visualization and downstream GIS analyses.

## Acknowledgments and references
- Data funded by NERC; ancillary data from COSMOS-UK network.
- Acknowledges site access, technical support, and installation/maintenance of instrumentation.
- References to methodology and supporting datasets provided for data provenance and reproducibility.