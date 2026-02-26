# Experimental design

## Overview
- Study conducted in South West England across grassland, moorland, and woodland sites along a restoration gradient (intense/reference, restoring/creation, pristine).
- Purpose: provide habitat data suitable for map-based GIS analyses to understand restoration status and species presence.
- Data available as two CSV files linked by SiteID and LocationID.

## Study design and scope
- Site selection: three locations per site, one for each habitat type, within a 2 km radius, across multiple land-use contexts.
- Restoration gradient categories:
  - Reference (control)
  - Restoration/creation
  - Pristine
- Habitat types covered: Culm, Grassland, Heathland/moorland, Woodland/orchards, with category-specific definitions of reference/restoration/pristine.
- Spatial context: plots and options referenced to agri-environment scheme codes (e.g., HK7, HO4).

## Sampling regime
- Plot size: approximately 50 × 50 meters, representative of land-use type.
- Survey approach: zig-zag transect; sampling points ~25 m either side of central line.
- Vegetation data:
  - 5 quadrats per plot along the line; record percentage cover of vascular plants and bryophytes.
  - Abundance for the entire plot via the DAFOR scale.
- Sward (grass height) data:
  - Measured at five locations per plot using direct measure and drop-disc methods.
- Data collection: on paper forms, later entered into an Access database; outputs provided as CSVs.

## Data structure and content
- Data files:
  - SWHabitatData.csv: quadrat-level vegetation data.
  - SWSwardData.csv: sward height data.
- Linking keys: SiteID and LocationID.
- Key fields in SWHabitatData.csv:
  - SiteID, LocationID: identifiers for site and location/plot.
  - Option: agri-environment scheme option applied (e.g., HK7).
  - HabitatType: habitat category (e.g., arable, conifer, culm, grassland, heathland, orchard, woodland).
  - OptionType: position in restoration gradient (pristine, restoration, reference, creation).
  - SurveyDate: date of survey.
  - QuadratSize: size of quadrats.
  - SpeciesName: scientific name (sometimes genus-level) or bare ground.
  - Dafor: DAFOR score.
  - Cover1–Cover5: percent cover for five quadrats (0 if not present; blank indicates not recorded for that quadrat).
- Key fields in SWSwardData.csv:
  - SiteID, LocationID, Option, HabitatType, OptionType, SurveyDate.
  - Method: measurement method (direct or drop disc).
  - SwardHeight: height in cm.
- Data notes:
  - Some SiteIDs/LocationIDs are missing in one file (e.g., SiteID gaps; specific IDs not present in either file).
  - Species data may be incomplete or recorded at genus level; blank covers indicate absence in that quadrat.

## Data quality and caveats
- Collected by experienced botanical surveyors.
- Data verified for anomalies (e.g., cover > 100%) against original sheets and corrected.
- Cautions on interpretation:
  - Blank covers mean species not recorded in that quadrat; absence across entire plot not guaranteed.
  - Null Dafor entries indicate not recorded; species may be missed, especially at low abundance.

## Reuse, licensing, and citation
- Licensing: Open Government Licence (OGL).
- Citation: Peyton, J.; Nuttall, P.; Gerard, F.; Pywell, R.F. (2017). Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014. NERC Environmental Information Data Centre. https://doi.org/10.5285/110199cf-245e-4fa8-a9ca-386657b5fe20

## GIS implications and usage
- Enables map-based visualization of habitat type, restoration category, and species composition by SiteID/LocationID.
- Facilitates spatial analysis of restoration gradients, impact assessment, and integration with other environmental layers.
- Data can be joined with external datasets using SiteID/LocationID and Option/OptionType for themed maps (e.g., habitat change over gradient, sward height distribution).