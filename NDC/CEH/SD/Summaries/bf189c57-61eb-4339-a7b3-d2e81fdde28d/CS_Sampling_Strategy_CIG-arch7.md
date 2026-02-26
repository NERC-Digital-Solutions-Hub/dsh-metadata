# The Sampling Strategy for Countryside Survey (up to 2007)

- The document details the evolution of the ITE Land Classification and the sampling framework for Countryside Survey field campaigns up to 2007, linking methodological history to current (2007) spatial data products.

## Overview and purpose

- Purpose: describe how field surveys are designed and how data are stratified, collected, and used to produce national and country-specific habitat estimates.
- Core idea: use an environmental stratification (ITE Land Classification) to ensure samples represent Britain's varied landscapes.
- Importance for GIS: provides the basis for map-based data products, classifications, and spatial estimates across GB, with explicit handling of country-specific reporting.

## Core concepts for GIS work

- Sampling unit: 1 km x 1 km squares (centre squares originally; later expanded with surrounding squares for classification stability).
- Stratified, random sampling: to reduce bias and ensure coverage across land classes.
- Land Classification: ITE Land Classification (32 classes in original framework; expanded to 40, then 45 with country-unit subdivisions for CS2007).
- Data flows: environmental attributes (altitude, geology, climate, etc.) drive classification and sampling frames; field data collected per square and aggregated to national/country estimates.
- National estimates: derived from mean habitat area per square within each Land Class multiplied by the total land-class area; later, separate country estimates (England with Wales; Scotland) requested and implemented.

## Evolution timeline and key changes

- 1978 – Initial Land Classification (CS1978)
  - ISA-based classification yielding 32 Land Classes from 1 km squares (center squares of a 15 x 15 km grid).
  - Classification included surrounding squares; total classified: ~6,039 squares.
  - Field survey: 8 squares per Land Class (256 total) to estimate national habitat areas.

- 1984 – Second Field Survey (CS1984)
  - Expanded to 12 km squares per Land Class (384 total).
  - Focus shifted toward land use, landscape features, habitat mapping.

- 1990 – All Squares Land Classification (CS1990)
  - Updated to classify every 1 km square in GB; 508 squares surveyed.
  - Resulting land-class map used for national estimates; satellite-derived land cover linked.

- 1998 – Revised Land Classification (CS1998/CS1990 revision)
  - Increased to 40 Land Classes to allow Scotland-only reporting; framework prepared for regional estimates.

- 2000 – Countryside Survey 2000 (CS2000)
  - Introduced separate-country reporting (England with Wales vs Scotland) with country-specific estimates.
  - Land Classes subdivided into country-unit versions; 40 strata expanded to 40 (and then to 45 with subdivisions).
  - Added 19 squares to ensure adequate representation of new classes; additional sampling allocated to Wales (and some reallocation to England).
  - Wales-specific adjustments increased Wales sampling density; Scotland maintained separate reporting.

- 2007 – Countryside Survey 2007 (CS2007)
  - Wales-only reporting intensified: created five new Welsh country-unit classes (5w, 6w, 7w, 15w, 18w); total strata increased to 45.
  - Additional 43 Welsh squares added; ensured minimum of 6 squares per Welsh class.
  - England retained most classes; a couple of English classes (5e, 15e) ended with 4 squares per class but deemed acceptable for precision.
  - Updated maps show revised England/Wales/Scotland Land Class framework and sampling squares.

## Data products and outputs

- Land Class maps: evolving classifications (1978 original 32 classes; later expansions to 40/45 with country-unit subdivisions) used as a spatial framework for maps and analyses.
- Sampling square maps: figures show the distribution and location of sample squares across GB and by country.
- Tables of sampling effort: detailed counts of squares per Land Class, per country, and per survey year (CS1978, CS1984, CS1990, CS2000, CS2007); extraction indicates sampling rate and coverage.
- National and country estimates: calculation method described (mean habitat per square within a class × total area of the class; with separate computations for England, Wales, and Scotland under CS2000/CS2007).
- Methodological notes: notes on consistency and comparability across surveys, acknowledging that changing classifications affects national estimates.

## Country-specific considerations

- England with Wales vs Scotland: country-unit versions of Land Classes created to enable separate reporting; adjustments included class subdivisions, aggregations, and additional squares to ensure representation in each country.
- Wales-specific reporting: heightened sampling density and Welsh-specific class subdivisions to deliver Wales-only habitat status and change information.
- Isle of Man: removed from country-unit estimates and replaced with additional English squares for England reporting.

## Uplands and additional modules

- An uplands module (CS2000) added 30 extra squares in upland/marginal areas to improve statistical accuracy for upland habitats within country-based estimates.

## Notable methodological notes

- Change management: switching to newer Land Classifications affects consistency of national stock estimates; preferred approach is to use the latest classification within a survey while recognizing cross-survey comparability challenges.
- Appendix and references: provides a historical appendix of Land Classification development and extensive bibliography for context and replication.

## Takeaways for GIS practitioners

- The Countryside Survey provides a robust, stratified sampling framework tied to a multi-era land classification system, enabling map-informed habitat estimation and trend analysis at GB and country levels.
- GIS workflows can leverage the evolving Land Class maps and sample-square grids to create consistent thematic maps, calculate area-based estimates, and compare land-cover/habitat metrics across survey years, with careful attention to classification changes when comparing across years.