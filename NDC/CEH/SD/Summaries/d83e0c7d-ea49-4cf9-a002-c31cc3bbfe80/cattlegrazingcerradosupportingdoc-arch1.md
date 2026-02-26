# Data overview

- Study scope: Plant community data from 100 plots of 1 m² across ten old-growth Cerrado grasslands in São Félix do Tocantins, Tocantins, Brazil, collected in March–April 2022.
- Experimental design: 5 cattle-grazed and burned old-growth grasslands and 5 ungrazed and unburned old-growth grasslands; 10 plots per grassland (total of 100 plots). A 50-m transect per grassland with plots systematically distributed along the transect (10 plots per transect).
- Land-use categories: cattle-grazed and burned (denoted as grazed) vs ungrazed and unburned (denoted as ungrazed).
- Data collection timeline and context: Five grazed/burned and five ungrazed/unburned sites within a 1,000-hectare area; climate and soil context described (dry winter, humid summer; arenosol soil; altitude ~500 m).
- Treatments and history: Traditional cattle ranching with burning before grazing; grazed sites had ~0.3 Nelore animals per hectare at sampling; unburned sites protected from fire for 14 years; no prior soil management or invasions by African grasses.

- Vegetation sampling protocol:
  - Within each plot, record all plant species, growth form (graminoids, forbs, shrubs), and estimate percent cover.
  - A nested subplot (0.5 m × 0.5 m) used to collect aboveground biomass and litter, partitioned into graminoid, forb, shrub, and dead biomass; dried at 80°C for 48 h and weighed (g m⁻²).
  - Cover estimates are 0–100% per species; total plot cover may exceed 100% due to 3D structure.
  - Data captured for all plots along the transects, plus site-level averages.

- Data files and structure:
  - CattleGrazingCerrado1.txt: 100 rows (plots) with plot-level diversity and structure variables.
    - Key columns: site, land_use, plot, total_richness, shrub_richness, graminoid_richness, forb_richness, shrub_cover, graminoid_cover, forb_cover, dead_biomass_cover, bare_ground, shrub_biomass, graminoid_biomass, forb_biomass, dead_biomass.
  - CattleGrazingCerrado2.txt: site-level average abundance (cover) for 118 species; rows = sites, columns = species; zeros indicate absence.
  - CattleGrazingCerrado3.txt: geographic coordinates (lat/long) of the old-growth grasslands (sites).
- Variables and measurements:
  - Diversity metrics per 1 m² plug: total_richness, graminoid_richness, forb_richness, shrub_richness.
  - Cover metrics per 1 m² plot: shrub_cover, graminoid_cover, forb_cover, dead_biomass_cover, bare_ground.
  - Biomass metrics (g m⁻²): shrub_biomass, graminoid_biomass, forb_biomass, dead_biomass.
  - Species abundance: site-level average cover for 118 species (CattleGrazingCerrado2).
- Spatial and sampling scale:
  - 10 old-growth grasslands × 10 plots per grassland = 100 plots total; each plot 1 m².
  - Transects oriented north-south; GPS provides precise site locations (as per CattleGrazingCerrado3.txt).

- Methodological notes:
  - Growth forms used for categorization: graminoids, forbs, shrubs (woody lianas and palms within shrub category).
  - Biomass conversion: from 0.25 m² subplots to per m² basis; biomass measured with high precision.
  - Data are intended to support analyses of how grazing and fire management influence plant diversity, structure, and biomass, enabling correlation and predictive modelling.

- Funding and provenance:
  - Data from two projects: ecological/economic evaluation of beef cattle on Cerrado pastures (FAPESP grant 2020/04713-5) and adaptive management of invasive species (NERC grant NE/S011641/1).

- Practical considerations for analysts:
  - Suitable for cross-site comparisons of land-use effects on diversity and biomass.
  - Enables modeling of relationships between plot-level diversity/biomass and site-level species composition.
  - Metadata-rich with explicit data structure; facilitates reproducibility and data sharing.