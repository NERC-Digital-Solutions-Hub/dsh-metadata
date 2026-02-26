# Data overview

- The dataset comprises plant community data from 100 plots (1-m² each) across five cattle-grazed and burned old-growth grasslands and five ungrazed and unburned old-growth grasslands in the northern Cerrado, São Félix do Tocantins, Tocantins, Brazil, collected in March–April 2022.
- Data are linked to two projects: ecological/economic evaluation of beef cattle on Cerrado pastures (FAPESP) and adaptive management of invasive species (NERC).
- Data are organized into three tab-delimited files: CattleGrazingCerrado1.txt, CattleGrazingCerrado2.txt, and CattleGrazingCerrado3.txt.

## Data files and contents

- CattleGrazingCerrado1.txt
  - Per-plot data for 100 sampling plots.
  - Columns include: site, land_use, plot, total_richness, shrub_richness, graminoid_richness, forb_richness, shrub_cover, graminoid_cover, forb_cover, dead_biomass_cover, bare_ground, shrub_biomass, graminoid_biomass, forb_biomass, dead_biomass.
  - Land use is described at the site level (grazed vs ungrazed; file notes “grazed” in this file and “ungrazed” in the other but both represent site types).
  - Units: richness in species per 1 m²; cover in percent (%); biomass in g m⁻².
- CattleGrazingCerrado2.txt
  - Per-site (per old-growth grassland) average cover for each of 118 plant species.
  - Rows = sites; columns = species; values = average cover (%) per site (zero indicates absence).
- CattleGrazingCerrado3.txt
  - Spatial locations (latitudes and longitudes) of the 10 old-growth grassland sites.

## Study area and sampling design

- Location: northern Cerrado, Tocantins state, Brazil; municipality of São Félix do Tocantins.
- Climate and environment: dry winter (May–Sept) and humid summer (Oct–Apr); annual rainfall ~1,400–1,500 mm; average altitude ~500 m; predominantly arenosol soils; flat relief.
- Plot design: within each old-growth grassland site, a 50-m North-South transect with 10 plots (1 m × 1 m) at regular intervals.
- Vegetation sampling within plots: all plant species recorded with growth form (graminoids, forbs, shrubs) and visual percent cover; dead biomass and bare ground recorded.
- Biomass sampling within each plot: a 0.5 m × 0.5 m subplot collected aboveground vegetation; biomass separated into graminoid, forb, shrub, and dead biomass; dried at 80°C for 48 hours and weighed; results converted to g m⁻².
- Temporal coverage: data collected in March–April 2022.

## Variables and data structure

- Plot-level data (CattleGrazingCerrado1.txt) include site, land_use, plot, diversity metrics (total_richness, shrub/graminoid/forb_richness), cover metrics (shrub/graminoid/forb_cover, dead_biomass_cover, bare_ground), and biomass metrics (shrub/graminoid/forb/dead_biomass).
- Site-level species abundance data (CattleGrazingCerrado2.txt) provide the average cover for 118 species per site.
- Spatial data (CattleGrazingCerrado3.txt) provide geolocations for each old-growth grassland site, enabling GIS mapping and spatial joins with plot data.
- Notable data characteristics:
  - Total vegetation cover in a 1-m² plot may exceed 100% due to vertical structure.
  - Zero values in species cover indicate absence at a site.
  - Growth forms: graminoids, forbs, and shrubs (woody lianas and palms categorized accordingly).

## Spatial and temporal readiness for GIS

- Spatial components: site-level coordinates (lat/long) enable mapping of old-growth grassland locations and spatial analysis of grazing vs. ungrazed treatments.
- Temporal component: one-time sampling window (March–April 2022); suitable for cross-site comparisons within this period.
- Data are provided as tab-delimited text files with explicit variable names and units, facilitating ingestion into GIS workflows and subsequent visualization (e.g., thematic maps of richness, cover, and biomass).

## Data processing, units, and provenance

- Derived metrics calculated from plot data include multiple richness, cover, and biomass measures at 1-m² plot scale.
- Biomass values are converted to grams per square meter (g m⁻²) after drying soil-subplot samples.
- Site-level species abundances (average cover per species per site) are provided separately for broader spatial analyses.
- Provenance: data collected as part of two funded projects; materials and identification were validated via field collection and herbarium consultations as needed.

## Data quality, scope, and limitations

- Field identifications underwent follow-up with specialists; some identifications were pending at collection time.
- The dataset focuses on 10 old-growth grasslands (5 grazed/burned, 5 ungrazed/unburned) with 10 plots per site, yielding 100 plots total; spatial resolution is at the plot level within each site.
- Potential considerations for GIS use:
  - Coordinate accuracy depends on GPS logging in field; ensure coordinate reference system is interpreted correctly when integrating with other layers.
  - Some variables may have missing values or require careful handling of zero-absence data in species covers.

## Potential GIS applications and considerations

- Map-based visualization of spatial patterns in richness, cover, and biomass across grazed vs ungrazed sites.
- Spatial comparison of plant community structure and composition among old-growth grasslands in Tocantins.
- Integration with environmental layers (soil type, altitude, climate) to analyze drivers of community differences.
- Suitability for multi-layer analyses: per-plot attributes (from CattleGrazingCerrado1.txt) and per-site species averages (CattleGrazingCerrado2.txt) can be joined via site identifiers.
- Caution regarding units and interpretation when aggregating plot-level data to site or landscape scales.