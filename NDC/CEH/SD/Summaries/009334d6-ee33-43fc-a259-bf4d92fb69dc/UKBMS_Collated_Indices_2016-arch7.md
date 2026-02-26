# The UK Butterfly Monitoring Scheme (UKBMS) collates data from over 2,000 sites per year throughout the UK.

## Overview
- UKBMS collects butterfly count data from over 2,000 sites annually across the UK.
- Data include all-species transects, reduced-effort Wider Countryside Butterfly Survey (WCBS) transects, single-species transects, timed counts, and egg/larval web counts.
- Transect routes are fixed to enable year-to-year comparisons; populations are estimated using standardized methods.

## Data collection methods
- All-species transects
  - Fixed-route line transect at a site; 2–4 km long; 45 minutes to 2 hours walk.
  - Record all butterfly species within a fixed-width band (typically 5 m) along the transect weekly from April to September.
  - 26 counts per year; transects divided into sections by habitat/management units.
  - Walks occur between 10:45 and 15:45 under suitable butterfly-activity weather (specific conditions described).
- Single-species transects
  - Follow all-species methodology but recorded only on weeks relevant to the focal species.
- Timed counts and egg/larval web counts
  - Timed counts record abundance of a species over a set period/area (within weather constraints).
  - Egg/larval web counts record eggs or larval webs in suitable habitat areas.
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort survey for wider countryside habitats (farmland, etc.).
  - Based on the BTO Breeding Bird Survey (BBS) design: two parallel 1-km transects within randomly selected 1-km squares, subdivided into 10 sections.
  - 2–4 visits per year (minimum 2 visits in July/August; spring visits encouraged).

## Data handling and storage
- Field data recorded on standard forms; entered online via UKBMS data entry site or via Transect Walker software.
- Data entry can be by the recorder or regional transect coordinators; coordinators compile region-wide data at season end.
- Online data and Transect Walker files uploaded into an Oracle database containing all records.

## Analytical methods
- Wider countryside species (WCBS and related data)
  - Use all counts across survey types to estimate the seasonal pattern for the year (two-stage model).
  - Stage 1: Generalized Additive Model (GAM) estimates annual seasonal flight pattern.
  - Stage 2: Model uses seasonal values as an offset to estimate annual abundance changes (seasonality-adjusted indices).
  - Method described in Dennis et al. 2013.
- Habitat specialists and regular migrants
  - GAMs impute missing values and calculate site indices.
  - Site indices are combined to derive a national annual Collated Index via log-linear modeling to account for year and site effects.
  - Collated Indices updated annually; indices for species recorded at five or more sites.
- Definitions and distinctions
  - Wider countryside species: mobile species across diverse habitats.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: species that overwinter outside the UK; not overwintering in the UK.
  - Some species (e.g., Red Admiral) may be partially resident in parts of the UK.
- Note on data timing
  - Collated Indices may be unavailable for some early years due to insufficient data; the dataset indicates the number of contributing years per species.

## Nature and units of recorded values
- Site indices: relative measures of population size; proportional to actual abundance; not absolute counts.
- Collated Indices: presented as log10 of the Collated Index (LCI); scaled so the average over the series equals 2, enabling relative time-based comparisons.

## Quality control
- In-field automated checks (Transect Walker) flag unlikely data entries (e.g., unusually high counts, records outside flight periods).
- Regional transect coordinators validate and review data; checks can be ongoing during the season.
- Post-entry validation includes automated/manual checks for:
  - Records outside known geographic distribution.
  - Records outside normal flight periods.
  - First-time site records.
  - Extreme or anomalous abundances.
- Output formats
  - Collated Indices stored as CSV files.
  - CSV columns include Species (scientific name per Fauna Europaea), Common name, Year, No. Sites, Collated Index, Time period.

## GIS-relevant notes (data formats, spatial aspects, and outputs)
- Transects are fixed routes (line features) enabling temporal GIS analyses and change detection along the same paths.
- WCBS samples occur within 1-km squares (polygon/grid references) for spatially distributed sampling of wider countryside habitats.
- Data originate from multiple sites with habitat units along transects, suitable for mapping habitat associations, transect segments, and site-level indices.
- Outputs suitable for GIS include: fixed transect lines, WCBS squares, site indices by year, and Collated Indices (CSV) for spatial visualization and trend analysis.