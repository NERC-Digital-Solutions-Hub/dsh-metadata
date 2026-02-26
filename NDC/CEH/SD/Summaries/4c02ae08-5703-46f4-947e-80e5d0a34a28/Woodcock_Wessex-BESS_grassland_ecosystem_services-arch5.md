# Experimental data on herbivorous pest insects, predatory insect occurrence and population growth rates of artificially established aphids from three crops.

## Overview
- Study assessing natural pest control ecosystem services provided by different grassland types (improved, restored, species-rich).
- Location and timeframe: 2013, five farms in Salisbury Plain, UK; part of the Wessex Biodiversity Ecosystem Services Sustainability (BESS) project within NERC.
- Focus: sentinel plants of field bean, wheat, and oilseed rape exposed to local predator communities to monitor herbivores, predators, and aphid population growth.

## Experimental design and data collection
- Grassland treatments:
  - Agriculturally improved (low diversity) MG6/MG7
  - Restored to high plant diversity within last 10 years (UK agri-environment scheme)
  - Species-rich (CG2/CG3) not agriculturally improved in last 50 years
- Field layout: 3 farms × 3 fields per farm × 3 grassland treatments = 15 fields; minimum 10 km between farms.
- Sentinel plants per field:
  - Oilseed rape: 3 pots (one plant per pot)
  - Wheat: 3 pots (10 tillers per pot)
  - Field beans: 3 pots (three plants per pot)
- Inoculation and monitoring:
  - Wheat and field beans inoculated with aphids (wheat: Rhopalosiphum padi; field bean: Aphis fabae) on subset of plants to assess impacts from local predators.
  - Aphid counts conducted weekly; predator and pest observations also recorded.
  - Plant diversity assessments conducted in each grassland field.
- Sampling methods:
  - Free-living predators (spiders, Coccinellidae, predatory beetles) identified via hand sorting and observation on four sampling dates.
  - Pest species counts collected alongside predator sampling.
  - Plant community composition measured using five 1×1 m quadrats per site.

## Data files and metadata
- Plants_2013.csv: site-level mean percent cover of all vascular plants; fields include site, treatment (I=improved, R=restored, SR=species rich), and cover percentage per species.
- Aphid_2013.csv: site-level mean aphid counts on sentinel plants; fields include date, days in field, crop type (field bean or wheat), site, treatment, and average aphid counts.
- Predator_2013.csv: site-level mean predator counts; fields include site, treatment, predator species, and average counts.
- Herbivore_2013.csv: site-level mean counts of herbivores feeding on sentinel plants; notes deer damage causing data loss in oilseed rape; fields include crop type, site, treatment, and mean herbivore counts.
- Metadata structure: each file includes descriptive fields (species names, site identifiers, treatment codes, units) and detailed descriptions for variables to support usability and interoperability.

## Data quality and provenance
- Quality checks: anomalous values screened after data entry.
- Taxonomic verification: invertebrate identifications validated against museum reference material (Oxford University Museums of Natural History).
- Documentation: metadata provided for all datasets with clear variable descriptions, units, and data provenance.
- Data completeness challenges: deer damage led to missing data in Herbivore_2013.csv; gain in metadata clarifies context and limitations.

## Governance, access, and use
- Data are organized to support discovery and reuse by researchers, land managers, and policy makers interested in natural pest control services across grassland types.
- Clear governance through standardized metadata, consistent variable naming, and documented collection protocols to enable cross-site comparisons and potential aggregation with other BESS datasets.
- Practical implications for data stewards:
  - Ensure ongoing updates and consistency across datasets (e.g., align site identifiers, treatment codes, and date formats).
  - Maintain provenance records and QA notes to facilitate reproducibility.
  - Flag and document data gaps or caveats (e.g., deer-related data loss) to support accurate interpretation.