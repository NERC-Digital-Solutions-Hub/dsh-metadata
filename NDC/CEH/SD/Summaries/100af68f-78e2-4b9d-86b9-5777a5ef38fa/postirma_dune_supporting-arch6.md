# Plant cover in foredunes following hurricane Irma: large scale surveys

## Overview
- Large-scale field survey of plant cover by species in foredunes affected by hurricane Irma (2017) along the Florida to Georgia coast (Cape Canaveral, FL to Tybee Island, GA).
- Temporal coverage: observations in February 2018, July 2018, and January 2019.
- Location and scope: up to 28 sites; field surveys conducted in foredune areas; sites selected for accessibility and a mix of coastal development levels.
- Personnel: John Griffin and Matthew Joyce.

## Data collection and design
- Sampling design: at each site, transects perpendicular to the shoreline positioned at ~50 m intervals; transects re-surveyed across time in roughly the same areas (within ~10 m) when possible.
- Sampling unit: 0.5 x 0.5 m quadrats along each transect; observations at 1 m intervals from the dune crest to the upper beach.
- Data collected per quadrat: plant species percentage cover (visually estimated); total cover is the sum of all species covers; species richness per transect.
- Variables observed: plant percentage cover by species, average plant cover, species richness.

## Data structure and metadata
- Key fields: sampling_date (month/year), site, latitude, longitude, transect, development category.
- Development categories with definitions: 
  - A: low development (e.g., parks; no development within ~1 km of foredune toe; small development within ~100 m of foredune)
  - B: moderate development (no direct development within foredune/first swale; boardwalks or low-density housing on second/third dune ridge)
  - C: high development (buildings directly on the beach behind dune margins)
- Observational details: transects 1–3 were used to represent each site; repeat surveys aimed to sample similar areas, though not always in every sampling round due to logistical reasons.
- Data quality notes: distributions screened for unusual values and cross-checked against field notebooks; NA indicates not applicable (sampling not conducted for that site-variable combination); 0 indicates absence of a species or zero species richness.
- Dataset description format: headers and descriptions included for each field; includes a note that there are 67 additional species columns beyond Uniola paniculata.

## Data formats and access
- Available in Excel and CSV formats.
- Key dataset fields include: Sampling_date, Site, Lat, Long, Transect, Development, Number of species recorded along the transect, Species.richness, Total.cover, Uniola_paniculata, and numerous other species columns.

## Potential uses and data products
- Ability to analyze spatial and temporal patterns in plant cover and species richness across sites with varying development levels.
- Potential to create dashboards or pivot-table summaries to enable self-serve exploration of species-specific and transect-level data.
- Use for trend analysis of foredune vegetation recovery or response to hurricane disturbance over time.

## Important considerations and limitations
- Some sites were not revisited in every sampling round due to logistical reasons; this results in incomplete time series for certain sites.
- Data are based on visual estimates of percent cover within 0.5 x 0.5 m quadrats, which may introduce observer variability.
- Data encompass a wide range of variables and numerous species columns, which may require careful data cleaning and consistent naming/alignment when merging with other datasets.