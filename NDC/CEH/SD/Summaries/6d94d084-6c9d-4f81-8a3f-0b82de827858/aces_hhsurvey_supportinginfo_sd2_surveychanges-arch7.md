# Abrupt Changes in Ecosystem Services and Well-Being in Mozambican Woodlands (NE/K010395/1) Household Survey Data Supplementary Document 2 : ACES Household Survey Changes - Mabalane to Marrupa and Marrupa to Gurué

- Purpose and scope
  - Documents survey instrument and questionnaire changes between three survey rounds in Mozambique: Mabalane (May–Oct 2014), Marrupa (May–Aug 2015), and Gurué (Aug–Dec 2015).
  - Focuses on how data collection adjustments affect data structure, coding, and subsequent analyses, including potential GIS applications.

## Changes from Mabalane (2014) to Marrupa (2015)

- Income section
  - More pre-coded multiple-choice answers to ease data recording.
  - Reordered questions in the income section (e.g., sequence: quantity sold, unit, price per unit changed to quantity sold, unit, price per unit).
- New content added
  - Questions on inputs used for tobacco production (commercial and subsistence) and “what type of woodfuel.”
  - Charcoal questions: price per unit added for charcoal produced in the past 12 months.
  - Derived income categories introduced: forest income, fishing income, environmental income.
  - New timing question: “In what month did you do this activity in the last year?” to capture seasonality.

## Changes from Marrupa (2015) to Gurué (2015)

- New topics and timing
  - Added questions on land conflicts and access to services, with both a 12-month window and a 5-year timeline, plus information on with whom the conflict occurred.
  - Month-of-activity questions continued to support seasonality analysis.
- Income and asset additions
  - Bamboo added as a pre-coded answer in direct forest income type.
  - New income code for selling along the street in village (local market/ Rua) and related categories.
  - Brick-making added as an income source.
- Wage labour enhancements
  - Added questions for name of employer and type of employment.
- Crop and agricultural additions
  - New income codes for crops (e.g., corn as merchant maize) and renting out equipment (e.g., tractors).
  - Added questions about inputs used for soya production (commercial and subsistence).
  - Disaggregation of crop production inputs by crop (previously aggregated).
  - Pest-related questions expanded: specific pest types and quantity of crops lost.
- Nutrition and inputs
  - Added questions about households’ main source of protein.

## GIS and data-product implications

- Data harmonization needs
  - Reordering and new variables across rounds require crosswalks to ensure consistent attribute schemas for GIS analyses.
  - Differences in coding (pre-coded answers, new income categories) necessitate recoding or mapping to a unified schema.
- Enhanced spatial context
  - Land conflicts and access to services introduce spatially-relevant attributes for mapping conflict incidence, service accessibility, and their temporal dynamics.
  - Seasonality timing (months of activity) enables temporal alignment of activities with land use and forest/resource maps.
- Data quality considerations
  - Expanded questions (new codes, disaggregated inputs, pest specifics) increase potential for missing data and require consistent data dictionaries and translation checks.
  - New or modified income and crop codes affect how ecosystem services and livelihood dependencies are represented geographically.

## Recommendations for GIS workflows

- Develop a harmonization schema
  - Create a crosswalk linking old and new variable codes to a unified GIS-ready schema.
  - Document any reordering impacts on longitudinal analyses.
- Update data dictionaries and metadata
  - Capture definitions for new variables (e.g., land conflicts, new income codes, pest categories) and their coding schemes.
- Ensure temporal alignment
  - Align month-of-activity data across rounds to enable seasonal mapping of activities and ecosystem services.
- Validate spatial analyses
  - Test mapping outputs with prototypes to confirm that new attributes (land conflicts, access to services, new income sources) integrate smoothly with existing spatial layers (forest cover, land use, infrastructure).
- Prepare for ongoing data integration
  - Implement data quality checks for new inputs disaggregated by crop and for derived income categories to support robust GIS analyses and map-based storytelling.