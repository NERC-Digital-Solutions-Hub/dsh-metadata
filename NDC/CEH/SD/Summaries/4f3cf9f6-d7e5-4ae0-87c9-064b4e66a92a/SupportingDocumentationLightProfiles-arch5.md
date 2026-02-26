# Vertical profile data of light transmission in Atlantic forests along a disturbance gradient

- A dataset of vertical profiles of light transmission (PAR) in montane humid Atlantic forest along a disturbance gradient in Brazil, associated with the paper Tropical forest light regimes in a human-modified landscape, Fauset et al., Ecosphere.
- Purpose: enable analysis of how light transmission through the canopy varies across intact, logged, secondary, and fragmented forests, with implications for forest structure and microclimate.

## Study site and plots

- Location: Núcleo Santa Virginia, Serra do Mar State Park, São Luis do Paraitinga, São Paulo, Brazil.
- Forest type: montane moist dense Atlantic forest with a steep coastal mountain range; climate ~2300 mm annual rainfall, mean temp ~17°C, frequent fog.
- Landscape context: inland, pastoral matrix with patches of privately owned forest; hilly terrain; fragmented areas drier and hotter than continuous forest.
- Plot design:
  - Continuous forest plots: intact-K, intact-M, logged (pre-1977 selective logging), secondary (mid-stage regenerating).
  - Fragments: fragment-C and fragment-L with two plots each (edge ~30 m from edge; interior ~100 m from edge); adjacent to cattle pasture.
  - Fragment history inferred from aerial imagery; fragment-C forested since before 1962; fragment-L edge formerly pasture, interior forested in 1962.

## Light profile measurements

- Instrumentation: 19 PAR sensors built per Fielder and Comeau (2000) method; GaAsP photodiodes in diffusers, calibrated against a LI-COR 190 sensor.
- Reference: one open-sky sensor connected to a separate datalogger (CR200) placed in clearing or atop canopy tower.
- Data acquisition: sensors multiplexed to capture simultaneous readings; 30-second measurements averaged to 1-minute values.
- Sensor deployment: sensors suspended from supports at 1 m intervals (vertical profile), using a rope over high branches; some measurements taken from a canopy tower.
- Sampling cadence and duration: each sampling point monitored for 1 hour to 3 days, including periods of diffuse light (overcast or dawn/dusk).
- canopy height data: canopy top height measured per sample point using laser rangefinder, hypsometer, or visual estimation.

## Sampling design and fieldwork timeline

- Field period: March–October 2016.
- Within-plot sampling: 10 sampling locations per plot; each location corresponds to a 20 x 20 m subplot (10 x 10 m for fragments).
- Profile depth and height: 18 m long profile sensor; measurements targeted under diffuse conditions to avoid sunflecks.
- Data independence: sampling points spaced at least 20 m apart to ensure independent light environments.
- Special cases: one sample used a narrow canopy tower; for some profiles, measurements above the top sensor were not recorded.

## Data processing and quality considerations

- Processing goal: derive light transmission (% of open-sky PAR) at each height, under diffuse conditions, for each sampling point.
- Steps:
  - Identify diffuse periods to compute mean % transmission for each sensor.
  - Compute mean profile for each plot by averaging across sampling points at each 1 m height.
  - For fragments, combine edge and interior transects.
  - Extrapolations and interpolations:
    - Heights above the top of the sampled tree set to 100% transmission.
    - Unsampled sections between the top sensor and canopy top interpolated linearly from 100% to the top sensor value.
    - If bottom sensor is above 1 m, heights below bottom sensor assumed equal to bottom sensor value.
  - Depth-based profiling: also produce mean profiles by depth from canopy top (0 m at canopy top) up to plot-specific mean canopy height; extrapolate if sample tree shorter than plot mean height.
- Outputs: two forms of mean profiles per plot (by height above ground and by depth below canopy).

## Data files and schema

- Profiles.csv: per-sampling-point profiles with columns:
  - height (m), mean_transmission (%), point (plot identifier), interpol (blank/'i'/'e' indicating interpolated/extrapolated), sd (standard deviation for the point), top (blank or 1 to mark canopy-top), depth (depth below canopy top, 0 at canopy top).
- MeanHeightProfiles.csv: mean transmission by height above ground for each plot.
  - Columns: Height, Mean_Transmission, SD_Transmission, Plot.
- MeanDepthProfiles.csv: mean transmission by depth below canopy top for each plot.
  - Columns: Depth, Mean_Transmission, SD_Transmission, Plot.
- ProfilesMetadata.csv: metadata for each profile with:
  - Plot name, Plot code (ForestPlots.net), Latitude/Longitude, Plot Area (ha), Fragment area (ha), ProfileID, Dates of light profile collection (DD/MM, 2015), Estimated sample tree height (m).

## Metadata, provenance, and reuse

- Data are tied to a published study and are intended for reuse in analyses of light regimes across disturbance gradients.
- The metadata fields support geospatial linking, plot-level filtering, and cross-referencing with ForestPlots.net.
- Note on provenance: fieldwork conducted 2016; some metadata references to 2015 dates for collection windows.

## Data governance and stewardship considerations

- Standards alignment: clear documentation of sensor calibration, open-sky reference, and measurement cadence supports reproducibility.
- Data quality: reliance on diffuse-condition windows; handling of incomplete canopy data through interpolation/extrapolation introduces assumptions that users should account for in analyses.
- Interoperability: multiple plot types and fragment contexts require careful handling when aggregating across plots.
- Limitations and caveats:
  - Missing height measurements above canopy top and below bottom sensors for certain samples; relies on assumptions for those segments.
  - Fragment histories are partially inferred; exact past conditions may vary by fragment.
  - Dates in metadata indicate 2015 collection periods for profiles, while fieldwork occurred in 2016; users should verify temporal alignment with their analyses.
- Access and reuse: data are organized into standard CSV files with explicit column definitions, enabling straightforward ingestion into analysis pipelines and cross-referencing with the associated publication.