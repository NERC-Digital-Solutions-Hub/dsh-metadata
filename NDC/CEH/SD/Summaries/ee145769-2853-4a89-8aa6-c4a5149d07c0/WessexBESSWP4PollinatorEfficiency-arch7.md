# Pollinator effectiveness in oilseed rape ( Brassica napus L.) in relation to behavioural and morphological characteristics .

- The dataset investigates how pollinator behavior and morphology influence pollen delivery to oilseed rape, with quantitative measures of pollen deposition and body-borne pollen.
- Context: Part of the Wessex BESS project (NERC-funded) and can be used alongside landscape-scale pollinator datasets.

## Study design, location, and timeframe

- Location: Wiltshire, UK (central point 51.185988° N, -1.832657° W).
- Timeframe: Data collected April–June over three field seasons (2014–2016).
- Fields: 15 fields of winter sown oilseed rape.
- Data linkage: Data can be integrated with other Wessex BESS pollinator datasets (notably landscape-scale surveys).

## Methods and data collection

- Field observation and sampling:
  - Flowers inspected for ripe anthers and receptive stigma; suitable flowers collected with care to prevent pollen transfer.
  - Visitor identification: species-level when possible; otherwise morphotype to at least family level.
- Visitor presentation methods:
  - Bouquet method for solitary bees, bumblebees, honeybees.
  - Plastic box method for beetles, flies, sawflies.
- Visit recording:
  - Visit duration (seconds) and visit type: probing, crawling, or short contact.
  - Post-visit handling: visitor captured for pollen analysis or released after the visit if not captured.
- Controls:
  - Control flowers collected and stigmas prepared without visits to assess baseline pollen transfer (median 11 pollen grains on control stigmas).

## Measurements and variables

- Pollen deposition (SVD):
  - Stigmas cut, prepared, and pollen grains counted under a microscope (x20).
- Pollen loads on pollinators:
  - Swabbing of head, top thorax, tarsi, and bottom thorax with fuchsin jelly; counts of pollen grains per body part.
  - Tarsi not swabbable for very small beetles and excluded.
- Morphological traits:
  - Body length, intertegular distance (ITD) or proxies (elytra width for some beetles).
  - Hair density on the thorax and hair type (branched/feathery, smooth, or no hair).
- Additional variables:
  - Functional group, visit method, date, pollinator ID, and taxonomic details.
- Data structure:
  - Two linked data files: NERCPollinatorEfficiency and NERCPollenSwab, with cross-linking via PollinatorID.

## Data quality assurance and missing data

- Protocol adherence:
  - Standardized field and lab protocols; data entered in MS Access; anomaly checks performed.
  - Training provided for consistent protocol execution.
- Missing data and notes:
  - PollinatorID 94 missing species-level data (only genus-level identified).
  - Several fields use coded descriptions (e.g., species codes, functional groups) to standardize data.
  - Some measurements (e.g., tarsi pollen counts) not possible for very small species, resulting in NA values.

## Datasets and linkage

- Files:
  - NERCPollinatorEfficiency: records of pollinator visits, pollen deposition on stigmas, visit details, and associated species/morphology data.
  - NERCPollenSwab: pollen counts from body-part swabs, linked to PollinatorID.
- Linkage:
  - Datasets can be linked to each other and to the broader Wessex BESS pollinator dataset via PollinatorID and FunctionalGroupPollSwab fields.

## Practical implications for GIS and map-based data products

- Spatial context:
  - Field locations and collection points enable mapping of pollinator activity and pollen transfer across landscapes.
- Data integration:
  - Rich attribute data (behavior, morphology, pollen metrics) can be joined with spatial layers (land cover, crop fields) for spatial analyses of pollination services.
- Potential applications:
  - Visualizing spatial patterns of pollen deposition by species or functional groups.
  - Linking pollen delivery efficiency to habitat features and field-scale management practices.
  - Supporting landscape-scale assessments of pollination services in oilseed rape.