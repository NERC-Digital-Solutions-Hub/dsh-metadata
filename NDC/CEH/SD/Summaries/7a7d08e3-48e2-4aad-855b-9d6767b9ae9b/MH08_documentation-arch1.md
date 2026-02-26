# Vegetation plot data and peat depths from Moor House National Nature Reserve, 2008-09

## Overview
- Dataset name: Vegetation plot data from a survey of Moor House National Nature Reserve, 2008-09
- Time period: June-August 2008 and July-August 2009 (with some plots surveyed in 2012)
- Geographic coverage: Moor House National Nature Reserve (Troutbeck catchment, Moor House-Upper Teesdale NNR); altitude 290–850 m; blanket bog with Calluna vulgaris and Eriophorum vaginatum dominates
- Purpose: Re-survey of part of the reserve to document plant species, vegetation height, slope, aspect, and peat depth, building on a previous survey from 1969

## Survey design & data collected
- Plot design: 2x2 m square plots arranged on a grid with 200 m intervals (some plots at 100 m); plots located by GPS
- Data collected per plot:
  - General plot information: plot number, location type, slope, aspect, vegetation height, peat depth, altitude (when recorded)
  - Vegetation data: plant species presence and percent cover (to the nearest 5%)
- Specific measurements:
  - Slope, aspect, vegetation height (average of three measurements)
  - Peat depth using extendable pole
  - Vegetation height and presence/cover for each species
- Data collection and QA:
  - Field survey coordinated by the Centre for Ecology and Hydrology, Lancaster
  - Full training provided to surveyors; species lists checked for accuracy
  - Training materials referenced: field survey handbook CS Technical Report No.2/07

## Data structure and contents
- File 1: MH08_VEGETATION_PLOTS.csv
  - Plot information and peat depth
  - Key fields: REP_ID (plot name), SLOPE, ASPECT, VEG_HT_AVE (average vegetation height in cm), PEAT_DEPTH (cm), ALT (altitude in m), X_COORD (OSGB1936 easting), Y_COORD (OSGB1936 northing), YEAR
- File 2: Vegetation species information
  - Fields per species per plot: REP_ID (plot name), BRC_NUMBER (Biological Record Centre code), BRC_NAMES (scientific name, per Stace 1997), COMMON_NAME, TOTAL_COVER (percent cover)
- Data notes:
  - Coordinates are OSGB1936; some ALT values may be missing (0 indicates not recorded)
  - Year indicates the survey year (2008 for the resurvey data)
- Data source and staff:
  - Field team includes researchers from Moor House NNR and University of Cumbria;  markers of provenance and data handling are documented

## Geographic and ecological context
- Moor House NNR:
  - England’s highest and largest terrestrial NNR
  - Dominant habitat: blanket bog with poor drainage on glacial till; extensive upland habitats
- Re-survey rationale:
  - Previous vegetation survey occurred over 50 years earlier (Eddy et al., 1969)
  - 2008 resurvey focused on Troutbeck catchment within Moor House due to scale and accessibility constraints

## Data quality and provenance
- Data provenance:
  - Collected under formal survey protocols; maintained by Centre for Ecology and Hydrology, Lancaster
  - Related publications and references:
    - Eddy, Welch, & Rawes (1969): Moor House vegetation baseline
    - Maskell et al. (2008): Vegetation Plots Handbook CS Technical Report No.2/07
    - Stace (1997): New flora of the British Isles
- Documentation and reproducibility:
  - Clear structure of header data and species lists
  - 2012 additional plots noted, expanding the dataset beyond the core 2008-09 survey
- Limitations for analysis:
  - Spatial extent limited to Troutbeck catchment; potential gaps for local-level inference outside surveyed plots
  - Some fields may be unrecorded or recorded with 0 values; data standardisation across plots is needed for cross-dataset analyses

## Potential analyses and uses for analysts
- Correlations and pattern discovery:
  - Peat depth vs vegetation height and species composition
  - Influence of altitude, slope, and aspect on species presence and cover
  - Species richness and community composition across the 2x2 m plots
- Modelling opportunities:
  - Predictive models of species distribution and peat depth interactions
  - Habitat mapping for blanket bog and associated plant communities
- Data integration:
  - Combine with older 1969 survey data or other Moor House datasets to assess temporal changes
  - Link to broader environmental variables (e.g., drainage, soil moisture) for more comprehensive models
- Data quality considerations:
  - Standardise cover estimates (nearest 5%), handle missing altitude or coordinates, align taxonomic names to current accepted nomenclature (BRC codes)

## References
- Eddy, A., Welch, D. & Rawes, M. (1969) The vegetation of Moor House National Nature Reserve in the North Pennines, England. Vegetatio, 16, 239-284.
- Maskell, L. C., Norton, L. R., Smart, S. M., Scott, R., Carey, P. D., Murphy, J., Chamberlain, P. M., Wood, C. M., Bunce, R. G. H. & Barr, C. J. (2008) Vegetation Plots Handbook CS Technical Report No.2/07. Centre for Ecology and Hydrology, Lancaster.
- Stace, C. (1997). New flora of the British Isles. Cambridge University Press.