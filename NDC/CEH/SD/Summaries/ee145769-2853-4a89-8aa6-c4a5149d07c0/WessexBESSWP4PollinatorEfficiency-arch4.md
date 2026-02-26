# Pollinator effectiveness in oilseed rape ( Brassica napus L.) in relation to behavioural and morphological characteristics

## Overview
- Study within the Wessex BESS project (NERC funding) to assess pollen deposition by pollinators on oilseed rape (OSR) and relate deposition to visitor behavior and morphology.
- Fieldwork in Wiltshire, UK, across 2014–2016 (three field seasons) on 15 OSR fields.
- Data can be integrated with landscape-scale pollinator datasets from the same program.

## Data assets and structure
- Files: two primary data files
  - NERCPollinatorEfficiency
  - NERCPollenSwab
- Linkage: data can be linked to NERCPollinatorEfficiency via PollinatorID; includes additional metadata to support cross-dataset joins (FunctionalGroupPollSwab, etc.).
- Dataset scope: observations of flower visitors, pollen deposition on stigmas, and body pollen loads; collection of morphological traits to explain deposition variability.

## Data collection and lab processing
- Field methods
  - Locations: 15 fields of winter sown OSR in Wiltshire (central point 51.185988°N, -1.832657°W).
  - Timeframe: April–June, 2014–2016.
  - Flower visitation: observed and sampled visitors; two presentation methods depending on visitor type
    - Bouquet method for solitary bees, bumblebees, honeybees
    - Plastic box method for beetles, flies, sawflies
  - Recorded per flower visit: visit duration and visit type (probing, crawling, short).
  - Post-visit: visitors captured for lab analysis or morphotype identified to at least family level if not captured.
  - Controls: unvisited flowers processed to control for handling and wind pollination; median pollen on controls = 11 (range 0–99, n=31).
- Lab processing
  - Pollen deposition (SVD): stigma halved, pollen counted on slides under 20x magnification; counting detects OSR pollen.
  - Pollen loads (on body): swabs of head, top thorax, tarsi, and ventral thorax using fuchsin jelly; slides prepared and pollen counted.
  - Morphology: measured body length, intertegular distance (ITD; proxy for some taxa), and hair density (percent coverage); hair type categorized (Branched, Smooth, No_hair).
  - Data quality controls: standardized protocols; data entered in MS Access; QA checks and training provided.
- Data handling nuances
  - Some body parts (e.g., tarsi of very small beetles) could not be swabbed; recorded as missing for those cases.
  - For certain beetles, ITD proxies used; average species values applied when individual measures unavailable.

## Measurements and variables
- Visit-level: VisitType (P = probed, C = crawled, S = short), LengthVisit (seconds), VisitDate.
- Pollen deposition: PolPerVis (number of pollen grains on stigma after a visit).
- Pollen loads: Back, Feet, Head, Under (pollen grains on body parts from swabs).
- Morphological traits: Body_Length (mm), intertegular_distance (mm), hair_density_Per (percent), hair_type (Branched, Smooth, No_hair).
- Sampling and method metadata: MethodUsed (Bouquet, PB for plastic box), Date, SpeciesCode/Description, Poll Swab indicator, etc.
- Quality and linkage: FunctionalGroup, FunctionalGroupPollSwab, PollSwab (Y/N), VisitType definitions, and units.

## Data quality, gaps, and metadata
- Data quality assurance
  - Adherence to set field and lab protocols; documented training and QA processes.
  - Data stored in MS Access with anomaly checks.
- Missing data and limitations
  - PollinatorID missing for one field entry; some species and morph traits not available for all individuals.
  - Feet values missing for a subset due to measurement limitations on small beetles.
  - Some fields use proxies or averages (e.g., ITD for certain beetles; species-average values used when individual data unavailable).
- Documentation and usability
  - Rich metadata structure with explicit field definitions, units, and categorical codes.
  - Clear mapping between NERCPollinatorEfficiency and NERCPollenSwab for integrated analyses.

## Data governance, discoverability, and accessibility
- Data are organized to support cross-dataset discovery and integration within the Wessex BESS project ecosystem.
- Metadata include data provenance, measurement methods, units, and coding schemes to support reproducibility and reuse.
- Data assets are suitable for integration with landscape-scale pollinator surveys and other Wessex BESS datasets.

## Potential uses and cross-dataset integration
- Linking behavioral and morphological traits to pollen deposition to identify traits associated with higher pollination efficacy.
- Integrating with landscape-scale pollinator datasets to model spatial patterns of pollen delivery.
- Informing data-driven improvements in pollination service assessments within OSR cropping systems.
- Data leaders could use these assets to verify data suitability, address gaps (e.g., missing PollinatorID or species-level detail), and align metadata for broader data standards and interoperability.