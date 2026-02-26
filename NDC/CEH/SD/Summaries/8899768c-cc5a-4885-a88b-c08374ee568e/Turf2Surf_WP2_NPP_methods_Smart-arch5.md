# Site identification and plot location

- Purpose: A comprehensive field protocol to sample multiple habitats (grasslands, bogs/heaths, montane, woodlands) for ecosystem productivity (annual net primary production, aNPP) and related soil, tissue, and structural measurements.
- Habitats covered: grazed grasslands, unenclosed calcareous/acid grasslands, graminoid vegetation on bogs/heaths, montane heath, broadleaved woodlands, conifer plantations, dwarf shrub heath, Sphagnum moss patches, and pleurocarpous moss mats.
- Overall design approach:
  - Randomized plot placement within defined habitat patches to minimize trampling and ensure representativeness.
  - Use of fixed plot layouts (1x1 m subplots within larger master plots) and nested plots (e.g., 14.14x14.14 m in woodlands) to enable cross-site comparisons and linkage to existing survey frameworks (CS Bunce plots).
  - Exclosures used where grazing could bias measurements; marker canes or posts used to refind plots if exclosures are removed.
  - GPS references and sketch maps essential for locating plots across seasons and years.

- Data collection cadence:
  - Winter: plot location, quadrat setup, initial biomass cut (1 cm), exclosures added if grazed, photographic documentation, and biomass weighing.
  - Spring: post-livestock removal imaging and documentation; marker canes or posts placed to aid Summer re-finding.
  - Summer: peak biomass harvests; soil sampling; plant tissue (P and N) sampling; LICOR measurement of maximum photosynthetic rate; DBH measurements in woodland plots; litter and biomass sampling; exclosures reinstalled before stock returns.
  - Autumn: second cuts where applied (grasslands, moorland); biomass weighing and sampling; exclosures removed in some habitats.
  - Additional habitat-specific procedures: montane plots with hanging baskets; conifer leaf production estimates; Sphagnum productivity via cranked wires; Pleurocarpous moss productivity using mesh mats; litter bucket deployment and monthly collection; tree coring for annual wood increment.

- Plot and sub-plot structure:
  - Grazed and ungrazed grasslands: four plots per site, 1x1 m sub-plots cut to 1 cm, exclosures installed post-cut, GPS recorded, photos taken, weights recorded.
  - Unenclosed calcareous/acid grasslands: grid-based location rather than fixed boundaries; four plots per site with similar sub-plot layout and measurements.
  - Woodlands (Conwy/Bunce CS style): 14.14 m x 14.14 m nested plot; two 1x1 m sub-plots per plot; random sub-plot coordinates within the plot; additional components include DBH, saplings, litter buckets, and litter collection.
  - Sphagnum patches: five patches with three cranked wires per patch; density measures via microplots (10x10 cm).
  - Dwarf shrub heath: patches of differing age since last burn; three 1x1 m plots per patch with cutting to 1 cm; N and P tissue sampling; growth measurements.
  - Montane: six inverted hanging baskets (three of each montane heath type) with annual monitoring.

- Key data to collect (per plot/sub-plot where applicable):
  - Spatial/identification: site name, habitat type, plot number, sub-plot number, GPS coordinates, plot orientation (N-S), sketch map bearings and distances, photo numbers.
  - Temporal: dates of site visits, cutting events, exclosure installation/removal, and sampling events.
  - Biomass and mass: fresh mass per sub-plot harvest, grab sample mass, dry mass (Dgs) from dried grab samples, and weights to track productivity.
  - Soil and tissue: soil sampling, plant tissue sampling for phosphorus and nitrogen, LICOR measurements of photosynthetic rate.
  - Structural metrics: DBH and height for trees/shrubs, tree/shrub sapling counts, dominant species identification, canopy volume estimates (for leaf production in conifers), litter bucket contents.
  - Sphagnum/peat metrics: capitulum density, stem weight per unit length, wire-based growth increments, dry weights from harvested moss tissue.
  - Moss and bryophytes: Pleurocarpous moss productivity via moss mats under mesh, with weight-based productivity estimates.
  - Additional measurements: litter production estimates from leaves, bark and stem data where applicable, and annual woody mass increment calculations.

- Data quality and provenance:
  - Standardized protocols underpinning all habitats (e.g., CS procedures for vegetation census, standard methods for biomass cutting, sub-plot measurements, and sampling orders).
  - Consistent use of units (grams, kilograms, centimeters, meters) and clearly labeled sample bags with date, plot, sub-plot, and content.
  - Photographic records before and after cuts, and during key steps to document plot states and equipment placement.
  - Documentation of exclosure status and refinding aids for longitudinal consistency.
  - Tree-core analysis and annual increment calculations require careful lab processing (drying, mounting, sanding, and software-assisted ring-width analysis).

- Data management implications for Data Stewards:
  - Data models must accommodate multi-habitat, multi-season, and multi-method measurements within a single study framework.
  - Strong metadata and data dictionaries are essential to capture the complex plot designs (including nested plots, random coordinates, and exclosure statuses) and to enable cross-site comparability.
  - Provenance tracking should cover field workflows (location, dating, cutting, exclosure installation/removal, sampling), lab processing (drying, weighing, tissue analyses), and data transformations (aNPP calculations, DBH/LA measurements, leaf production estimates).
  - Data sharing should enable integration with external portals and existing CS/Bunce datasets, with consistent identifiers linking plots, sub-plots, samples, and lab results.
  - Quality assurance processes must verify measurement units, replicate counts, calibration of instruments (e.g., LICOR, scales), and correct linking of GPS coordinates to plot IDs.

- Key analytical components to support (highlights for data users):
  - Net primary production (aNPP) estimation using the formula:
    - aNPP = Dgs × (F1m / Fgs)
    - Dgs: dry mass from grab sample
    - F1m: fresh mass per 1 m2 harvest
    - Fgs: fresh mass of grab sample
  - Tree growth increment calculation framework (involving form factor, diameter at breast height, height, and wood density).
  - Crown leaf production estimates for conifer plantations using canopy measurements, branch sampling, and leaf mass per branch.

- Anticipated challenges relevant to data stewardship:
  - Incomplete or variable user needs across habitat types; need for harmonized data summaries across sites.
  - Data capture across many systems and formats (field sheets, lab logs, and electronic records) requiring careful integration.
  - Managing large data volumes from numerous plots across habitats and seasons, including high-volume images and lab results.
  - Ensuring robust re-findability of plots across years with exclosures and marker cane references, especially in unenclosed sites.
  - GPS accuracy limitations in some environments and potential procedural deviations (e.g., grid-based vs boundary-based plots).

- Suggested governance actions for ongoing data management:
  - Create a centralized data dictionary describing all variables, units, and codes for each habitat type and sampling event.
  - Establish standardized file naming conventions and version control for field sheets, lab results, and derived metrics (e.g., aNPP, DBH, leaf production).
  - Maintain explicit linkages between field IDs (site, plot, sub-plot) and laboratory results (tissue P/N, wood density, moss weights) to enable reproducible analyses.
  - Archive raw data (field measurements, weights, photos) with metadata and provide access controls and data sharing guidelines, including citation standards.
  - Develop templates for data entry that enforce validation rules (e.g., unit checks, plausible ranges, mandatory fields) to minimize labeling errors.
  - Ensure documentation is available for all species identifications, sampling methods, and any habitat-specific deviations from the core protocol.