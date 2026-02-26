# Introduction

- Study sample: 51 sites across three CAZ zones in Madagascar; measurements and samples taken at five locations along ~60 m transects, from upslope (location 1) to downslope (location 5); samples collected at surface and 2 depths below surface; soil texture samples combined per depth per transect.
- Data completeness: missing data represented as NaN; file describes data collection methods and data contents.

## Spatial and land-use metadata

- Transect number: used by P4GES hydrology team for all measurements and samples.
- ZOI (zone of interest): study region designation in P4GES.
- Land use classification: six categories based on dominant species and owner interviews (CC: closed canopy forest; RF: reforestation; TSA: tree fallow; SSA: shrub fallow; TM: degraded grassland; EUC: eucalyptus plantation).
- Site naming: site location name linked to transect and land use; P4GES site name provided for cross-dataset comparison.
- Soil description: brief, field-based texture notes (rough estimates; recommended to use text data for texture).
- Dominant species: names of predominant vegetation.
- Site description: average slope aspect and angle for the site and transect.

## Measurement locations and coordinates

- Sample locations: five points per transect with specific latitude, longitude, and local slope for each point (1–5); coordinates in decimal degrees, WGS84; slope measured with an inclinometer.
- Some transects (16–18, 22, 31–44) had slope measurements between sample points.

## Soil hydraulic conductivity (Ksat)

- Ksat at surface (0–10 cm): measured with a double-ring infiltrometer (inner ring 15 cm); depth of ponding 10–20 cm; Ksat calculated from steady-state infiltration rate; data provided per point (1–5) plus site-level statistics (average, median, standard deviation).
- Ksat at depth (10–20 cm and 20–30 cm): measured with an Amoozemeter (constant head permeameter); Ksat calculated from steady-state rate; per-point values with site statistics.

## Soil texture and sampling handling

- Soil texture: collected at 2.5–7.5 cm, 12.5–17.5 cm, and 22.5–27.5 cm; bulk sample per depth per transect; stored in airtight bags; analyzed at VU University (Netherlands) using Helium-Neon Laser Optical System; transects 55–57 analyzed at the University of Zürich using sieving and Sedigraph.
- For transects 1–10, bulk samples from 12.5–17.5 cm and 22.5–27.5 cm were combined before analysis.

## Other soil hydrological characteristics

- Undisturbed soil core (100 cm³) collected at each measurement location at the three depth bands; measurements taken immediately after sampling, after 5 days of saturation, after 3 days of gravity drainage, and after oven drying at 105°C for 24 h.
- Variables calculated per sample and per site: porosity, moisture content at field capacity, and bulk density.

## Calculations and derived metrics

- Bulk density: dry weight divided by 100 cm³ volume.
- Porosity: based on saturated weight, dry weight, water density, and 100 cm³ volume.
- Moisture content at field capacity: based on drainage weight difference and dry weight, normalized by water density and volume.

## Data quality, structure, and provenance

- Data organization includes per-point (1–5) and per-site statistics (mean, median, std) for Ksat and other properties.
- Data missingness indicated by NaN; units specified for each measurement (e.g., Ksat in mm/hr).
- Provenance notes: laboratory analyses differ by transect group (VU Netherlands vs. University of Zürich) for texture data; references to standard methods and prior publications for details (Styger et al. 2007; Zwartendijk et al. 2017).

## References

- Styger E, Rakotondramasy HM, Pfeffer MJ, Fernandes ECM, Bates DM. 2007. Influence of slash-andburn farming practices on fallow succession and land degradation in the rainforest region of Madagascar. Agriculture, Ecosystems & Environment, 119:257-269.
- Zwartendijk BW, van Meerveld HJ, Ghimire CP, Bruijnzeel LA, Ravelona M, Jones JPG. 2017. Rebuilding soil hydrological functioning after swidden agriculture in eastern Madagascar. Agriculture, Ecosystems & Environment, 239:101-111.