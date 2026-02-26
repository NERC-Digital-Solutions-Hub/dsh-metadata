# Woodlands Survey Site Information 1971-2001

## Overview
- 1971: 103 broadleaved woodlands surveyed across Britain; ecological data collected at site level and from 16 random 200 m² plots per site.
- Follow-up: Same sites re-surveyed in 2000, 2002, and 2003 (referred to as 2001), using identical field methods.
- Objective: Analyze ecological change between 1971 and the 2000s and identify principal drivers of change using a suite of explanatory variables from survey data and external sources (e.g., atmospheric deposition of sulfur and nitrogen, climate, canopy changes, woodland management).
- Key publications: Kirkby et al. (2005) and Corney et al. (2004) provide results and analysis; consult these for methodological and analytical details.

## Survey Design & Methods
- Stratified sampling across the surveyed area.
- Field methods follow Bunce & Shaw’s 1973 standardized survey approach; field handbook available in supporting documentation.

## Data Coverage & Provenance
- Baseline year: 1971; follow-up years: 2000, 2002, 2003 (with 2003 data standardized to 2002 in metadata).
- Originators (1971): R.G.H. Bunce & M.W. Shaw; (2001–3): S. Smart, H. Black, K. Kirby, P. Corney, et al.
- Related datasets and context: Countryside Survey; Steele (1968) National Survey of Woodlands.

## Data Structure & Fields
- Hierarchical data: Site and Plot level descriptors.
- Key fields:
  - Site: site code (1–103), site name, country (England/Scotland/Wales), easting/northing (OSGB grid, kilometres), slope and aspect (1971 and 2000s), date of surveys, recorders.
  - Plot: plot number (1–16), plot descriptions, slope and aspect (1971/2000s).
  - Descriptors: codes, descriptions, notes, and code groups.
  - Year: year of survey for site/plot descriptions (1971 or 2000s).
  - Field sheets: organization by field_sheet (Site Header, Site Descriptions, Plot Header, Plot Descriptions).
- Data categorization and indices:
  - Groups of site-level descriptors enable construction of indices for woodland management (wm), tree/shrub regeneration (r), open habitats (o), and adjacent land cover (l).
  - Open habitat scoring uses a weighted system (e.g., 1 for narrow paths, 5 for wide rides) to reflect openness and influence on habitat abundance.
- Supporting documentation notes the exact year of survey may be found in the Woodlands_Survey_Flora_1971_2001 dataset.

## Derived Indices & Scoring
- Indices compiled from site descriptions to quantify changes in:
  - Woodland management intensity
  - Regeneration of trees/shrubs
  - Open habitats
  - Adjacent land cover
- Open habitat abundance is weighted to reflect the relative size/impact of different features.

## Related Datasets & Access
- Related datasets: Countryside Survey; historical references (e.g., Steele 1968).
- Documentation and metadata are provided to support data reuse, including a field handbook and detailed data dictionary within the dataset.

## Temporal Coverage
- 1971 baseline surveys with follow-ups in the early 2000s (2000, 2002, 2003; referred to as 2001 in some contexts).
- Date fields include Year 1971 and Date2003 (with date standardized to 2002 for the survey period).

## Documentation & References
- References include methodological and analytical work:
  - Kirby et al. (2005) on measuring long-term ecological change (1971–2001)
  - Corney et al. (2004) on landscape-scale drivers of vegetation in British woodlands
  - Additional supporting documentation and field methods references (Bunce & Shaw, 1973; Steele, 1968; Avery, 1973)

## Potential Uses for Environmental Monitoring & Policy Evaluation
- Long-term monitoring of woodland ecological change and driver attribution (deposition, climate, management practices).
- Standardized, replicable dataset suitable for time-series analyses and cross-site comparisons.
- Integration with other environmental data sources to enhance value beyond single-use analyses; supports transparency and data sharing by preserving underlying site/plot descriptors and open-habitat indices.

## Considerations for Analysts
- Data quality assurance and standardization are central, with outputs designed as clear, shareable formats (reports, maps, charts) and datasets stored in appropriate portals.
- The dataset is structured to enable combining with external environmental data (e.g., atmospheric deposition, climate) to explore drivers of change.