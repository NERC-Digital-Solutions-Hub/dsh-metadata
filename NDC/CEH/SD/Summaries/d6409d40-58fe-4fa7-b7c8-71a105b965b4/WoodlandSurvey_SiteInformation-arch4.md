# Woodlands Survey Site Information 1971-2001

## Overview
- Biobank-style dataset of ecological data from 103 broadleaved woodlands in Britain, surveyed in 1971 with detailed plot-level data and revisited in 2000, 2002, and 2003 using the same methods.
- Data collected include canopy and ground flora composition, soil pH, Soil Organic Matter, habitat management, and a wide range of plot- and site-level descriptors.
- Analyses aim to identify ecological change and its drivers (atmospheric deposition of sulfur and nitrogen, climate, canopy change, woodland management).
- Findings and methods are published in related work (Kirby et al. 2005; Corney et al. 2004); consult these for detailed field methods and analytic results.

## Data Scope and Scope of Use
- Survey design: stratified sampling across the 103 sites; field methods follow Bunce & Shaw (1973) standardized survey protocol; a field handbook accompanies the data.
- Data types: site-level descriptors, plot-level descriptors, species/plant data, soil metrics, management practices, and environmental drivers.
- Related datasets and context: linked to Countryside Survey and earlier national woodland surveys.

## Temporal Coverage
- Baseline: 1971 survey data for sites and plots.
- Re-surveys: 2000, 2002, 2003 (referred to as 2001 in documentation), using identical field procedures to enable long-term change assessment.

## Data Structure and Semantics
- Core entities:
  - Site: site_code (1–103), site_name (text)
  - Plot: plot_number (1–16)
  - Code and Description: coded descriptors for site/plot characteristics; Code_group categories to group site descriptions
  - Score: numeric weighting for open habitat features (example: 1 for narrow paths, 5 for wide open habitats) to construct abundance indices
  - Year: survey year for descriptors (1971; 2000s)
  - Field_sheet: sheet type (Site header, Plot header, Site descriptions, Plot descriptions)
  - Slope and Aspect: 1971 and 2000s values
  - Location: Easting and Northing (OSGB GB National Grid, in kilometres)
  - Recorders: initials for surveyors (1971 and 2003)
  - Date2003: standardized survey start date (year standardized to 2002 in metadata)
  - Notes and supporting metadata
- Indices and groupings:
  - Constructed indices for woodland management (wm), tree/shrub regeneration (r), open habitats (o), and adjacent land cover (l) using coded site descriptors.
- Data lineage and references:
  - Supporting documentation clarifies data provenance and the relationship to the Flora dataset (Woodlands_Survey_Flora_1971_2001).

## Data Quality, Metadata, and Access
- Detailed documentation of data structure, field names, and coding schemes is provided, including how openness is weighted for open habitat indices.
- Original publications (Kirkby et al. 2005; Corney et al. 2004) provide field methods and analytic results; the dataset itself serves as the underlying data source for those analyses.
- Access note: The dataset is accessible via the provided DOI (http://doi.org/10.5285/d6409d40-58fe-4fa7-b7c8-71a105b965b4) and is related to other datasets such as Countryside Survey.

## Provenance and Contacts
- 1971 originators: R.G.H. Bunce & M.W. Shaw (Woodland Ecology Section, Nature Conservancy Merlewood)
- 2001–2003 contributors: Simon Smart, Helaina Black, Keith Kirby, Phil Corney (CEH Lancaster, English Nature, University of Liverpool)
- References for methods and results include Avery (1973); Corney et al. (2004); Haines-Young et al. (2003); Kirby et al. (2005).

## References (selected)
- Avery, B. W. (1973). Soil Classification in the Soil Survey of England and Wales.
- Corney, P.M. et al. (2004). The effect of landscapescale environmental drivers on the vegetation composition of British woodlands. Biological Conservation.
- Haines-Young, R.H. et al. (2003). Changing landscapes, habitats and vegetation diversity across Great Britain. Journal of Environmental Management.
- Kirby, K.J. et al. (2005). Measuring Long Term Ecological Change in British woodlands (1971-2001): A re-survey and analysis based on the 103 Bunce 1971 sites. English Nature Research Reports.