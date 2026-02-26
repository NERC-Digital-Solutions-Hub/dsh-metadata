# Plant cover in foredunes following hurricane Irma: large scale surveys

## Overview
- Basic description: plant cover by species sampled on three occasions using 0.5 x 0.5 m quadrats along 3 transects at up to 28 sites in Florida and Georgia, USA, in foredune areas; hurricane Irma impacted coastline in Oct 2017.
- Study area: sites distributed between Cape Canaveral (Florida) and Tybee Island (Georgia), USA.
- Temporal coverage: sampling in February 2018, July 2018, and January 2019.
- Key metrics: plant percentage cover by species; average plant cover; species richness.

## Experimental design and sampling
- Site selection: February 2018 selection along the study coastline based on accessibility and permit considerations; aim to capture a mix of coastal development levels; sites undergoing active restoration re-surveyed.
- Transects and sampling: at each site, transects perpendicular to the shoreline positioned at ~50 m intervals; along each transect, observations at 1 m intervals from foredune crest to upper beach within a 0.5 x 0.5 m quadrat; estimate percentage cover for each plant species; total cover is the sum of all species’ covers; species richness is the number of species observed along a transect.
- Re-sampling: transects 1–3 at each site re-positioned within ~10 m for repeated surveys.
- Data checks: distributions screened for unusual values and cross-checked against field notebooks; NA indicates not applicable (sampling not conducted for that site/variable); 0 indicates absence of a species or zero species richness.

## Variables and data structure
- Observed variables: plant percentage cover by species; average plant cover; species richness.
- Dataset fields and coding:
  - Sampling_date: month and year of sampling.
  - Site: name of study site.
  - Lat, Long: latitude and longitude of site.
  - Transect: transect number.
  - Development: category of development with broad definitions:
    - A = low development: no development within ~1 km of foredune toe; mostly parks.
    - B = moderate development: no direct development within foredune/first swale; boardwalks or low-density housing on second/third dune ridges.
    - C = high development: buildings directly on the beach behind dune margins.
  - Number of species: count of species along the transect.
  - Total.cover: total plant cover along the transect.
  - Uniola_paniculata: mean cover of Uniola paniculata along the transect.
  - Other species: 67 additional species columns follow Uniola_paniculata.
- File formats: Excel and CSV.
- Dataset field descriptions: includes header and descriptive notes for each field.

## Spatial and data quality considerations for GIS
- Spatial components: site locations with Lat/Long; multiple transects per site enabling transect-level mapping and aggregation.
- Temporal components: three sampling dates across 2018–2019 for longitudinal analysis.
- QA/metadata: explicit data validation steps noted; clear handling of not-applicable and zero values.
- Compatibility for GIS workflows: data structured per transect with per-species cover allowing creation of species distribution rasters or vectors, as well as summary layers (e.g., total cover, species richness, dominant species like Uniola_paniculata).

## Usage notes and caveats
- Measurements are visual cover estimates within 0.5 x 0.5 m quadrats, which are suitable for map-based visualization and trend analyses but are not absolute abundances.
- Development category context enables spatial analyses across environmental gradients.
- Coordinate reference system is not specified; only lat/long are provided, which may require CRS specification for GIS integrations.
- The dataset is designed to support temporal comparison and species-specific mapping across foredune habitats affected by hurricane Irma.