# Vertical profile data of light transmission in Atlantic forests along a disturbance gradient

## Overview
- Dataset of vertical profiles of light transmission (PAR) in intact, logged, secondary, and fragmented montane humid Atlantic forest in Brazil.
- Associated with the paper Tropical forest light regimes in a human-modified landscape, Fauset et al., Ecosphere.
- Data describe local light environments across disturbance gradients and forest conditions.

## Study site and sampling design
- Location: Núcleo Santa Virginia, Serra do Mar State Park, São Luis do Paraitinga, São Paulo, Brazil.
- Forest type: Montane moist dense forest; hillside terrain with surrounding pastoral landscapes outside the park.
- Plot types:
  - Within continuous forest: intact-K, intact-M, logged, and secondary (mid-stage secondary after charcoal production).
  - Fragments outside the reserve: fragment-C and fragment-L, each with an edge and interior transect.
- Sampling framework:
  - 1-ha permanent plots in continuous forest (4 plots) and 2 plots in fragments (edge and interior).
  - For fragments, two 10 x 250 m plots per fragment (edge ~30 m from edge, interior ~100 m from edge).
- Historical context: Fragment histories inferred from aerial imagery; interior/exterior arrangements reflect long-term forest presence or prior land use.

## Light profile measurements and instrumentation
- 19 PAR sensors built following Fielder and Comeau (2000) method.
- Sensors calibrated against a LI-COR 190 quantum sensor.
- Open-sky reference sensor deployed in a clearing or atop a canopy tower in the secondary plot.
- Data collection:
  - Sensors suspended along a rope from tree branches using a can be deployed with a canopy setup.
  - Sensor supports spaced at 1 m intervals; measurements taken every 30 seconds and averaged per minute.
- Measurement height: profiles collected up to 18 m; highest measured leaves height recorded for each sampled tree.
- Special cases: one sample used a narrow canopy tower; for some trees, portions above the top sensor were not measured.

## Metadata and field metadata
- ProfilesMetadata.csv includes:
  - Plot name, ForestPlots.net code, geographic coordinates, plot and fragment areas, unique ProfileID, dates of collection, and estimated top-tree height.
  - Dates listed as all 2015 in this metadata file, while fieldwork occurred in 2016 (discrepancy noted in metadata).

## Data processing and derivation of light profiles
- Diffuse-condition filtering: identify times with diffuse light to avoid sunflecks and sun-angle effects.
- Profile construction: compute mean % transmission (relative to open-sky PAR) across all data points collected under diffuse conditions.
- Plot-level mean profiles:
  - Average % transmission at each 1 m height across sampling points.
  - For fragments, combine edge and interior data.
  - Above canopy: assume 100% transmission.
  - Unmeasured sections (top above sensor): estimate via linear interpolation from 100% at canopy top to the measured value at the top sensor.
  - If bottom sensor is below 1 m, assume transmission below that height equals the bottom sensor value.
- Depth-based profiles: also produce mean profiles using depth from canopy top (0 m at canopy top) up to the plot’s mean sample tree height; extrapolate if necessary.
- Files produced:
  - Profiles.csv: mean transmission by height with flags for interpolated/extrapolated values, standard deviations, and indicators for top or depth positions.
  - MeanHeightProfiles.csv: mean transmission and SD by height for each plot.
  - MeanDepthProfiles.csv: mean transmission and SD by depth below canopy for each plot.

## Data files and key columns
- Profiles.csv
  - height, mean_transmission, point (plot identifier), interpol (i/e/blank), sd, top (1 indicates canopy-top row), depth
- MeanHeightProfiles.csv
  - Height, Mean_Transmission, SD_Transmission, Plot
- MeanDepthProfiles.csv
  - Depth, Mean_Transmission, SD_Transmission, Plot
- ProfilesMetadata.csv
  - Plot name, Plot code (ForestPlots.net), Latitude/Longitude, Plot Area (ha), Fragment area (ha), ProfileID, Dates of light profile collection, Estimated sample tree height

## Data quality, limitations, and governance considerations
- Strengths:
  - Multi-condition gradient (intact, logged, secondary, edge/interior fragments) enabling comparisons across disturbance regimes.
  - Rigorous calibration against a reference sensor and standardized measurement protocol.
  - Detailed metadata linking profiles to plots and locations and providing sampling context.
  - Both height-based and canopy-depth-based profile representations facilitate different analytical approaches.
- Limitations and caveats:
  - Some portions of the top-of-canopy to sensor gap were estimated via interpolation; below-bottom sensor, values assumed constant.
  - Unsampled sections near the top and sensor positions introduce extrapolation uncertainties.
  - Dates in metadata indicate 2015 for collection dates, while fieldwork was conducted in 2016; users should verify temporal alignment for analyses.
  - Fragment histories are partially inferred from imagery; precise disturbance histories may be uncertain for some plots.
- Governance implications for data leaders:
  - Clear provenance through metadata and standardized data products supports reproducibility and cross-study integration.
  - Data are organized in a consistent schema (Profiles, MeanHeightProfiles, MeanDepthProfiles, ProfilesMetadata), enabling discoverability and reuse (e.g., with ForestPlots.net).
  - Consideration of updates, versioning, and ongoing data quality checks if integrating with broader data ecosystems.

## Potential uses and relevance for data strategy
- Use cases:
  - Modeling light regimes across disturbance gradients to inform forest management and restoration planning.
  - Cross-site synthesis of vertical light profiles under different forest conditions.
  - Validation and calibration data for remote sensing or ecological models of canopy light transmission.
- Data strategy takeaways:
  - Demonstrates the end-to-end workflow from field measurement to multiple derived products (height- and depth-based profiles) with thorough metadata.
  - Highlights the importance of documenting measurement context (plot-level details, fragment status, and sampling design) for data discoverability and reuse.
  - Provides a robust example of coordinating field data collection with a standardized data product structure suitable for sharing and integration with data platforms.