# Abstract

## Purpose and scope
- Presents data from the NERC project on effects of artificial light at night on a multi-trophic insect-plant-parasitoid food web.
- Aims to scrutinise how different light intensities affect ecological interactions and to inform future monitoring decisions.

## Study system and design
- Field site and controlled-temperature lab room at Penryn Campus, University of Exeter.
- Randomized block design with 6 blocks and eight light treatments: control (no light) plus 0.1, 1, 5, 10, 20, 50, 100 lux at plant height.
- 48 mesocosms (cages) containing experimental plant–insect communities.
- Plant species: broad bean (Vicia faba) and barley (Hordeum vulgare); aphids: Aphis fabae, Acyrthosiphon pisum, Megoura viciae; parasitoids: Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae; generalist parasitoid Praon dorsale linking to multiple aphids.
- Field observations weekly from week 1 for 9 weeks; plant biomass measured at end of the experiment (48 h at 50°C).

## Data collected and measures
- Insect counts for all species (winged and unwinged aphids where recorded).
- Parasitoid attack outcomes: mummy counts (successful attacks).
- Parasitoid behavior under varying light intensities.
- Plant biomass (dry weight) for mesocosms with and without insects.

## Experimental conditions and timeline
- Additional experiment to assess light effects on plants without aphids (30 mesocosms; 3 weeks total).
- Parasitoid behavior experiments conducted under different light treatments, including complete darkness and graded lux levels (0.1–100 lux).
- Behavioral setups included multiple cage experiments to test location preferences and attack rates under day/night and light conditions.

## Data management, quality control, governance
- Data entry verification with comparison to hard copies.
- Details of data structure documented across eight files.
- Metadata and variable naming conventions provided to aid reuse and interpretation.

## Data structure and fields
- Eight data files cover: insect population dynamics, plant biomass (with and without insects), and parasitoid behavior/attack rates.
- Key fields and codes include:
  - ab.factor (counting proportion within cages)
  - Block and Mesocosm identifiers
  - Treat.lux and Light.lux (light treatment levels)
  - Abundance variables for Megoura viciae (M.v), Acyrthosiphon pisum (A.p), Aphis fabae (A.f), Sitobion avenae (S.a)
  - Parasitoid counts (Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae)
  - Praon dorsale attacks on each aphid species
  - Plant biomass (plantbiomass.g)
  - Mummy counts (Aphid.mummies) as a measure of successful attacks
  - Parasitoid.Location indicators (Parasitoid.on.plant, Parasitoid.on.side.of.cage, Parasitoid.ceiling)
  - Temporal and experimental condition indicators (First, Light.Dark)

## Accessibility and usage notes
- Underlying data are designed for transparency and reuse in policy-relevant monitoring, with explicit data governance and sharing considerations.
- Some plant biomass data have missing labels, illustrating practical data integrity challenges in complex field/lab studies.
- Data are organized to support cross-study integration and multi-trophic monitoring evaluations.

## Relevance to monitoring frameworks and policy
- Demonstrates a robust, multi-trophic monitoring design linking environmental Driver (artificial light) to ecological responses across insects, plants, and parasitoids.
- Highlights practical governance needs: metadata completeness, data standardization, data cleaning, and openness of underlying data for policy evaluation and decision-making.
- Illustrates common barriers for monitoring authors: data access delays, siloed datasets, full public sharing of datasets, and ensuring up-to-date data and metadata, all of which require clear governance and data management at the source.