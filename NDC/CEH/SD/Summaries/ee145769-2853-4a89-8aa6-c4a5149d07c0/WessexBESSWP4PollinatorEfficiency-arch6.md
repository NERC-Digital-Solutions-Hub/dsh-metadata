# Pollinator effectiveness in oilseed rape ( Brassica napus L.) in relation to behavioural and morphological characteristics .

- Overview
  - Dataset from the Wessex BESS project (NERC Biodiversity and Ecosystem Service Sustainability program) to quantify pollen grain delivery per visit by pollinators to oilseed rape (Brassica napus L.).
  - Also captures behavioural and morphological traits to explore traits linked to pollen delivery.
  - Can be used with other Wessex BESS datasets, especially landscape-scale pollinator surveys.

- Study design and setting
  - Location: Wiltshire, UK (central point 51.185988° N, -1.832657° W).
  - Timeframe: April–June, 2014–2016 (three field seasons).
  - Sites: 15 fields of winter-sown OSR.
  - Field procedures: observe flower visitors; present flowers using bouquet method for solitary bees, bumblebees, honeybees or plastic-box method for non-bees; leave visitor undisturbed to contact stigma.

- Data collected and key variables
  - Pollen deposition (SVD): total pollen grains on stigma after a single visit (microscopy at x20).
  - Pollen loads: free pollen on body parts swabbed (head, top thorax, tarsi, bottom thorax); counts from jelly cubes; tarsi excluded for small beetles.
  - Morphological traits: body length, intertegular distance (ITD; proxy where needed), hair density on thorax, hair type (Branched, Smooth, No_hair).
  - Visit metadata: visit duration (LengthVisit, seconds), visit type (VisitType: probing, crawling, short), field method used (MethodUsed: B for bouquet, PB for plastic box).
  - Taxonomic and grouping data: PollinatorID, SpeciesCode, Description, Family, FunctionalGroup (and FunctionalGroupPollSwab for linking to other data).
  - Pollen swab data: presence of free pollen on body parts (PollSwab: Y/N), counts on Back, Feet, Head, Under; 15-stroke swabs per body part.
  - Data structure: two linked files—NERCPollinatorEfficiency and NERCPollenSwab; PollSwab can be linked to PollinatorEfficiency via PollinatorID.
  - Controls: control OSR flowers processed similarly but without visitation; median pollen on control stigmas observed as 11 (n=31).

- Experimental and lab methods
  - Flower sampling and stigma preparation: preserved in glycerine jelly with basic fuchsin; stigma removed for pollen counting.
  - Pollen counting: small sections from stigma melted onto slides; pollen grains counted under microscope.
  - Pollen swabbing: jelly cubes used to collect pollen from predefined body parts; prepared slides counted under microscope.
  - Morphology and trait data collected per species (average values used when multiple individuals available).

- Data quality assurance
  - Standardized field and lab protocols; training provided by R. Shaw.
  - Data entry in MS Access with anomaly checks.
  - Documentation of missing data and coding conventions; detailed description of file contents and column meanings.
  - Notable data notes: PollinatorID 94 missing species data; some columns have complex coded formats (e.g., SpeciesCode, VisitType, FunctionalGroup).

- Data attributes and usage notes
  - Data format includes dates, geographic coordinates, durations, and multiple measurement units (continuous and categorical).
  - Where possible, species- or group-level averages are used for traits (e.g., body length).
  - Caution for certain limitations: tarsi of small beetles could not be swabbed (7 NA values for Feet); some missing identifiers and coding inconsistencies may require careful handling when merging with other datasets.

- Practical implications for data use and integration
  - Enables analysis of relationships between pollinator behaviour/morphology and pollen deposition efficiency.
  - Supports cross-dataset work within the Wessex BESS framework, particularly integration with landscape-scale pollinator surveys.
  - Provides a well-documented basis for creating data products (dashboards, summaries, or exploratory analyses) to explore pollinator effectiveness in OSR systems.