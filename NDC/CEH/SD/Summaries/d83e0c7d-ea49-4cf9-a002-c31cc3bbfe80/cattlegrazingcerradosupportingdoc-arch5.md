# CattleGrazingCerrado Plant Community Data

## Overview
- Plant community data collected from 100 plots (1 m²) across 10 old-growth grasslands in the northern Cerrado, Tocantins, Brazil, March–April 2022.
- Comparison between 50 plots from cattle-grazed and burned grasslands and 50 plots from ungrazed and unburned grasslands.
- Data assembled from two funded projects and compiled into three data files describing plot-level diversity/structure, site-level species abundance, and site locations.

## Data collection and sampling design
- Study area: 1,000 hectares in São Félix do Tocantins; average altitude ~500 m; dry winters and humid summers; arenosol soil; long history of fire-grazing management.
- Sampling design: 10 old-growth grasslands (five grazed/burned and five ungrazed/unburned); within each grassland, a 50 m transect with 10 plots (1 m × 1 m) along the transect.
- Within each 1 m² plot:
  - All plant species recorded, growth form classified (graminoids, forbs, shrubs).
  - Species cover estimated (%); dead biomass cover and bare ground estimated.
  - A 0.5 m × 0.5 m subplot harvested for aboveground biomass; biomass separated into graminoid, forb, shrub, and dead biomass, dried (80°C, 48 h) and weighed (g m⁻²; converted to g m⁻² for 1 m²).
- Data processing:
  - Derived variables include total, graminoid, forb, and shrub richness per plot; cover by growth form; dead biomass and bare ground; and biomass per growth form.
  - Site-level species abundance: average cover of 118 species per site across 10 plots (zeros indicate absence).

## Data files and structure
- CattleGrazingCerrado1.txt
  - 100 rows (plots) and columns for sample identifiers and plant community variables.
  - Key columns: site, land_use, plot, total_richness, shrub_richness, graminoid_richness, forb_richness, shrub_cover, graminoid_cover, forb_cover, dead_biomass_cover, bare_ground, shrub_biomass, graminoid_biomass, forb_biomass, dead_biomass.
- CattleGrazingCerrado2.txt
  - Rows correspond to sites; columns correspond to average cover for each of 118 recorded species.
  - Zeros indicate species absence at a site.
- CattleGrazingCerrado3.txt
  - Geographic coordinates (lat/long) for each old-growth grassland site.

## Variables and units
- Richness: species per 1 m² (total, graminoid, forb, shrub).
- Cover: percentage (%) for shrub, graminoid, forb, dead biomass; bare ground in percentage.
- Biomass: grams per square meter (g m⁻²) for shrub, graminoid, forb, dead biomass.
- Composition and structure: per-plot values plus site-level mean covers for species.

## Site context and logistics
- Grasslands:
  - Five grazed and burned; five ungrazed and unburned old-growth sites (ten plots per site).
  - Long-term land-use history includes burning after the dry season to facilitate cattle grazing (Sept fire; grazing Oct–Apr).
- Site attributes:
  - 1,000 hectares total; average climate and soil context provided (arenosol soil; flat relief).
  - Grazing intensity at sampling: ~0.3 Nelore per hectare (grazed/burned sites).
  - Ungrazed sites protected from fire for 14 years; no prior soil management or cultivation.
- Location data:
  - Coordinates of the grasslands provided in CattleGrazingCerrado3.txt.

## Provenance and funding
- Projects:
  - Ecological and economic evaluation of beef cattle on Cerrado pastures.
  - Optimising long-term management of invasive species using adaptive management.
- Funders:
  - Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP) grant 2020/04713-5.
  - Natural Environment Research Council (NERC) grant NE/S011641/1.

## Data quality and processing
- Field identifications supported by specialists and herbarium consultations; some identifications may require lab confirmation.
- Note: total plot cover may exceed 100% due to 3D plant structure.
- No soil management or cultivation reported prior to sampling; all sites were free from African grasses invasions.
- Data organized with explicit site/plot identifiers and clear, explicit variable definitions to support interoperability.

## Data governance and reuse
- Data are organized into clearly documented, machine-readable text files with defined units and descriptions for metadata consistency.
- Useful for meta-analyses or cross-site comparisons of vegetation responses to grazing and fire regimes in Cerrado old-growth grasslands.
- Users should align data across files by site and plot; site-level abundance complements plot-level richness and cover data.

## Key stewardship considerations
- Maintain alignment of site codes across the three files; ensure correct interpretation of land_use labels (grazed vs. ungrazed) consistent with the dataset description.
- Preserve measurement methods (biomass drying protocol, cover estimation approach) to ensure comparability with related datasets.
- Provide clear licensing and data access terms to facilitate reuse and attribution. Consider adding metadata fields for data provenance, collection personnel, and data validation status if expanding the dataset.