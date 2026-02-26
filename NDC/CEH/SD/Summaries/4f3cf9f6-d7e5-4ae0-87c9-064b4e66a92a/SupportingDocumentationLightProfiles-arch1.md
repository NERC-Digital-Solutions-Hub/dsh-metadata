# Vertical profile data of light transmission in Atlantic forests along a disturbance gradient

- A dataset of vertical light transmission profiles in Atlantic forest across disturbance states, associated with the paper “Tropical forest light regimes in a human-modified landscape” (Fauset et al., Ecosphere).
- Captures intact, logged, secondary, and fragmented montane humid Atlantic forest in Brazil.

## Study site and landscape context

- Location: Serra do Mar State Park, Núcleo Santa Virginia, São Luís do Paraitinga, São Paulo, Brazil.
- Forest type: montane moist dense forest with rich species diversity and fog frequent in the area.
- Surrounding landscape: inland pastoral matrix with cattle pasture and eucalyptus plantations; hills inside and outside the park.
- Plots and disturbance states:
  - Continuous forest plots: intact-K, intact-M, logged (pre-1977 park), and secondary (mid-stage regrowth after charcoal clearance).
  - Fragment plots: fragment-C (edge ~30 m from edge) and fragment-L (edge ~30 m from edge, interior ~100 m from edge).
- Fragment history: fragment-C forested since before 1962; fragment-L edge was pasture and interior forested in 1962 (historical imagery).

## Light profile measurements

- Instrumentation: 19 PAR sensors (GaAsP photodiodes) calibrated against a LI-COR 190 quantum sensor; one open-sky reference sensor.
- Deployment: sensors mounted on a canopy-supported structure with a 1 m vertical spacing; data logged with CR200, CR800, and multiplexers.
- Measurement protocol: data collected every 30 seconds; profiles averaged to one-minute values; a canopy tower was used for at least one sample in the secondary plot.
- Profile construction: rope-based sensor suspension from a high tree branch; measurements aimed to cover diffuse light periods to avoid sunflecks.

## Sampling design and metadata

- Field period: March–October 2016.
- Within-plot sampling: 10–12 sampling locations per plot; subplots of 20 x 20 m (10 x 10 m in fragments).
- At each sampling point: the tallest suitable tree selected to enable full light-path measurements; minimum 1 hour to a maximum 3 days per point.
- Height measurements: highest leaves measured with laser/hypsometer or visual estimation.
- Key metadata file: ProfilesMetadata.csv including:
  - Plot name and plot code (ForestPlots.net)
  - Latitude/Longitude
  - Plot Area (ha) and Fragment Area (ha)
  - ProfileID (edge/interior indicators for fragments)
  - Dates of light profile collection (DD/MM, 2015)
  - Estimated top-tree height (m)

## Data processing and profile construction

- Diffuse-condition filtering: manual inspection to select times with diffuse light (avoiding sunflecks).
- Profile calculation:
  - Compute mean % transmission relative to open-sky reference for each sensor.
  - Mean profile per plot: average across sampling points; for fragments, combine edge and interior transects.
  - Above-canopy extrapolation: assume 100% transmission above the top of the sampled canopy.
  - Unmeasured sections: interpolate linearly from 100% at canopy top to the top sensor height; if bottom sensor is above 1 m, values below bottom equal bottom sensor value.
- Depth-from-canopy profiles: also produced by aligning all top-of-canopy measurements at depth 0 and extending down to the plot mean sample-tree height; extrapolate if sample trees are shorter.
- Resulting mean profiles:
  - Mean profiles by height above ground (MeanHeightProfiles.csv)
  - Mean profiles by depth below canopy (MeanDepthProfiles.csv)

## Data files and structure

- Profiles.csv: % transmission profiles by height for each sampling point.
  - Columns: height (m above ground), mean_transmission (%), point (plot identifier), interpol (i = interpolated, e = extrapolated; blank = measured or 100% above canopy), sd (std dev across times), top (flag for canopy top), depth (depth below canopy top; 0 = canopy top).
- MeanHeightProfiles.csv: mean % transmission by height for each plot.
  - Columns: Height (m above ground), Mean_Transmission, SD_Transmission, Plot.
- MeanDepthProfiles.csv: mean % transmission by depth below canopy for each plot.
  - Columns: Depth (m below canopy top), Mean_Transmission, SD_Transmission, Plot.
- ProfilesMetadata.csv: metadata for each profile (as described above) including plot identifiers, locations, areas, profile IDs, dates, and estimated tree height.

## Relevance and potential analyses

- Enables comparisons of light regimes under different disturbance histories and fragment contexts.
- Supports analyses of vertical light attenuation, canopy structure, and their relation to habitat modification.
- Useful for correlating light profiles with forest structure, species composition, and microclimate variations across intact, logged, secondary, and fragmented forests.
- Data processing notes assist reproducibility, including diffuse-condition selection, interpolation/extrapolation rules, and depth-from-canopy standardization.