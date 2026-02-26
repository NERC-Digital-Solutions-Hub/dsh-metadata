# Pollinator effectiveness in oilseed rape ( Brassica napus L.) in relation to behavioural and morphological characteristics

## Overview
- Dataset from the Wessex BESS project aimed at assessing the number of pollen grains delivered in a single visit by various pollinators to oilseed rape (Brassica napus L.).
- Includes linked behavioural and morphological data to identify traits associated with improved pollen delivery.
- Designed to be used alongside landscape-scale pollinator datasets within the Wessex BESS program.

## Field study and sampling
- Location: Wiltshire, UK (central point 51.185988° N, -1.832657° W).
- Timeframe: April–June over three field seasons (2014–2016).
- Fields: 15 fields of winter sown oilseed rape.
- Experimental controls: Control stigmas collected and processed to control for handling and wind pollination; median pollen on control stigmas was 11 (range 0–99, n=31).

## Experimental design and collection methods
- Flower visitation observations and collection methods varied by visitor type:
  - Bouquet method for solitary bees, bumblebees, and honeybees.
  - Plastic box method for beetles, flies, and sawflies.
- For each flower visit:
  - Recorded visit duration (seconds) and visit type (probing, crawling, short).
  - Visitor was subsequently captured (or morphotype recorded if not captured) and stored for pollen analysis.
- Flower handling minimized pollen transfer from anthers to stigma during setup.

## Measurements and variables
- Pollen deposition (SVD):
  - Stigmas were split and processed to count total pollen grains (SVD) under x20 magnification.
- Pollen loads on pollinators:
  - Pollen swabs collected from head, top of thorax, tarsi, and bottom of thorax (15 strokes per site; jelly samples prepared for microscopy).
  - Tarsi swabbing excluded for very small beetles due to size limitations.
- Morphological traits:
  - Body length (front of eyes to tip of abdomen).
  - Intertegular distance (ITD) as a proxy for body size (or alternative proxy for some beetles).
  - Hair density on the thorax surface (percentage, assessed in 5% increments).
  - Hair type (Branched/feathery, Smooth, No_hair).
- Species and visitor information:
  - Taxonomic identification to genus/species where possible; functional groups assigned based on size/behavior.
  - Visit type and duration linked to pollinator identity when available.

## Data processing and quality assurance
- Protocols:
  - Field and laboratory data collection followed standardized protocols; data entered in MS Access.
  - Training provided to ensure consistency.
- Data management:
  - Two primary data files: NERCPollinatorEfficiency and NERCPollenSwab.
  - Collected data linked to other Wessex BESS pollinator datasets via identifiers (e.g., functional group linkage).
- Documentation:
  - Extensive metadata described for each field and laboratory variable to enable reuse and integration with other datasets.

## Datasets and linkage
- NERCPollinatorEfficiency:
  - Contains measures of pollen deposition per visit (SVD) and associated visit-level details (visit duration, visit type, pollinator identity).
- NERCPollenSwab:
  - Contains pollen counts from body-part swabs (head, back, feet, underside) to quantify pollen loads carried by pollinators.
- Linkages:
  - Datasets can be linked using PollinatorID; PollSwab linkage enables integration with the broader Wessex BESS Pollinator survey data (FunctionalGroupPollSwab provides linking codes).

## Missing data and limitations
- Missing data:
  - PollinatorID for one individual (94) could only be identified to genus; affected species-level and morphological trait analyses.
  - Several metadata fields (SpeciesCode, Description; PollinatorID, Description; Family, Description; VisitorType, Description; FunctionalGroup, Description; etc.) include missing or non-standard entries.
  - Some body-part swab data (Feet) have NA values (7 values) due to tarsi measurement constraints for small beetles.
- Data completeness:
  - Not all individuals could be measured for all morphological traits; proxies (e.g., ITD) used when species data were limited.
  - Some fields use category codes or descriptions that require careful interpretation to ensure consistent cross-dataset linkage.

## Data sharing and usage notes
- The dataset is designed to be used in conjunction with other Wessex BESS data, enabling landscape-scale and species-level analyses of pollinator effectiveness.
- While sharing is possible and encouraged to support monitoring and policy evaluation, users should account for missing metadata and potential measurement limitations when integrating with other datasets.