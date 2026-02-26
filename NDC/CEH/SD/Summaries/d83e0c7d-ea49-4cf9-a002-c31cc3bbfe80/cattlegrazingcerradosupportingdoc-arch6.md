# Data overview

- Scope
  - Plant community data from 100 plots (1 m² each) across 10 old-growth grasslands in São Félix do Tocantins, Tocantins, Brazil.
  - Comparison between 50 plots in cattle-grazed and burned old-growth grasslands and 50 plots in ungrazed and unburned old-growth grasslands.
  - Sampling conducted in March–April 2022; old-growth grasslands historically burned and grazed on a 2-year cycle.

- Study context and funding
  - Integrated across two projects: ecological/economic evaluation of beef cattle on Cerrado pastures and adaptive management of invasive species.
  - Funded by Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP, Grant 2020/04713-5) and Natural Environment Research Council (NERC, Grant NE/S011641/1).

- Sampling design and field methods
  - Each old-growth grassland has a 50-m transect with 10 plots (1 m × 1 m) along the transect.
  - Within each plot: identification of all plant species, growth form (graminoids, forbs, shrubs), and visual cover (%). Dead biomass and bare ground also estimated.
  - A 0.5 m × 0.5 m subplot used to collect aboveground biomass and litter, sorted into graminoid, forb, shrub, and dead biomass; dried at 80°C for 48 hours and weighed (g m⁻², converted from g per 0.25 m²).
  - Species identifications supported by specialists/herbarium when needed.

- Data structure and files
  - CattleGrazingCerrado1.txt
    - 100 rows (plots); 15 columns with site-level and plot-level metrics.
    - Key columns: site, land_use (grazed or ungrazed), plot, total_richness, shrub_richness, graminoid_richness, forb_richness, shrub_cover, graminoid_cover, forb_cover, dead_biomass_cover, bare_ground, shrub_biomass, graminoid_biomass, forb_biomass, dead_biomass.
  - CattleGrazingCerrado2.txt
    - 10 rows (sites) × 118 species, tab-delimited; average cover per site for each species.
    - Zeros indicate absence of a species at a site.
  - CattleGrazingCerrado3.txt
    - Latitude/longitude coordinates for the 10 old-growth grasslands (location data).

- Variables and measurements
  - Diversity and structure: total_richness, shrub_richness, graminoid_richness, forb_richness (species per 1 m²).
  - Cover: shrub_cover, graminoid_cover, forb_cover, dead_biomass_cover, bare_ground (percent).
  - Biomass: shrub_biomass, graminoid_biomass, forb_biomass, dead_biomass (g m⁻²).
  - Composition by site: average species cover across 10 plots per site; presence/absence implied by zero values.

- Data provenance and quality
  - Field identifications validated via specialist consultation and herbarium references.
  - Biomass measured with high precision (0.1 mg precision) and standardized to g m⁻².
  - Data compiled from two main projects; linkage through 100 plots, 10 sites, and 10 transects.
  - Spatial context provided by separate location file (CattleGrazingCerrado3.txt).

- Potential uses and data products
  - Compare plant community structure and biomass between grazed/burned vs. ungrazed/unburned grasslands.
  - Analyze species richness by growth form and cover/biomass distributions.
  - Integrate species abundance per site with plot-level metrics for regional assessments.
  - Create self-serve dashboards or reports; map sites using coordinates in CattleGrazingCerrado3.txt.
  - Support policy and management decisions in Cerrado grassland ecosystems and cattle management practices.

- Formats and access
  - All three files are tab-delimited text files with clearly described headers and units.
  - Supplementary metadata embedded in the variable names and descriptions (e.g., units and interpretation of zero values).