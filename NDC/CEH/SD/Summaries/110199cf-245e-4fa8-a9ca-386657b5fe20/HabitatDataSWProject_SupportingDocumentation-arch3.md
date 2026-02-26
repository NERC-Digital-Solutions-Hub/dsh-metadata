# Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014

## Purpose and scope
- Provides environmental health measurements to evaluate restoration across grassland, moorland/heathland, and woodland sites in South West England.
- Captures a restoration gradient with three categories: reference (control/intense land use), restoration/creation, and pristine.
- Sites are grouped by habitat type within clusters of three locations (within 2 km), enabling comparative monitoring across restoration stages.

## Experimental design
- Habitat categories defined per habitat type (Culm, Grassland, Heathland/moorland, Woodland/orchards) with explicit reference, restoration/creation, and pristine definitions.
- Each site contains three locations representing the gradient and is located within South West England.
- The gradient options often map to agri-environment scheme codes (e.g., HK7 for Restoration of species-rich grass).

## Sampling regime
- Plots: ~50 × 50 m representative of land-use type (intensive, restoring, pristine).
- Within-plot sampling: zig-zag walk; five quadrats along the central line to estimate vascular plant and bryophyte cover; DAFOR scores for overall plot vegetation.
- Sward height: measured at five locations per plot using direct measurement and a drop-disc method.
- Data collection: recorded on paper forms and entered into an Access database; outputs provided as two CSV files.

## Data structure and contents
- Two CSV files:
  - SWHabitatData.csv: quadrat-level vegetation data (SiteID, LocationID, HabitatType, Option, OptionType, SurveyDate, QuadratSize, SpeciesName, Dafor, Cover1–Cover5, etc.).
  - SWSwardData.csv: sward height data (SiteID, LocationID, HabitatType, Option, OptionType, SurveyDate, Method, SwardHeight).
- Key linking identifiers: SiteID and LocationID.
- Option and OptionType fields denote the restoration category (pristine, restoration, reference, creation) and the specific land-use option applied (e.g., HK7 for restoration of species-rich grass).
- Data notes include:
  - SiteID ranges 1–130 (SiteID 39 absent in habitat data).
  - LocationID ranges; some IDs absent in either file.
  - Detailed definitions of habitat types and option categories.

## Nature and units of recorded values
- Habitat data: species names (often at species level), cover percentages (Cover1–Cover5), DAFOR scores.
- Sward data: height in centimeters; method indicates direct measurement or drop-disc.
- Metadata fields include survey date, quadrat size, and habitat/type classifications.

## Quality control
- Data collected by experienced botanical surveyors.
- Validation included checks for anomalous values (e.g., >100% cover) and cross-checks against original sheets with corrections as needed.

## Data reuse, access, and licensing
- Licensed under the Open Government Licence (OGL).
- Citation recommended: Peyton, J.; Nuttall, P.; Gerard, F.; Pywell, R.F. (2017). Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014. NERC Environmental Information Data Centre. DOI: 10.5285/110199cf-245e-4fa8-a9ca-386657b5fe20
- Data suitable for informing monitoring frameworks due to standardized gradient design, explicit metadata, and open access.

## Relevance for monitoring frameworks
- Demonstrates a structured approach to environmental monitoring across restoration stages with clear indicators (species composition, cover, and sward height).
- Provides a dataset that can support trend analysis, gap assessment, and governance of data collection and sharing for policy evaluation and decision-making.