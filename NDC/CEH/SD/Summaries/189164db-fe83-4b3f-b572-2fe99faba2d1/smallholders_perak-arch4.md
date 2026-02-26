# Data on the locations of and temperatures (in deg C) recorded by dataloggers deployed in the soil during surveys at 24 oil palm smallholder farms in Perak, Malaysia

## Purpose and scope
- Describes soil temperature data, insect biodiversity observations, predator–prey assessments, vegetation and soil environmental measurements, and social survey data collected across 24 oil palm smallholders in Perak, Malaysia.
- Aimed to enable assessment of how differing plantation management practices influence soil conditions, insect communities, and associated ecological interactions over about a 24-hour field period.

## Study design and sampling
- Collaboration levels with Wild Asia (WA) among smallholders: WAGS-BIO (trained in sustainable practices), WAGS (information on RSPO/MSPO with eventual assessments), and Independent farmers (no WA guidance).
- Sampling locations: four main points per smallholder plot (T1–T4), spaced ~20 m apart, yielding 96 sampling points across 24 farms.
- Data collection windows: May–July 2022 (soil and biodiversity) and December 2021–February 2022 (environmental and survey data).
- Methods:
  - Dataloggers: Thermochron iButton devices buried at 5 cm depth to record soil temperatures; data downloaded and quality-checked by Cambridge researchers.
  - Biodiversity surveys: 100 m transects with 5 m × 5 m observation boxes; butterflies, Nephila spiders, assassin bugs documented; weather and microhabitat recorded; species identified with guides and photos when needed.
  - Predation/entomology: sticky traps (30 cm × 30 cm) hung 40 cm above ground; bait cards with mealworms to assess predation; traps collected after 24 hours and photographed; insects sorted to order level.
  - Vegetation and soil environment: environmental surveys at 47 plantations including crop types, vegetation cover and height, canopy density, microclimate (air temp/humidity), leaf litter, soil moisture, soil pH, A-horizon depth, and Visual Evaluation of Soil Structure (VESS).
  - Social surveys: farmer demographics, management practices, attitudes toward wildlife, income, and agricultural motivations; ethical approval obtained; data anonymised. 

## Datasets and key data components
- Soil temperature data
  - Location and time-stamped air/soil temperature readings (TempHr1–TempHr26), with hourly granularity after datalogger setup.
  - Metadata includes PlantationCode, SamplePoint (T1–T4), data collection timing, and notes on NA entries when data were missing or incomplete.
- Insect biodiversity observations
  - Species identifications (SpeciesID), encounter data, and counts by life state (flying, resting, sunning, interacting, nectaring).
  - Weather conditions and date/time of surveys; microhabitat descriptions; plant species involved in nectaring.
- Sticky traps and predation data
  - Trap locations (StickyTrapSamplePoint) with setup and collection times; counts by taxonomic groups (e.g., ants, termites, wasps, various arthropod orders); total specimen counts and ordinals; notes on additional taxa.
  - Mealworm bait cards: number remaining after 24 hours to infer predation pressure.
- Vegetation, microclimate, and soil data (47 plantations)
  - Plot-level environmental variables: crop type and percent cover, GPS coordinates for plot corners and center, side lengths, neighbouring habitat types, canopy density, leaf litter depth, soil moisture and pH, A-horizon depth, and VESS scores.
  - Vegetation structure: plant height measurements, canopy openness (both optical and visual assessments), air temperature/humidity at sampling points, and palm-related metrics (age, height, epiphyte cover, herbivory, health).
- Long-form plantation survey data (49 plantations)
  - Plantation characteristics (type, size, land-use history, district, coordinates, owner/manager details), sociodemographic information of respondents, management practices, attitudes toward wildlife, and economic factors.
  - Detailed management and input data (herbicides, fertilizers, intercropping, livestock, pest/disease management, costs, yields, prices, and conversions).
  - Motivations and perceptions related to nature, culture, health, and economic factors; several open-ended responses included.
- Cross-site and socio-ecological context
  - Data also reference parallel sampling in Riau, Indonesia, and Banting, Malaysia as part of a broader project.

## Data quality, structure, and ethics
- Data are standardized and quality-checked by field teams and Cambridge researchers to ensure consistency and correct timing alignment across datasets.
- Units and variable types are specified (e.g., temperatures in °C, dates in YYYY-MM-DD, times in HH:MM, distances in metres/hectares, etc.).
- Social data are anonymised; participants provided consent; some responses are NA due to field decisions, non-response, or sensitivity. Acknowledges potential errors or misreporting in self-reported data.

## Collaboration, governance, and use cases
- Data reflect a collaboration framework among WA, smallholders at three levels of engagement, and an academic partner, highlighting data governance considerations such as standards, discoverability, and cross-dataset integration.
- Intended use includes assessing how management practices influence soil conditions, biodiversity (arthropods and predators), and vegetation structure, with potential to inform data-driven improvements in agro-ecosystem management and policy guidance within a multi-site network.

## Limitations and caveats
- Some fields contain NA values due to non-recovery, incomplete measurements, or self-reported data gaps.
- Social data are self-reported and not independently validated; the observational data are cross-sectional within a 24-hour window and may not capture longer-term dynamics.
- Taxonomic resolution varies across datasets (e.g., order-level for many arthropods; species-level for some insects in certain parts of the dataset).

## Practical takeaways for data leadership
- The collection illustrates a multi-source, multi-dimensional data system combining environmental, ecological, and social data across a network of farmers, with careful calibration and data governance practices.
- Emphasizes the importance of clear metadata, consistent variable definitions, and standardized data cleaning to support integrative analyses and policy-relevant insights.
- Demonstrates opportunity and challenges in aligning data collection across partners with varying levels of collaboration, while preserving data quality and discoverability for broader reuse.