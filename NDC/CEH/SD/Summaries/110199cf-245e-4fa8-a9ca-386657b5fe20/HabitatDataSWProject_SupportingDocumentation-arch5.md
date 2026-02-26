# Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014

- Purpose: Document experimental design, data collection, structure, and licensing for habitat data across restoration gradients in South West England to support discovery, reuse, and governance of the dataset.
- Stewardship context: Data are provided under Open Government Licence and accompanied by a formal citation; the dataset is organized to be discoverable and usable by researchers, with clear identifiers, metadata, and linkage between files.

## Study area and design

- Location: South West England.
- Gradient and habitat types: Grassland, heathland/moorland, woodland/orchard, representing a restoration gradient from reference (intense land use) through restoration/creation to pristine conditions.
- Site selection: For each habitat type, three locations within a 2 km radius were chosen to form a consistent restoration gradient.
- Plot size and sampling frame: Approximately 50 × 50 meters per plot; a zig-zag survey line with points about 25 m from the central line; five quadrats per plot along the line to assess vascular plants and bryophytes.
- Measurements captured: Percent cover (vascular plants and bryophytes) in quadrats (5 per plot) and sward height using two methods (direct measurement and drop disc).

## Data collected and structure

- Data files:
  - SWHabitatData.csv: Quadrat data (species names, DAFOR scores, cover percentages across five quadrats).
  - SWSwardData.csv: Sward height data (five measurements per plot; method used).
- Linkage: Both files connect via SiteID and LocationID.
- Key fields (highlights):
  - SiteID: Unique site identifier (1–130; note some gaps, e.g., no SiteID 39 in habitat data).
  - LocationID: Unique location/plot identifier (2–150; some gaps, e.g., no LocationID 18, 32, 88, 121 in habitat data).
  - Option: Agri-environment scheme code (e.g., HK7 for “Restoration of species-rich grass”).
  - HabitatType: Habitat category (arable, conifer, culm, grassland, heathland, orchard, woodland).
  - OptionType: Position in the restoration gradient (pristine, restoration, reference, or creation).
  - SurveyDate: Date of survey.
  - QuadratSize: Quadrat dimensions (meters).
  - SpeciesName: Scientific name (or genus level when unresolved); includes bare ground.
  - Dafor: DAFOR abundance score (text).
  - Cover1–Cover5: Percentage cover in five quadrats (percent; blank = not recorded or not present).
  - SwardHeight: Height measurement in cm.
  - Method: Sward height recording method (direct measure or drop disc).
- Data types and units: Explicit descriptions provided for each column; units include percent for cover, cm for height, and meters for quadrat size.

## Data quality, provenance, and validation

- Collected by experienced botanical surveyors to ensure accurate percent covers and species identifications.
- Quality checks included validation of anomalous values (e.g., covers >100%), cross-checks against original recording sheets, and corrections where needed.
- Data interpretation notes:
  - Nulls in DAFOR should be treated with caution and not automatically interpreted as absence across the plot, as rare or missed occurrences are possible.
  - Some systemic gaps exist in the dataset (e.g., missing SiteIDs/LocationIDs listed above), which should be accounted for in analyses and metadata.

## Data governance, access, and reuse

- Licensing: Open Government Licence (OGL) for data reuse.
- Citation requirements: Please cite Peyton et al. (2017) when using the dataset:
  Peyton, J.; Nuttall, P.; Gerard, F.; Pywell, R.F. (2017). Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014. NERC Environmental Information Data Centre. https://doi.org/10.5285/110199cf-245e-4fa8-a9ca-386657b5fe20
- Publication and hosting: Data are provided in two CSV files with clear documentation of fields, data types, and provenance; suitable for ingestion into standard data repositories and catalogues.
- Stewardship notes:
  - The dataset is prepared to support data discovery and reuse, with defined data types, units, and cross-file linking.
  - Potential updates would require systems in place for updating both files and their linkage, respecting sharing limitations.

## Practical considerations for Data Stewards

- Ensure ongoing data governance by maintaining the SiteID and LocationID mappings and clarifying any future updates or corrections.
- Preserve metadata integrity, including the Option, HabitatType, and OptionType fields, to preserve interpretability of restoration gradients.
- Track and communicate any known data gaps (e.g., missing IDs) to data users and include these caveats in data catalogs and READMEs.
- Provide or maintain tools to validate that DAFOR entries and cover percentages are used consistently across users and analyses.

## Known limitations and caveats

- Some SiteIDs and LocationIDs are missing in the provided files; users should account for these gaps in analyses and reporting.
- DAFOR values may be missing in some records; treat missing values with caution.
- The dataset covers surveys conducted in 2014 within a specific region (South West England); extrapolation beyond these contexts should be done carefully.

## Summary for discovery and use

- Two linked CSV files provide a comprehensive record of plant community composition and sward structure across a restoration gradient in grassland, moorland, and woodland habitats.
- Data are carefully curated, quality checked, and licensed for open reuse, with clear attribution guidance.
- The dataset supports analyses of restoration outcomes, biodiversity targets, and habitat management effectiveness, and is suitable for integration into broader data governance and stewardship workflows.