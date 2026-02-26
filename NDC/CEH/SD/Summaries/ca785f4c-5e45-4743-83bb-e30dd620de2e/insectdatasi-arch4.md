# Data overview

- Study scope
  - Records of insect visitations to flowers in a wildflower seed mix trial conducted in a single field on two farms: Church Farm, Oxfordshire and Lee Farm, West Sussex.
  - Seed plots: 20 x 5 m contiguous plots with four different seed mixes plus a control fallow.

- Collection/generation methods
  - Surveys conducted April–August in 2019, 2020, and 2021.
  - Each year had eight survey periods; farms were surveyed on two days per period.
  - During each survey, plots were walked along a central line; insects visiting flowers within 2 m of either side were identified in flight or captured for lab identification.

- Nature and units of record
  - Insects visiting flowers identified to a group level (hoverfly, other fly, solitary wasp, solitary bee, bumblebee, honeybee, beetle, butterfly) and counted.
  - Bees, hoverflies, and butterflies further identified to species level where possible and counted.

- Quality control
  - Wild bee and hoverfly specimens not identifiable by the primary identifier were sent to experts for accurate species identification, with sub-samples examined to ensure accuracy.

- Details of data structure
  - Data stored in an Excel spreadsheet named InsectData.csv with 14 columns:
    - Year (year of data collection)
    - Date (date of survey)
    - Month (month of survey)
    - Period (specific survey period)
    - Farm (farm where survey occurred)
    - PlotID (exact plot surveyed)
    - Mix (wildflower seed mix sown in the plot)
    - Replicate (treatment replicate)
    - Flower.family (family of the flower visited)
    - Flower.species (species of the visited flower)
    - Insect.taxa (insect group)
    - Insect.genus (insect genus)
    - Insect.species (insect species)
    - Sex (sex of the insect, where recorded)

- Data accessibility and format
  - Data available as a CSV file (InsectData.csv) containing structured, multi-year observational data with standardized fields.

- Spatial and temporal coverage
  - Timeframe: 2019–2021 (April–August sessions each year).
  - Locations: Church Farm (Oxfordshire) and Lee Farm (West Sussex) with precise coordinates provided for each site.