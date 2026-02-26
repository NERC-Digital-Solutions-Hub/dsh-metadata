# Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014

## Overview
- Dataset from habitat surveys across grassland, moorland, and woodland sites in South West England, spanning a restoration gradient (intense/reference, restoration/creation, pristine).
- Each gradient location includes three habitat types within a 2 km radius; data collected in 2014.
- Data designed to support analysis of restoration outcomes and habitat management, with outputs suitable for dashboards, reports, and further data products.

## Experimental design
- For each restoration gradient and habitat type, three locations were selected within 2 km of each other in South West England.
- The restoration gradient definitions:
  - Reference (control/intense), Restoration/Creation, Pristine.
  - Habitat-specific examples include culm, grassland, heathland/moorland, and woodland/orchards with defined options.
- Options (e.g., HK7: Restoration of species-rich grass) denote the specific management/restoration treatment applied to each plot.

## Sampling regime
- Plots: approximately 50 × 50 m representative of the land-use type.
- Survey method: zig-zag walk with five quadrats along the central line, each approximately 25 m apart.
- Data collected per quadrat: percentage cover of vascular plants and bryophytes, using five quadrats per plot; abundance across the full plot recorded using the DAFOR scale.
- Sward height: measured at five locations per plot using two methods—direct measure and drop disc.
- Data collection media: paper forms, later entered into an Access database; outputs provided as two CSV files.

## Data structure and files
- Two linked CSV data files:
  - SWHabitatData.csv: quadrat-level habitat data (species, cover, DAFOR, etc.).
  - SWSwardData.csv: sward height data (method, height in cm).
- Linkage: both files connect via SiteID and LocationID.
- Site and location identifiers:
  - SiteID runs sequentially from 1 to 130 (note: SiteID 39 is absent in habitat data).
  - LocationID runs sequentially from 2 to 150 (note: LocationID 18, 32, 88, 121 absent in habitat data; 31, 39, 65, 89 absent in sward data).

## Nature and units of recorded values
- SWHabitatData.csv columns include: SiteID, LocationID, Option, HabitatType, OptionType (pristine/restoration/reference/creation), SurveyDate, QuadratSize (m), SpeciesName, Dafor, Cover1–Cover5 (%).
- SWSwardData.csv columns include: SiteID, LocationID, Option, HabitatType, OptionType, SurveyDate, Method (direct/drop disc), SwardHeight (cm).
- Data notes:
  - Missing covers indicate species not present in that quadrat.
  - Null DAFOR values indicate not recorded; interpret with caution as species may be missed.
  - SpeciesName may be species-level or genus-level identifications; some bare ground entries are included.

## Data quality and provenance
- Survey conducted by experienced botanical surveyors to ensure accuracy in percentage cover and species ID.
- Data checks included validation for anomalous values (e.g., covers > 100%), cross-checks with original sheets, and corrections as needed.

## Reuse, citation, and licensing
- Licensed under the Open Government Licence (OGL).
- Citation recommended:
  Peyton, J.; Nuttall, P.; Gerard, F.; Pywell, R.F. (2017). Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014. NERC Environmental Information Data Centre. https://doi.org/10.5285/110199cf-245e-4fa8-a9ca-386657b5fe20
- Data are provided by CEH/NERC Environmental Information Data Centre; suitable for inclusion in data products and broader analyses.

## Known data gaps and limitations
- Some SiteID and LocationID values are missing in the respective data files (e.g., SiteID 39 in habitat data; SiteID 31, 39, 65, 89 in sward data; LocationID 18, 32, 88, 121 absent in habitat data).
- Caution advised when aggregating across sites/locations due to missing entries and potential identification limits (e.g., some taxa identified to genus level).

## Potential data products and use cases
- Self-serve dashboards comparing restoration outcomes across habitat types and options (pristine vs. restoration vs. reference).
- Analyses of species composition, richness, and cover changes under different restoration treatments.
- Cross-tabulation of sward height with habitat type and option type for vegetation structure assessment.
- Integration with agri-environment scheme data (e.g., HK codes) to evaluate policy impacts on habitat restoration success.
- Data fusion with other regional datasets to support regional biodiversity assessments and restoration planning.