# Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014

## Aim and scope
- Document experimental design and methods for habitat data collected along restoration gradients (intense/reference, restoration/creation, pristine).
- Cover grassland, heathland/moorland, and woodland/orchard habitats within South West England.
- Data intended for monitoring environmental health and informing policy-relevant assessments over time.

## Experimental design
- Sites selected where three locations (one per habitat type) fall within a 2 km radius, all within South West England.
- Restoration gradient categories defined per habitat (e.g., reference/intense, restoration/creation, pristine) with specific option codes (e.g., HK7, HO4, HC9/10, HC7, etc.).
- Habitat types and restoration options are encoded to allow standardized comparisons across sites and time.

## Sampling regime
- Sampling area: approximately 50 × 50 meters per plot, representative of land-use type (intensive, restoring, pristine).
- Survey method: zig-zag transect; five quadrats along the line to record:
  - Percentage cover of vascular plants and bryophytes by species (in each quadrat).
  - DAFOR abundance rating for species across the entire 50 × 50 m plot.
- Sward height: measured at five locations per plot using two methods:
  - Direct measurement with a ruler.
  - Drop disc method (disc height above ground).
- Data collection then transcribed from paper forms into an Access database and exported as CSV outputs.

## Data structure and contents
- Two CSV files:
  - SWHabitatData.csv: quadrat-level data.
  - SWSwardData.csv: sward height data.
- Linking keys: SiteID and LocationID connect the two files.
- Key fields in SWHabitatData.csv include:
  - SiteID, LocationID, Option, HabitatType, OptionType, SurveyDate, QuadratSize, SpeciesName, Dafor, Cover1–Cover5.
- Key fields in SWSwardData.csv include:
  - SiteID, LocationID, Option, HabitatType, OptionType, SurveyDate, Method, SwardHeight.
- Units and data types:
  - QuadratSize: metres; SwardHeight: cm; Cover: percentage; SurveyDate: date; Dafor: categorical; others: text or numeric as described.
- Data caveats:
  - Some SiteID and LocationID values are missing in the two files (e.g., SiteID gaps; certain LocationID gaps) and some IDs are absent in the sward dataset.

## Quality control
- Data collected by experienced botanical surveyors to ensure accuracy in percent cover and species identifications.
- Automated checks for anomalies (e.g., cover > 100%) and cross-checks against original recording sheets, followed by corrections as needed.

## Data reuse and citation information
- Licensing: Open Government Licence (OGL).
- Citation: Peyton, J.; Nuttall, P.; Gerard, F.; Pywell, R.F. (2017). Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014. NERC Environmental Information Data Centre. https://doi.org/10.5285/110199cf-245e-4fa8-a9ca-386657b5fe20

## Relevance for environmental monitoring and policy evaluation
- Enables standardized assessment of habitat restoration outcomes across multiple habitat types and gradients.
- Supports aggregation by option type and habitat, facilitating temporal comparisons and evidence-based policy performance analysis.
- Data are structured for integration into monitoring portals and reuse under open licensing.