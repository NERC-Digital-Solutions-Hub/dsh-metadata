# Pollinator effectiveness in oilseed rape ( Brassica napus L.) in relation to behavioural and morphological characteristics

## Overview
- A dataset describing pollinator effectiveness in oilseed rape, focusing on the number of pollen grains delivered in a single visit (single-visit deposition, SVD) and related behavioural and morphological traits.
- Collected as part of the Wessex BESS project (NERC-funded) to complement landscape-scale pollinator surveys.
- Fieldwork conducted in Wiltshire, UK, over three seasons (April–June) from 2014 to 2016 across 15 winter sown OSR fields.
- Aims to link pollinator behaviour and morphology to pollen delivery, enabling integration with broader Wessex BESS datasets.

## Field site, timing, and scope
- Location: Wiltshire, central UK (approximate coordinates provided in study).
- Fields: 15 fields of winter oilseed rape.
- Timeframe: 2014–2016, April–June each year.
- Data types include: pollinator visits, pollen deposition on stigmas, pollen loads on pollinators, and morphological traits.

## Experimental design and data collection
- Flower visitation: OSR flowers inspected for ripe anthers and receptive stigmas; suitable flowers collected for testing.
- Visitor handling methods (vary by visitor type):
  - Bouquet method for solitary bees, bumblebees, and honeybees (flowers taped to a straw as a mobile bouquet).
  - Plastic box method for beetles, flies, and sawflies (flowers placed in a 1 cm straw segment and covered with a plastic container).
- Visit recording: duration of contact with reproductive parts and visit type (probing, crawling, or short contact).
- Specimen handling: visitors captured and transported for lab analysis; stigma removed and preserved for pollen assessment.
- Controls: control OSR flowers collected and stigmas prepared without visitation to control for handling and wind pollination.
- Core metrics:
  - Pollen deposition on stigmas (SVD) measured after stigma processing.
  - Pollen loads on pollinators obtained via jelly swabs from head, thorax, and legs, with counts under microscopy.
- Morphological data: body length, intertegular distance (ITD; or proxy for certain beetles), hair density on thorax, and hair type (branched, smooth, or none).

## Pollen deposition and pollen load measurements
- Pollen deposition (SVD): stigmas were halved, crushed, and pollen remaining counted under 20× magnification; small jelly cubes used to transfer detached pollen for counting.
- Pollen loads: swabs taken from predefined body parts (head, thorax top, tarsi, thorax underside); each part swabbed with jelly and pollen counted.
- Proxies and exclusions: tarsi counts excluded for very small beetles; ITD proxies used for some species where direct measurements were unavailable.

## Morphological traits and links to pollen data
- Traits measured to relate to pollen transfer efficiency:
  - Body length (from front of eyes to abdomen tip).
  - ITD (or proxies for certain beetle groups).
  - Hair density on the upper thorax (percent coverage, estimated in 5% increments).
  - Hair type (branched/feathery, smooth, or no hair).
- Purpose: investigate how size, body hair, and body surface area relate to both SVD and pollen loads.

## Data quality assurance and structure
- Protocols: standardized field and lab procedures; trained personnel conducted data collection.
- Data handling: entries captured in MS Access; routine anomaly checks.
- Files provided:
  - NERCPollinatorEfficiency: records of field visits, visitor identity, method, visit type, duration, pollen deposition (SVD), etc.
  - NERCPollenSwab: pollen counts from body-part swabs linked to corresponding PollinatorID.
- Data linkage: files can be linked via PollinatorID; PollenSwab and PollinatorEfficiency datasets are designed for integration with broader Wessex BESS pollinator datasets.

## Missing data and data dictionary notes
- Notable missing data:
  - PollinatorID 94 could only be identified to genus; species and morphological traits missing.
  - Some columns have NA values (e.g., Feet for tarsi data in small beetles).
- Data dictionary coverage:
  - Detailed column descriptions for both datasets include: PollinatorID, VisitorType, FunctionalGroup, MethodUsed, VisitType, LengthVisit, Date, body measurements (Body_Length, intertegular_distance), hair density/type, pollen counts (PolPerVis), swab indicators (PollSwab), and linked fields.
- Several fields reflect categorical coding (e.g., unique species codes, functional groups) and continuous measurements (e.g., pollen counts, lengths).

## Accessibility and potential analyses
- Datasets are designed to be compatible with the Wessex BESS pollinator survey data and can be linked across studies via PollinatorID (and FunctionalGroupPollSwab for cross-dataset linking).
- Potential analyses for researchers aligned with the Analysts archetype:
  - Correlations between SVD and pollen loads on different body parts.
  - Relationships between morphological traits (size, ITD, hair density/type) and pollen transfer efficiency.
  - Impact of visit type and behaviour (probing, crawling, short contact) on pollen deposition.
  - Integration with landscape-scale pollinator data to model how morphological and behavioural traits influence pollination success at larger scales.
- Limitations to consider:
  - Missing species-level data for at least one pollinator.
  - Proxies used for some ITD measurements; measurement variability across taxa.
  - Some data points missing or NA in specific body-part swab measurements.