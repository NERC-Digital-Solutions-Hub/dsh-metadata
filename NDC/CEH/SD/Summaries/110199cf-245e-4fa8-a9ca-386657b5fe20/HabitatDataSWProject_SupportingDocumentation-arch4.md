# Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014

## Aim and scope
- Documents habitat restoration data collected across grassland, moorland/heathland, culm, and woodland/orchard types in South West England during 2014.
- Experimental design follows a restoration gradient with three habitat locations per site within a 2 km radius, covering reference (intense/controls), restoration/creation, and pristine conditions.
- Each habitat type is defined by a specific set of reference/restoration/pristine criteria per habitat.

## Experimental design
- For each site, three locations (one per habitat type) within 2 km radius.
- Restoration gradient categories defined per habitat (reference, restoration/creation, pristine) with codes such as HK7 (example) referring to agri-environment scheme options.
- Plots: approximately 50×50 m representative of land-use type (intensive, restoring, pristine).
- Sampling along a zig-zag transect with five quadrats per plot to assess plant cover (vascular plants and bryophytes) and DAFOR abundance scoring.
- Sward height measured at five locations per plot using two methods: direct measure and drop disc.

## Sampling regime
- Data collected via a 50×50 m plot with five quadrats along a transect; percentage cover recorded for vascular plants and bryophytes in each quadrat.
- Abundance across the whole plot recorded using DAFOR scale.
- Sward height measured at five locations per plot by direct measurement and by drop-disc method.
- Data captured on paper forms and later entered into an Access database using a purpose-built form.

## Data structure and contents
- Two CSV files:
  - SWHabitatData.csv: quadrat-level data
  - SWSwardData.csv: sward height data
- Linking keys: SiteID and LocationID (shared between files).
- SWHabitatData.csv columns include: SiteID, LocationID, Option, HabitatType, OptionType, SurveyDate, QuadratSize, SpeciesName, Dafor, Cover1-5, etc.
- SWSwardData.csv columns include: SiteID, LocationID, Option, HabitatType, OptionType, SurveyDate, Method, SwardHeight.
- Data coding:
  - Option reflects restoration actions (often an agri-environment scheme code like HK7).
  - HabitatType includes arable, conifer, culm, grassland, heathland, orchard, woodland.
  - OptionType indicates position in the restoration gradient: pristine, restoration, reference, or creation.
- Data completeness notes:
  - SiteID runs 1–130 (SiteID 39 absent in habitat data).
  - LocationID runs 2–150 (some IDs missing in both datasets).
  - Some SiteID/LocationID combinations have no data for certain fields.

## Nature and units of recorded values
- Quadrat data (SWHabitatData.csv):
  - Cover1-5: percentage cover per quadrat (0–100%); blank indicates absence in that quadrat.
  - Dafor: categorical abundance score; null in some cells (may indicate not recorded or missed occurrences).
  - SpeciesName: taxon name (sometimes genus-level) or bare ground; QuadratSize noted in metres.
- Sward data (SWSwardData.csv):
  - SwardHeight: height in centimetres.
  - Method: recording method (direct measure or drop disc).

## Quality control and provenance
- Survey conducted by experienced botanical surveyors.
- Data checked for anomalies (e.g., cover >100%), cross-checked against original sheets, and corrected as needed.
- Nulls in DAFOR treated with caution, as missed detections possible.

## Licensing, reuse and citation
- Licensed under the Open Government Licence (OGL).
- Please cite: Peyton, J.; Nuttall, P.; Gerard, F.; Pywell, R.F. (2017). Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014. NERC Environmental Information Data Centre. https://doi.org/10.5285/110199cf-245e-4fa8-a9ca-386657b5fe20

## Notes for data leaders
- The dataset provides a structured, linkable two-file schema (habitat quadrats and sward measurements) suitable for cross-site comparisons and integration with other datasets via SiteID/LocationID.
- Metadata clarity around options and restoration gradient positions supports cross-site harmonization and re-use in policy or planning contexts.
- Useful for evaluating restoration outcomes, identifying data gaps, and informing data governance around ecological monitoring programs.