# Vegetation plot data from a survey of Moor House National Nature Reserve, 2008-09

- This dataset records plant species presence and abundance in 2x2 meter plots within Moor House National Nature Reserve (Troutbeck catchment), England.
- Timeframe: re-survey conducted in June–August 2008, July–August 2009 (with a few additional plots surveyed in 2012).
- Aim: re-survey part of Moor House to compare with a prior survey from the 1960s and to document current vegetation and habitat characteristics in a blanket bog-dominated upland area.

## Dataset contents and structure

- Data is provided in two comma-separated value (CSV) files:
  - MH08_VEGETATION_PLOTS.csv
    - Plot header information: REP_ID (plot name), SLOPE, ASPECT, VEG_HT_AVE (average vegetation height in cm), PEAT_DEPTH (cm), ALT (altitude in metres; 0 if not recorded), LOCATION (location type), X_COORD, Y_COORD (OSGB197x coordinates), YEAR (year of survey).
    - Vegetation data: BRC_NUMBER (species code), BRC_NAMES (scientific name, per Stace 1997), COMMON_NAME, TOTAL_COVER (percent cover, 1% increments).
  - The dataset covers habitat and site descriptors as well as species presence and cover per plot.
- Plot design and sampling:
  - Grid-based sampling with plots spaced at approximately 200 m (some 100 m) intervals.
  - Each plot is a 2x2 m quadrat with measurements of altitude, slope, aspect, vegetation height, and underlying peat depth.
  - Species presence and percent cover were recorded for each plot.
  - GPS-based plot locations; data collected using an electronic tablet with a program adapted from Countryside Survey 2007.
- Spatial reference: coordinates provided as OSGB36 easting/northing.
- Coverage: Troutbeck catchment within Moor House, England’s highest and one of the largest blanket bog NNRs, with peat depths typically 2–3 m and diverse upland habitats.

## Survey design, methods, and quality

- Field team: staff coordinated by the Centre for Ecology and Hydrology (CEH), Lancaster; surveyors include researchers from the University of Cumbria.
- Training: full training provided to surveyors; species lists have been checked for accuracy.
- Documentation and references:
  - Field survey handbook (CS Technical Report No. 2/07) for methodology.
  - Background references include Eddy et al. (1969) vegetation study of Moor House and Stace (1997) flora reference.
- Data quality and interpretation:
  - Header information (plot metadata) and species data are aligned by plot identifier (REP_ID).
  - ALT, PEAT_DEPTH, and other habitat descriptors are recorded where available; some plots may have missing altitude (0 indicates not recorded).

## Provenance and key documents

- Originating context: Moor House National Nature Reserve, with re-survey motivated by the need to update vegetation data after more than five decades since the 1960s survey.
- Key documents:
  - Field survey handbook (Centre for Ecology and Hydrology, Lancaster).
  - Eddy, Welch & Rawes (1969) vegetation study of Moor House.
  - Maskell et al. (2008) Vegetation Plots Handbook (CS Technical Report No. 2/07).
  - Stace (1997) New flora of the British Isles.

## Relevance for monitoring frameworks and policy

- Enables monitoring of vegetation composition and cover in upland blanket bog habitats, contributing to:
  - Assessment of habitat condition and trends over time.
  - Evaluation of peatland health, biodiversity status, and potential responses to environmental change.
  - Baseline data for long-term monitoring programs and for informing management decisions at Moor House NNR.
- Data governance and openness implications:
  - Data are structured with explicit metadata (plot descriptors and species data) and publicly accessible field documentation.
  - Provides a model for integrating site-level ecological measurements (habitat, peat depth, and vegetation metrics) into monitoring frameworks.

## Key references

- Eddy, A., Welch, D. & Rawes, M. (1969). The vegetation of Moor House National Nature Reserve in the North Pennines, England. Vegetatio, 16, 239-284.
- Maskell, L. C. et al. (2008). Vegetation Plots Handbook CS Technical Report No.2/07. Centre for Ecology and Hydrology, Lancaster.
- Stace, C. (1997). New flora of the British Isles. Cambridge University Press.