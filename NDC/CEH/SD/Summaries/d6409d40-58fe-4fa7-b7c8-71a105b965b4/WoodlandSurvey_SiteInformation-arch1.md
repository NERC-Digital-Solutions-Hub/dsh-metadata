# Woodlands Survey Site Information 1971-2001

## Overview
- National survey of 103 broadleaved woodlands in Britain conducted in 1971.
- Detailed ecological data collected at the site level and from within 16 random 200 m² plots per site.
- Data include canopy and ground flora composition, soil pH, soil organic matter, habitat management, and various plot- and site-level descriptors.
- Re-surveyed in the 2000s (2000, 2002, 2003; referred to as '2001') using identical field methods to assess ecological change.
- Analyses aimed to identify drivers of change, incorporating variables such as atmospheric deposition of sulfur and nitrogen, climate, canopy structure changes, and woodland management.
- Foundational publications for methods and results are Kirkby et al. (2005) and Corney et al. (2004); users should consult these for detailed methods and findings.

## Survey Design & Methods
- Stratified sampling across the study area; field surveys conducted following Bunce & Shaw (1973) standardized methods.
- A field handbook is included in supporting documentation.
- Re-survey design followed the same methods, enabling comparison across time.
- Related contextual datasets include Countryside Survey and the 1968 Steele national woodland survey.
- Originators and key contributors (1971 and 2001–2003) are listed, with affiliations.

## Data Structure and Variables
- Data organized by:
  - Site: Site code (1–103), Site_name (where Field_sheet = 'Site header' only).
  - Plot: Plot number (1–16) (where Field_sheet = 'Plot descriptions' or 'Plot header' only).
  - Code and Description fields detailing site/plot descriptors.
  - Notes and Code_group fields to categorize site description codes.
  - Groupings and scores for constructing indices:
    - Open habitats index weighted by size/impact (e.g., 1 for narrow features, 5 for wide rides).
  - Temporal and spatial variables:
    - Year of survey for site descriptions, slope and aspect in 1971 and 2000s (Slope71, Slope03; Aspect71, Aspect03).
    - Geospatial coordinates (Easting, Northing in OSGB GB National Grid, in kilometres).
    - Date fields: Date1971 (start of 1971 survey), Date2003 (survey start in 2000s; standardized to 2002 in metadata).
    - Recorders1971 and Recorders2003 indicating surveyors.
    - Site_usage indicating management status (e.g., managed/unmanaged).
- Data include cross-time comparability through identical field methods and standardized descriptors.

## Open Habitat Scoring and Indices
- Open habitat descriptors are weighted to produce an index of abundance, reflecting the extent of openness.
- Weighting scheme examples:
  - Path 1–5 m wide assigned a score of 1.
  - Ride wider than 5 m assigned a score of 5.
- Indices cover woodland management (wm), tree and shrub regeneration (r), open habitats (o), and adjacent land cover (l); designed to quantify change over time.

## Related Datasets and Provenance
- Related datasets and references:
  - Countryside Survey
  - Steele, R.C. (1968): National survey of woodlands (reprint)
- Publications for methodological detail and analysis:
  - Corney et al. (2004): The effect of landscapescale environmental drivers on vegetation composition.
  - Kirby et al. (2005): Measuring Long Term Ecological Change in British woodlands (1971–2001): a re-survey and analysis.
  - Kirkby et al. (2005): Detailed analysis focusing on change drivers (as cited).

## Access, Usage and Documentation
- Users are advised to consult the cited publications for field methods and analytical results.
- The dataset includes extensive metadata and documentation sections, including field sheets and code group descriptions.
- Date handling note: Date2003 is a reference point with standardized year; actual survey year is documented in accompanying metadata.
- Supporting documentation provides deeper details on site usage, coding, and scoring.

## Limitations and Analytical Considerations
- Potential scale and resolution mismatches when integrating with other datasets (local vs. national scale).
- Open habitat and other indices rely on specific weighting schemes; interpretation should consider these construction rules.
- Some plots may have missing surveys or nosurvey reasons documented in the metadata.
- Access to historical data and field sheets may be required to reproduce methods exactly.

## References
- Avery, B. W. (1973). Soil Classification in the Soil Survey of England and Wales. Journal of Soil Science.
- Corney, P.M., LeDuc, M.L., Smart, S.M., Kirby, K.J., Bunce, R.G.H., Marrs, R.H. (2004). The effect of landscapescale environmental drivers on the vegetation composition of British woodlands. Biological Conservation.
- Haines-Young, R.H., Barr, C.J., Firbank, L.G., et al. (2003). Changing landscapes, habitats and vegetation diversity across Great Britain. Journal of Environmental Management.
- Kirby, K.J., Smart, S.M., Black, H.I.J., Bunce, R.G.H., Corney, P.M., Smithers, R.J. (2005). Measuring Long Term Ecological Change in British woodlands (1971-2001): A re-survey and analysis of change based on the 103 sites in the Bunce 1971 woodland survey. English Nature Research Reports.