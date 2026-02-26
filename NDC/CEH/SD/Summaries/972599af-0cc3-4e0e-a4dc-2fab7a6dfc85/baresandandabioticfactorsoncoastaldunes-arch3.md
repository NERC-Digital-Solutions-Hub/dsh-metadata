Bare sand data collection and wind modelling in coastal dune environments

## Overview
- Describes how bare sand and related abiotic factors (wind speed, dune slope, slope aspect) were quantified across four coastal dune sites to test their relationships.
- Combines remote sensing data (aerial imagery, LiDAR DEMs) with computational wind modelling (CFD) and ground-truth style classifications.

## Study sites and data sources
- Locations: Aberffraw, Ainsdale, Morfa Dyffryn, Penhale.
- Aerial imagery collection periods:
  - Aberffraw: April 2015
  - Ainsdale: April 2015
  - Morfa Dyffryn: July 2014
  - Penhale: May 2016
- Digital Terrain Model (LiDAR) years:
  - Aberffraw: 2015
  - Ainsdale: 2016
  - Morfa Dyffryn: 2015
  - Penhale: 2017
- LiDAR and imagery sources: Natural Resources Wales Historic LiDAR Archive; England LiDAR Digital Terrain Model; EDINA Aerial Digimap Service.

## Data collection and generation methods
- Bare sand mapping:
  - Method: Semi-automatic classification in QGIS using the SCP (semi-automatic classification plugin) with a minimum distance algorithm on true-colour RGB images.
  - Training: 60 ROIs total (30 vegetation, 30 bare sand) to represent class color ranges; training polygons of comparable size.
  - Imagery: 0.25 m pixel resolution; cloud-free; spring/summer capture; imagery within 1 year of the corresponding DTM.
  - Repeats: Bare sand classification repeated three times per site due to variability in mapping results.
  - Output: Percentage of bare sand per 2.5 m2 area (per CSV file).
- Topographic variables:
  - Aspect and slope calculated from LiDAR-derived DEMs using QGIS; values averaged over 2.5 m2 areas.
- Wind speed modelling:
  - CFD modelling with OpenFOAM (SIMPLE scheme; RANS; RNG k-ε turbulence).
  - Domain: top boundary 40 x 40 x 40 m tapering to 2.5 x 2.5 x 2.5 m at the surface; upwind inlet at least 100 m from the study area; overall height at least 5x tallest topographic point.
  - Wind data: incident wind conditions derived from meteorological stations for the 10 years preceding the aerial image date; 0.4 m above the surface computed outputs.
  - Turbulence and shear: calculations of shear velocity and vertical profiles (U, k, ε) using specified equations and constants (von Karman κ=0.42, z0=0.175 m).
  - Resolution and convergence: calculations completed when velocity residuals reached 1e-4.
- Data provenance and modelling references: Blocken et al. (CFD wall functions); Congedo (SCP); Delgado-Fernandez et al. (dune dynamics); Smyth et al. (wind flow over dunes); Levin et al. (surface roughness estimation); Mather & Tso (classification methods); Richards & Hoxey (BCs for k-ε).

## Wind modelling and input conditions
- Incident wind conditions (per site):
  - Ainsdale: Crosby station; SSE 10 km; wind dir 252°; wind speed 9.22 m/s.
  - Aberffraw: Valley station; NW 9 km; wind dir 214°; wind speed 9.48 m/s.
  - Morfa Dyffryn: Valley station; NW 56 km; wind dir 214°; wind speed 9.48 m/s.
  - Penhale: Culdrose station; SSW 32 km; wind dir 236°; wind speed 8.76 m/s.
- Domain setup details ensure appropriate sampling of wind fields near dune surfaces.

## Data structure and variables
- File organization: Each location has a CSV file prefixed by the location name.
- Recorded columns:
  - X coordinate: Centroid X (OSGB 1936 / British National Grid) of the 2.5 m2 area.
  - Y coordinate: Centroid Y (OSGB 1936 / British National Grid) of the 2.5 m2 area.
  - Aspect: Compass direction the dune slope faces (2.5 m2 average).
  - Slope: Angle of inclination (2.5 m2 average).
  - Wind speed (m/s): Modelling output at 0.4 m above the surface.
  - % bare sand: Iteration 1 percentage (2.5 m2 area).
  - % bare sand: Iteration 2 percentage (2.5 m2 area).
  - % bare sand: Iteration 3 percentage (2.5 m2 area).

## Temporal coverage
- Aerial imagery: 2014–2016 window across sites (specific years per site as above).
- LiDAR/DTM: 2014–2017 across sites (specific years per site as above).
- Wind data: Incident wind conditions drawn from the 10-year window prior to image collection dates.

## Purpose and analytical objective
- Primary aim: Statistically test relationships between bare sand and three abiotic factors (wind speed, dune slope, dune slope aspect) across coastal dunes.
- Data generated to support environmental health monitoring related to coastal dune dynamics and response to abiotic drivers.

## Data quality, governance, and sharing
- Documentation includes method transparency (training ROIs, iteration approach, CFD setup, and input data sources).
- Metadata elements captured (locations, dates, data sources, resolutions, computational parameters).
- Potential access considerations: public sharing of underlying datasets can be a barrier; dataset preserves provenance and methodology to facilitate reproducibility and governance.

## References
- Blocken, Stathopoulos, & Carmeliet (CFD for atmospheric boundary layer).
- Congedo (SCP documentation).
- Delgado-Fernandez et al. (parabolic dune dynamics and mesoscale relevance).
- Hesp et al. (flow over foredune).
- Levin et al. (surface roughness estimation over dunes).
- Mather & Tso (classification methods for remotely sensed data).
- Richards & Hoxey (BCs for k-ε models).
- Smyth et al. (various dune aerodynamics and mapping studies).