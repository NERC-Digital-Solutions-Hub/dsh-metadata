# HANDB OOK OF FIEID METHODS Merlevod, 1974. May VEGETATION SURVEY OF SHETLAND HANDBOOK OF FIELD METHODS

- Purpose: A field methods handbook detailing a vegetation survey of the Shetland Islands, outlining how to locate plots, collect data, and prepare for later analysis and modelling of the environment.
- Scope: Focus on terrestrial vegetation; describes plot-based sampling, habitat recording, soil profiling, and auxiliary data (aquatic habitats, animals, management, and land use).

## Context and Objectives for GIS Use

- Document spatially explicit vegetation data to support impact assessment from offshore development and to inform predictive environmental models.
- Provide a replicable, bias-minimising sampling framework suitable for integration into map-based data products and GIS analyses.
- Enable multivariate analysis (e.g., ordination) to quantify vegetation variation and parameterize environmental models.

## Survey Design and Plot Locating

- Plot distribution: Random, to avoid subjective location bias; plots referenced on maps or aerial photographs.
- Ground-to-map translation:
  - Identify a recognizable landscape feature near the target plot as a control point.
  - From the control point, use map bearing and a Silva compass with 100° magnetic declination adjustment; measure ground distance with map scale.
  - Pace out the ground distance, applying corrections for pace length and slope if needed.
- Alternative localization: If aerial photographs at ~1:10,000 scale are available, locate plots on the photo and navigate from ground features to the plot.
- Safety and access: Some plots may be avoided if dangerous (steep cliffs, boggy ground) or on cultivated land without permission.

## Plot Sampling and Quadrat Layout

- Basic sampling unit: 200 m quadrat centered on the plot location.
- Nested quadrats (to scale):
  - 4 m quadrat (inner)
  - 25 m quadrat
  - 50 m quadrat
  - 100 m quadrat
  - 200 m quadrat
- Quadrats are laid out using five cords anchored at the four corners and center, forming concentric sampling areas.
- Random orientation: A cross on the center post is spun to randomize the diagonals’ orientation.
- Field setup and orientation are designed to minimise bias between ground and map locations.

## Data Collection and Field Sheets

- Ground flora recording (per quadrat):
  - Record habitats and plant species, noting presence/absence and obtain percent cover-abundance estimates to the nearest 5%.
  - Start with the 4 m quadrant, then progress outward, recording only species not already found in inner quadrats.
  - Collect unidentified plants and any voucher material; ignore bryophytes and macrolichens growing on non-soil surfaces unless relevant.
  - Provide two independent cover estimates to improve reliability; compute mean coverage.
  - Use the “Code” column for later data sorting (to be ignored on the field sheet copy).
- Soil profile data (central plot center):
  - Expose soil profile with auger; record horizons and depths, including litter, organic, leached, and mineral layers.
  - Assess organic matter content, moisture, texture, color, decomposition, and structure using standardized attributes.
  - If peat or water is present, note corresponding depths and features; maximum depth recorded if deeper than auger.
- Habitat data (Plot habitat sheet and 50 m edge habitat sheet):
  - Record slope and aspect; classify rock-related habitats (outcrops, scree, rock piles) and vegetation habitats (dense heather, grassland, Sphagnum, moss, epiphytic lichens, aquatic bryophytes, macrofungi, trees/shrubs).
  - Document aquatic habitats (ponds, lakes, rivers; bed types; flow rates; springs; seepage; marshes; disturbed water bodies).
  - Capture management and land-use details (fences, drains, sheep enclosures, buildings, rubbish, tracks, roads, burning events, peat digging, quarries).
  - Note nearby 50 m edge features that may influence the plot (e.g., grazing, drainage, crofting activity, saltmarsh, dune systems).
- Aquatic habitats and animals:
  - Use standardized categories for aquatic systems and animals observed (e.g., rabbits, cattle, ponies, grazing indications, droppings, signs of grazing intensity).
- Management and land-use data:
  - Distinguish improved grazing, arable areas, rough grazing, built features, and various human alterations.
- Finishing the plot:
  - Ensure all sheets are filled, collect two soil samples and any unidentified plants, and pack samples for transport.

## Data Formats and Practical Considerations

- Field sheets and figures:
  - Examples of completed sheets illustrate how to fill in species, cover, soil attributes, and habitat types (figures referenced in the guide).
- Data integration potential:
  - The structured, codified data (species lists, cover percentages, soil attributes, habitat types) are designed for later synthesis and modelling, compatible with GIS-based analyses and multivariate ordination.

## Habitat and Landscape Data Details

- Plot habitat (within plot):
  - Attributes include slope, aspect, rock outcrops, grassy and bryophyte habitats, aquatic and epiphytic components, and management features.
- 50 m area habitats:
  - Document habitat types and human impacts within a 50 m radius of the plot (similar categories to the plot habitat sheet; added land-use and infrastructure detail).
- Data visualization readiness:
  - The dataset supports creation of habitat maps, microhabitat layers, and proximity analyses relative to plot points.

## Outputs, Analysis, and Modelling Intent

- Analytical aim: Use collected data to determine the range of variation in Shetland vegetation and to calibrate mathematical models predicting environmental responses to factors such as oil-related development.
- Modelling notes:
  - Multivariate techniques (e.g., ordination) will be applied to the vegetation data to establish variation patterns across plots.
  - The resulting models are intended to support scenario analysis and impact assessments for future development planning.

## GIS-Relevant Considerations

- Spatial data needs:
  - Georeferenced plot locations, nested quadrat coordinates, and habitat/land-use classifications for raster/vector GIS layers.
- Data standards:
  - Consistent field coding for species, habitat types, soil horizons, and management features to enable cross-site comparisons and reproducibility.
- Workflow implications:
  - Clear documentation of data collection procedures to ensure repeatability and integration into GIS databases and modelling pipelines.

## Endnotes and References

- The handbook includes actual field examples (Figures 2, 4, 5, etc.) to illustrate data capture and sheet completion.
- Appendix and example datasets provide context for new field teams and help calibrate field-to-GIS workflows.