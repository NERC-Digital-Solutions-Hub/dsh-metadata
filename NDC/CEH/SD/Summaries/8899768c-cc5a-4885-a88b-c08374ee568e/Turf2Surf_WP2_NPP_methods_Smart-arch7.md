# Site identification and plot location

- Purpose: A comprehensive field protocol for locating, testing, and recording vegetation plots across diverse habitats to enable subsequent GIS-based analysis of productivity (aNPP), biomass, and related environmental variables.
- Approach: Combine GPS coordinates, sketch maps, compass bearings, and measured plot layouts to ensure plots can be refound with minimal trampling and that data are spatially compatible for cross-site and cross-habitat comparisons.

## Plot design by habitat and layout

- Grazed silage fields
  - Four plots per field, placed on a line 3 m from the field boundary and at least 3 m from each other.
  - Boundary length estimated by pacing; inner boundary length derived by subtracting 3 m from each side.
  - Plot locations determined by drawing four random numbers along the inner boundary; each plot oriented north-south to sample vegetation moving away from boundary.
  - Within each plot: lay out a 1x1 m quadrat, photograph, obtain GPS reference, and remove overhanging biomass before cutting to 1 cm height.
  - Exclosures installed after cutting; plots are refound and re-measured in subsequent visits.

- Unenclosed calcareous and acid grasslands
  - Plot location uses a map-based grid over the selected habitat; boundaries are less clearly defined than enclosed fields.
  - Random plotting within the grid; orientation and quadrat protocol as above; exclosures or marker canes used to aid refinding.

- Winter and seasonal visits for unenclosed habitats
  - In winter: select four plots >5 m from boundaries and >=3 m from other plots; establish habitat area and random X,Y coordinates.
  - Summer: peak biomass harvesting, soil and plant tissue sampling (P and N), and LICOR measurements; exclosures or marker canes used to refind plots.

- Montane and special habitats
  - Montane heath: six inverted hanging baskets/cages installed to sample montane vegetation types; follow similar cutting and sampling protocols as unenclosed plots.
  - Habitats where exclosures are not required (e.g., deer-impacted woodland): fewer exclosures; focus on nested woodland plots.

- Woodlands (nested plot design)
  - 14.14 m x 14.14 m nested plot per site; within each plot, two 1x1 m sub-plots placed at random locations (each >=3 m apart).
  - Plot corners marked with coloured canes; two sides paced or measured to set X and Y references; photograph and sketch maps created for refinding.
  - Sub-plots oriented north-south; all biomass cuts to 1 cm; exclosures installed if grazed; markers or posts used when ungrazed.

- Verbal and vernal flora (spring)
  - May visit to detect vernal flora; if present, sub-plots may be cut in flower but still green; tissue sampling and weighing follow subsequent visits.

## Refinding plots and spatial data capture

- Use sketch maps, GPS coordinates, compass bearings, and paced distances to relocate plots with minimal disturbance.
- Markers (marker canes, posts) and exclosures used to aid refinding in summer.
- Record-keeping includes plot numbers, photobox numbers, date, and GPS position for each plot and sub-plot.

## Plot layout and sub-plots

- Within each larger plot (e.g., 14.14 m x 14.14 m), two 1x1 m sub-plots are placed at random locations (determined by random X and Y coordinates between 0 and 14 m).
- Sub-plots are at least 3 m apart; sides of the larger plot are documented as X and Y references for future rerecording.
- Sub-plot orientation, GPS coordinates, and corner markers are logged on the sketch map.

## Seasonal data collection workflow

- Winter visits
  - Location and orientation; establish area; plot coordinates; photograph; cut to 1 cm; weigh; install exclosures or marker posts; minimal trampling.

- Spring visits
  - May: vernal flora check; cut and weigh if present; collect grab samples; return to lab for dry-weight calculations.

- Summer visits (peak biomass)
  - Harvest sub-plots; soil sampling; plant tissue sampling for P and N; LICOR measurement of photosynthetic rate; refind plots; photograph completed plots.

- Autumn visits
  - Revisit plots; harvest/record biomass again; remove exclosures; capture additional data as needed (e.g., regrowth assessment in enclosed vs. unenclosed plots).

## Habitat-specific productivity and biomass protocols

- Sphagnum and bog/heath productivity
  - Sphagnum patches: identify patches, lay 10x10 cm microplots, install cranked wires (three per patch; five patches total intended), record capitula density, and measure shoot extension quarterly over two years.
  - Pleurocarpous mosses: annual production using mesh mats; harvest after one year, dry and weigh, and compute bryophyte productivity with upper/lower bound estimates.

- Dwarf shrubs (bog and heath)
  - Late-summer sampling across patches of differing age since last burn; 1 m2 plots with random sub-plots; cut to 1 cm, weigh, sample for N and P; record species composition and shrub/tree sapling presence.

- Tree and stand productivity in woodlands
  - DBH measurements for all trees/shrubs >1.3 m; height estimation with relascope; tree coring for annual ring analysis; prepare cores for lab analysis; compute annual woody mass increment using a published formula involving form factor, DBH, height, and wood density.

- Leaf production in conifer plantations
  - Estimate leaf production from crown canopy volume; sample branches for current-year growth; weigh dried leaves; combine with branching metrics to estimate annual leaf production per tree.

- Litter and litter-bucket sampling
  - Install 20 random litter buckets per 14.14 m plot (>=2 m apart from subplots); empty and weigh monthly; dry at 80 C; determine litter production per unit area.

- Tree coring and growth calculations
  - Collect cores at 1.3 m height; lab prep includes drying, mounting, sanding; compute annual increment using ring widths and wood density; integrate with other productivity fractions.

- Grassland and meadow cutting protocols
  - Enclosed and unenclosed grasslands: cut to 1 cm, weigh fresh mass, take grab samples, photograph, and repeat across all plots and subplots; exclosures managed to minimize trampling.

## Data products and GIS-ready considerations

- Spatial framework
  - Use consistent georeferencing: GPS coordinates for all plots, sub-plots, exclosures, litter buckets, marker canes, and tree cores.
  - Document plot extents (14.14 m square plots; 1x1 m sub-plots) and relationships to reference features (fences, gates, markers) for long-term refinding.

- Data layers to support GIS visualisations
  - Plot centroids and boundaries (14.14 m plots; 1x1 m sub-plots)
  - Exclosure locations and marker canes
  - Litter bucket locations and outputs (monthly weights)
  - Tree DBH and stems with species labels
  - Sphagnum patch coordinates and cranked wire positions
  - Pathways and transects for minimal trampling design
  - Photos and numeric measurements (dates, photo IDs, sample IDs)

- Data collection cadence
  - Seasonal schedule (Winter, Spring, Summer, Autumn) with explicit steps for cutting, weighing, sampling, and exclosure management
  - Re-finding procedures to ensure data from different years/sites can be aligned geospatially

- Quality and compatibility
  - Standardised measurement units and protocols across habitats
  - Clear mapping between field notes, sketch maps, GPS data, and laboratory results for seamless GIS integration

## References

- Cited foundational methods and calculations (e.g., tree growth, Sphagnum productivity, bryophyte production, and aNPP formulas) to support reproducibility and cross-site comparability.