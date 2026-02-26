# Experimental data on herbivorous pest insects, predatory insect occurrence and population growth rates of artificially established aphids from three crops

## Overview
- Field study (2013) in Salisbury Plain, UK, assessing whether grassland types (improved, restored, species-rich) provide natural pest control ecosystem services.
- Sentinel plants of three crops (field bean, wheat, oilseed rape) used to monitor herbivorous pests, predatory insects, and aphid population growth.
- Part of the Wessex Biodiversity Ecosystem Services Sustainability (BESS) project within NERC BESS programme.

## Study design and context
- Grassland treatments:
  - I = agriculturally improved (low diversity, MG6/MG7)
  - R = restored to high plant diversity within last 10 years (agri-environment scheme)
  - SR = species-rich grassland not agriculturally improved in last 50 years
- 3 farms, fields replicated across farms (15 fields total; 3 fields per farm, one per grassland type)
- Sentinel plants established on 15 fields on 2/6/2013
- Crops: oilseed rape (3 pots), wheat (3 pots with 10 tillers), field beans (3 pots with 3 plants)

## Methods and data collection
- Plant preparation: greenhouse-grown to align phenology; then placed in field sites and allowed to reach full development.
- Aphid inoculation: subset of plants inoculated with aphids for pest-pressure evaluation
  - Wheat: Rhopalosiphum padi
  - Field bean: Aphis fabae
  - Inoculation: 5 aphids per pot; 2 field beans per pot and 5 wheat tillers per pot
- Monitoring:
  - Aphid populations: weekly counts (to nearest 10 during peak counts 25/6–15/7/2013)
  - Predator sampling: four dates (mid-June 2013); hand sorting 5 minutes per plant cluster; focus on spiders, Coccinellidae, predatory beetles
  - Pest sampling: counts of pest species on sentinel plants during same dates
  - Plant community composition: five 1×1 m quadrats per site; tallied vascular plant cover (vertical projection)
- Quality assurance: data checked for anomalies; invertebrate IDs verified against Oxford University Museums of Natural History collections

## Data and metadata
- Plants_2013.csv: site-level mean percentage cover for plant species; fields include Species (Latin name), Site, Treatment (I/R/SR), Cover_% (continuous)
- Aphid_2013.csv: site-level mean aphid counts; fields include Date, Days_exp, Crop (field bean or wheat), Site, Treatment, Aphid_ave
- Predator_2013.csv: site-level mean predator counts; fields include Site, Treatment, N_average
- Herbivore_2013.csv: site-level mean herbivore counts on sentinel plants; fields include Site, Treatment, Crop, N_average
- Metadata structure: each dataset contains identifiers for Site, Treatment (I=improved, R=restored, SR=species rich) and relevant measurement units (percentage cover, counts, dates)

## Quality assurance and data validation
- Anomalies checked after data entry
- Taxonomic identifications validated against museum reference material

## Data governance and accessibility considerations for Data Leaders
- Clear, structured metadata with documented field meanings, units, and coding for treatments
- Consistent site and treatment identifiers to support integration with broader datasets
- Data quality checks and taxonomic verification documented
- Data collected across multiple farms and fields to support generalizability, with explicit sampling dates and procedures

## Limitations and caveats
- NA data in Herbivore_2013.csv due to deer damage to some plants (oilseed rape)
- Counts subjected to rounding during peak aphid periods (25/6–15/7/2013)
- Temporal window limited to specific dates in 2013; spatial replication restricted to five farms within a region
- Focus on sentinel plants may not capture all field-scale interactions

## Potential applications for data leaders
- Assess effectiveness of different grassland types in providing natural pest control across crops
- Inform design of agri-environment schemes and biodiversity-friendly farming practices
- Integrate with larger datasets on ecosystem services, metadata standards, and data discoverability to support cross-institution collaboration
- Use the detailed metadata and standardized fields to improve data stewardship, interoperability, and long-term reuse in policy and research networks