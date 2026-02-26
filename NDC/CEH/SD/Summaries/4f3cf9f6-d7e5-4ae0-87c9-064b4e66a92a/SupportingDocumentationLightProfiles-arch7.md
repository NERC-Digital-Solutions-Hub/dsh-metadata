# Vertical profile data of light transmission in Atlantic forests along a disturbance gradient

## Overview
- Provides vertical profiles of light transmission (% PAR) through montane humid Atlantic forest under different disturbance states: intact, logged, secondary, and fragments.
- Associated with the paper Tropical forest light regimes in a human-modified landscape, Fauset et al., Ecosphere.
- Aims to enable GIS-based understanding of how light regimes vary with forest condition and structure.

## Study site
- Location: Núcleo Santa Virginia, Serra do Mar State Park, São Luis do Paraitinga, São Paulo, Brazil.
- Forest type: Montane moist dense forest with diverse flora; frequent fog; mean annual precipitation ~2300 mm; mean temperature ~17°C.
- Landscape context: Inside park with continuous forest and hilly terrain; inland is pastoral with patches of privately owned forest, cattle pasture, and eucalyptus.
- Plot design: 1-ha permanent plots within the park (continuous forest) and newly established plots outside the reserve in fragments. Plot types include intact-K, intact-M, logged, and secondary in continuous forest, plus fragment-C and fragment-L with edge and interior transects.
- Fragment history: Edge vs interior sampling; fragment histories inferred from historical imagery (fragment-C forested since before 1962; fragment-L edge previously pasture in 1962).

## Light profile measurements
- Instrumentation: 19 PAR sensors built per Fielder and Comeau (2000) method; GaAsP photodiodes housed in diffuser assemblies; individually calibrated against LI-COR 190 sensor.
- Reference: One open-sky sensor connected to a datalogger used as reference; other sensors connected to multiplexers for simultaneous measurements.
- Deployment: Sensors suspended from supports along a 1 m spacing rope; measurements every 30 seconds, averaged per minute.
- Deployment details: Profile length of 18 m; in some cases top portion (> canopy) not measured; canopy/topography allowed measurement down to 6 m below canopy where possible.
- Sampling protocol: March–October 2016; inside each plot, 10–12 sampling locations; subplots sized 20 x 20 m (or 10 x 10 m for fragments); tallest suitable tree selected for measurements; one sample used a canopy tower.

## Data collection and tree measurements
- Each sampling point: Minimum 1 hour, maximum 3 days of recording under diffuse light conditions (to avoid sunflecks and sun-angle effects).
- Tree height: Highest leaves height measured with laser rangefinder, hypsometer, or visual estimation.
- Sampling density: Aimed to cover spatial variability within each plot under stratified design.

## Data processing and profile construction
- Diffuse-condition filtering: Identify time periods with diffuse illumination to compute percent transmission relative to open-sky.
- Profile calculation: For each point, compute mean PAR transmission (% of open-sky reference) across diffuse periods.
- Height- and depth-based means:
  - Height-based profiles: Mean % transmission at each 1 m height above ground, averaged across sampling points in a plot; for fragments, edge and interior data combined.
  - Top-of-tree gap handling: If top sensor is below crown, interpolate linearly from 100% at canopy top to measured value at top sensor.
  - Below-sensor assumptions: If bottom sensor is above 1 m, values below bottom sensor assumed equal to bottom sensor value.
  - Depth-based profiles: Also compute profiles with depth from canopy top (0 m at canopy top); extend to mean sample tree height; extrapolate downward for shorter trees.
- Special cases:
  - Heights above the topmost sensor treated as 100% transmission.
  - Combined edge/interior data for fragments to produce full fragment profiles.

## Data files and structure
- Profiles.csv: Per-point height-based % transmission profiles with columns:
  - height (m above ground)
  - mean_transmission (%)
  - point (plot identifier)
  - interpol (blank / 'i' / 'e' for interpolated or extrapolated)
  - sd (standard deviation)
  - top (blank or '1' indicating top-of-tree row)
  - depth (depth below canopy top; 0 at canopy top)
- MeanHeightProfiles.csv: Plot-level mean profiles by height above ground
  - Columns: Height, Mean_Transmission, SD_Transmission, Plot
- MeanDepthProfiles.csv: Plot-level mean profiles by depth below canopy
  - Columns: Depth, Mean_Transmission, SD_Transmission, Plot
- ProfilesMetadata.csv: Metadata for the profiles with columns:
  - Plot name (as in document)
  - Plot code (ForestPlots.net code)
  - Latitude/Longitude (decimal degrees)
  - Plot Area (ha)
  - Fragment area (ha)
  - ProfileID (unique ID; edge indicated by 'e', interior by 'i' where applicable)
  - Dates of light profile collection (DD/MM, all 2015)
  - Estimated sample tree height (m)

## GIS-relevance and usage notes
- Rich spatial context: includes precise plot coordinates, fragment locations, and edge/interior distinctions suitable for spatial analysis of light regimes.
- Facilitates mapping of vertical light structure across disturbance gradients (intact, logged, secondary, fragments).
- Data processing rules (diffuse conditions, interpolation/extrapolation, canopy-top depth) are described to support reproducible GIS workflows and integration with other environmental layers.
- Important caveats: sampling gaps for the tallest canopy portions (top of canopy may be underrepresented where sensors cannot reach); some extrapolation applied where necessary; data tied to specific field conditions and dates (diffuse-light windows).

## Reference
- Tropical forest light regimes in a human-modified landscape, Fauset et al., Ecosphere.