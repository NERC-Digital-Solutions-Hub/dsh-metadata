# Model output for different scenarios of treebelts situated downwind of an ammonia source

- Purpose: Present model outputs for how planted tree shelterbelts downwind of ammonia sources can recapture ammonia, with benefits for animal welfare and the environment, and potential to disperse emissions away from sensitive habitats.

- Scope and geography:
  - Great Britain covered on a 100 by 100 km grid (10,000 km² per grid cell); Northern Ireland represented by a single 10,000 km² square.
  - Dataset contains scenarios varying canopy depth and tree height while keeping source area and distance to trees constant.

- Meteorological inputs:
  - Based on CHESS-met GB data (1961–2017), aggregated to 100 km × 100 km resolution.
  - Ten-year representative year (2008–2017) with four days per season to capture seasonal variation.
  - Variables used: relative humidity, air temperature, wind speed; PAR derived from incoming solar radiation.
  - Northern Ireland weather approximated by the closest GB grid-square on the west coast of Scotland.

- Tree characteristics and canopy design:
  - Tree heights vary by grid due to geography (soil and weather); heights derived from Forest Research DSS tools (and NI analogues).
  - Treebelt design: a front main canopy (2–4 m spacing) to allow ammonia entry, plus a backstop canopy (conifer/evergreen) with tight spacing (2 m or less) to form a thick barrier.
  - Leaf Area Index (LAI):
    - Main canopy LAI varies by season and age (seasonal LAI values provided for ages corresponding to 5, 15, 25, 50 years and a 2.5 m tree spacing; values increase with age and differ by season).
    - Backstop canopy LAI is constant across seasons (no seasonal variation) and tied to Sitka Spruce (conifer) with a 2 m spacing.
  - LAI and canopy parameters are drawn from 3PGmix model outputs (Forrester & Tang) using Sitka Spruce and Aspen references.

- Modelling approach:
  - Coupled models:
    - MODDAS-2D v2.7.1 (2D Lagrangian Stochastic dispersion) to compute ammonia recapture.
    - OpenFOAM v1706 for turbulence input to MODDAS (Segersson modifications applied to canopy physics).
    - A Python 2.7 coupler links the models.
  - Computation performed on the LOTUS cluster (JASMIN) in parallel.

- Constant scenario variables (unchanged across runs):
  - Ammonia source area: 15 m² (2D domain).
  - Distance between the source shed and trees: 20 m.
  - Particles emitted: 80,000 from source; 800,000 within canopy.
  - Ammonia source density: 951 s m⁻³.

- Data quality and validation:
  - Visual QA of input data; meteorological data mapped and checked; LAI reviewed by Forest Research; input-file generation code reviewed; models themselves are peer-reviewed (OpenFOAM and MODDAS).

- Data structure and key fields:
  - Season: winter, spring, summer, autumn.
  - LAD_BACK, LAD_MAIN: leaf area density for backstop and main canopies.
  - HEIGHT_MAIN, HEIGHT_BACK: canopy heights (m).
  - DEPTH_MAIN, DEPTH_BACK: canopy depths (m, along the X axis).
  - LAI_BACK, LAI_MAIN: leaf area indices (dimensionless).
  - TOTAL_RECAPTURE: overall ammonia recapture percentage for the scenario.
  - MAIN_RECAPTURE: recapture percentage for the main canopy only.
  - BACK_RECAPTURE: recapture percentage for the backstop canopy only.
  - SDEN: source particle density (sm⁻³ s⁻¹).
  - LATITUDE_WGS89, LONGITUDE_WGS84: grid coordinates (WGS84).
  - SQ_NUMBER: GB grid square ID (not used for Northern Ireland).
  - YEAR: plant age category (values correspond to 5, 15, 25, 50 years).
  - TIME: measurement time (3 am or 3 pm; encoded as 3 or 15).

- Data access and provenance:
  - Datasets compiled from published models (MODDAS-2D, OpenFOAM) with a Python coupler; QA and metadata prepared to support discoverability.

- References:
  - Forrester & Tang (2016); Loubet et al. (2006); Robinson et al. (2020) on CHESS-met; Segersson (2017) on OpenFOAM; Bealey et al. (2014) on agro-forestry ammonia modelling.