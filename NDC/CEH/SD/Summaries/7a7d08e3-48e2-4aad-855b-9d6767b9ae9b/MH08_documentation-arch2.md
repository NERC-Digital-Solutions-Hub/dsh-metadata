# Vegetation plot data from a survey of Moor House National Nature Reserve, 2008-09

- Purpose and relevance
  - A standardized vegetation dataset for monitoring the Moor House National Nature Reserve (NNR) ecosystem, enabling assessment of environmental health and habitat changes over time.
  - Provides plot-level and species-level information suitable for comparison with other monitoring datasets and for informing policy and management decisions.

- Survey Design & Methods
  - Survey area: Troutbeck catchment of Moor House NNR (England’s highest and largest terrestrial NNR), dominated by Calluna vulgaris and Eriophorum vaginatum.
  - Timeframe: June–August 2008 and July–August 2009 (some plots surveyed again in 2012).
  - Plot layout: Grid-based sampling with plots spaced at 200 m intervals (some 100 m), located via GPS.
  - Plot size: 2 × 2 m squares.
  - Data collected per plot:
    - Header information: plot number, location type, slope, aspect, peat depth, vegetation height.
    - Environmental measurements: peat depth (cm), altitude (m, when recorded), SLOPE, ASPECT, vegetation height.
    - Vegetation data: presence/absence and percent cover of species (to nearest 5%).
  - Survey quality: Full training for surveyors; accuracy checks on species lists.
  - Data collection tool: Electronic tablet with software adapted from Countryside Survey 2007.

- Data Structure
  - Two comma-separated value (CSV) files:
    - MH08_VEGETATION_PLOTS.csv
      - Plot information and peat depths:
        - REP_ID (plot name), SLOPE, ASPECT, VEG_HT_AVE (average vegetation height in cm), PEAT_DEPTH (cm), ALT (altitude in m, 0 if not recorded), LOCATION, X_COORD (OSGB1936 easting), Y_COORD (OSGB1936 northing), YEAR.
    - Vegetation species information:
      - REP_ID, BRC_NUMBER (species code), BRC_NAMES (scientific name), COMMON_NAME, TOTAL_COVER (percent cover for the species, 1 = present).
  - Documentation of fields includes description of each variable and measurement units.

- Geographic and Temporal Coverage
  - Location: Moor House National Nature Reserve, Troutbeck catchment, England.
  - Time period: June–August 2008 and July–August 2009 (plus additional plots in 2012); altitude range 290–850 m across the reserve.

- Origin and Documentation
  - Originators: Rose, R.J.; Wood, C.M.; Ostle, N.; Turner, C.; Whitfield, M.; Looker, A.; Looker, G. (University of Cumbria) with survey coordination by the Centre for Ecology and Hydrology, Lancaster.
  - Key documents:
    - Field survey handbook.
    - References include Eddy et al. (1969), Maskell et al. (2008) Vegetation Plots Handbook, and Stace (1997) on plant nomenclature.

- Data Quality and Use
  - Built on standardized methods aligned with established vegetation survey practices to support long-term environmental monitoring.
  - Data are suitable for assessing vegetation composition, structure, and peatland habitat characteristics, aiding comparisons over time and integration with other monitoring datasets.
  - Ensures data storage and accessibility through established project portals and archives.