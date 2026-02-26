# Vertical profile data of light transmission in Atlantic forests along a disturbance gradient

- Provides vertical profiles of light transmission (% PAR reaching a point) across a disturbance gradient in montane humid Atlantic forest in Brazil.
- Associated with the paper Tropical forest light regimes in a human-modified landscape, Fauset et al., Ecosphere.

## Study site and disturbance gradient

- Location: Núcleo Santa Virginia, Serra do Mar State Park, near São Luis do Paraitinga, São Paulo state, Brazil.
- Forest type: Montane moist dense forest with high biodiversity (palms, ferns, lianas, etc.).
- Climate: ~2300 mm annual precipitation; cool, mild temperatures (mean ~17°C); frequent fog.
- Landscape context: Inland matrix of cattle pasture and occasional eucalyptus plantations; hilly terrain.
- Disturbance gradient sampled:
  - Continuous forest: intact plots (intact-K, intact-M) and a logged area (logged).
  - Secondary forest: regenerating mid-stage secondary forest (secondary).
  - Fragments: two fragments (fragment-C near Catuçaba, fragment-L near Lagoinha) with edge and interior transects.
- Plot design:
  - In-park plots: four plots within continuous forest (two intact, one logged, one secondary).
  - Fragments: two 10 x 250 m transects per fragment, sampling at edge (~30 m from edge) and interior (~100 m from edge), adjacent to pasture.

## Light profile measurements

- Instrumentation: 19 PAR sensors using GaAsP photodiodes with cos-sine diffusers; sensors calibrated against a LI-COR 190 quantum sensor.
- Reference: One open-sky reference sensor connected to a separate datalogger, located in a clearing or atop a canopy tower.
- Data collection: Measurements every 30 seconds; profiles averaged to 1-minute values.
- Sensor deployment: Sensors suspended on cords from supports mounted on trees, with 1 m vertical intervals between sensors.
- Coverage: Profiles collected from ground level up to a maximum of 18 m (top sensor below the canopy top in some cases). In cases where canopy height exceeded sensor reach, the top portion above the highest sensor was not measured and interpolated as needed.
- Tree height: Height of the sampled trees recorded using laser rangefinders, hypsometers, or visual estimation.

## Sampling design and field workflow

- Field period: March–October 2016.
- Within-plot sampling: 10 locations per plot; each location sampled in a 20 x 20 m subplot (10 x 10 m for fragments).
- Selection criteria: At least 20 m between sampling points; tallest suitable tree with clear line of sight for rope/sensor installation.
- Special case: One sample used a canopy tower for sensor suspension.
- Sampling duration: Each point sampled for a minimum of 1 hour to a maximum of 3 days, ensuring periods of diffuse light conditions.

## Metadata and data organization

- ProfilesMetadata.csv: metadata for each light profile with fields:
  - Plot name, Plot code (ForestPlots.net), Latitude/Longitude, Plot Area (ha), Fragment area (ha), ProfileID, Dates of light profile collection (DD/MM, all 2015), Estimated sample tree height (m).

## Data processing and handling

- Diffuse light selection: Manually identify periods under diffuse conditions to avoid sunfleck and sun angle effects.
- Profile computation: For each profile, compute mean % transmission relative to the open sky reference across diffuse periods.
- Plot-level means: For each plot, average % transmission at each 1 m height above ground across all sampling points.
- Fragment data: Edge and interior transect data are combined for mean profiles.
- Unsampled sections:
  - If the top of the tree is higher than the top sensor, interpolate between 100% transmission at the canopy top and the top sensor height.
  - If the bottom sensor is above 1 m, assume transmission below that height equals the bottom sensor’s value.
- Depth-based profiles: In addition to height-above-ground profiles, provide profiles as depth below canopy top (0 m at canopy top) for comparability across trees of varying heights.
  - Depth-based data cover up to the mean sample tree height for each plot; when sample trees are shorter, values are extrapolated downward.
- Notation for data quality: Profiles.csv includes interpolation (‘i’) and extrapolation (‘e’) flags; sd reflects variation across time within a profile point.

## Data files and structure

- Profiles.csv: per-point light profiles
  - Columns:
    - height: height above ground for the measurement
    - mean_transmission: % transmission at that height
    - point: profile plot identifier
    - interpol: blank, 'i', or 'e' indicating measured, interpolated, or extrapolated values
    - sd: standard deviation of % transmission across the timeseries
    - top: blank or '1' (1 indicates the row corresponds to the top-of-tree height)
    - depth: depth below canopy top (0 = canopy top)
- MeanHeightProfiles.csv: mean profiles by height for each plot
  - Columns: Height, Mean_Transmission, SD_Transmission, Plot
- MeanDepthProfiles.csv: mean profiles by depth for each plot
  - Columns: Depth, Mean_Transmission, SD_Transmission, Plot
- ProfilesMetadata.csv: per-profile metadata
  - Columns: Plot name, Plot code, Latitude/Longitude, Plot Area (ha), Fragment area (ha), ProfileID, Dates of light profile collection (DD/MM, 2015), Estimated sample tree height (m)

## Potential uses and considerations for data support

- Cross-plot comparisons:
  - Examine how vertical light regimes differ across intact, logged, secondary, and fragment contexts.
  - Compare edge vs interior light environments within fragments.
- Depth- and height-based analyses:
  - Utilize both Height profiles and Depth profiles to understand light attenuation relative to canopy structure and tree height.
- Data integration:
  - Combine with other ecological or structural measurements from the plots (e.g., tree height, biomass) for multi-factor analyses.
- Quality and limitations:
  - Certain top-canopy measurements may be interpolated or extrapolated; check interpol and top columns for each profile.
  - Field dates are listed as 2015 in metadata, while fieldwork occurred in 2016; consider this when aligning with other time-series data.
  - Measurements stop at the highest sensor’s reach (up to 18 m); higher canopy layers beyond sensor reach are estimated via interpolation.