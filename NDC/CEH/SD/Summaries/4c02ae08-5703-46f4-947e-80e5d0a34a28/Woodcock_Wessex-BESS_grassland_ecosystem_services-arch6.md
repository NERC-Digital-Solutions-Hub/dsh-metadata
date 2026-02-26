# Experimental data on herbivorous pest insects, predatory insect occurrence and population growth rates of artificially established aphids from three crops

## Summary at a glance
- Purpose: Assess the potential for different grassland types (improved, restored, species-rich) to deliver natural pest control ecosystem services by monitoring pests, predators, and aphid growth on sentinel crops.
- Timeframe and location: 2013, five farms on Salisbury Plain, UK; part of the Wessex Biodiversity Ecosystem Services Sustainability (BESS) project under NERC.
- Experimental setup: Sentinel plants of field bean, wheat, and oilseed rape placed in three grassland types; aphids inoculated on wheat and field beans; predator and pest activity recorded.
- Datasets included:
  - Plants_2013.csv: mean % cover of plant species per site
  - Aphid_2013.csv: aphid counts on sentinel plants
  - Predator_2013.csv: predator counts by site and species
  - Herbivore_2013.csv: herbivore counts on sentinel plants
- Data quality: QA checks conducted; invertebrate IDs verified against museum material.

## Study context and design
- Objective: Explore how grassland management and diversity influence natural pest control services.
- Grassland types (on 15 fields across 3 farms): 
  - Agriculturally improved (low diversity; MG6/MG7)
  - Restored to high plant diversity (within last 10 years)
  - Species-rich (CG2/CG3) grasslands not agriculturally improved in last 50 years
- Experimental replication: Three farms, each with three fields representing the three grassland types.
- Sentinel plants and inoculation:
  - Crops: field bean, wheat, oilseed rape
  - Sentinel setup: 3 pots per crop per field (beans: 3 plants per pot; wheat: 10 tillers per pot; oilseed rape: 1 plant per pot)
  - Inoculation: aphids introduced on wheat and field beans to monitor growth under local predator pressure
- Data collection: 
  - Predator and other herbivorous insects observed on sentinel plants
  - Plant diversity assessed in each grassland
  - Snapshots of predator and pest populations taken over multiple dates
  - Plant community composition measured with 5 quadrats per grassland
- Timeline: Establishment 2 June 2013; observational and sampling dates around 11–19 June and 16–19 July 2013; counts continued 25 June–15 July 2013 for aphids due to rapid growth

## Data structure and content
- Datasets (CSV files):
  - Plants_2013.csv
    - Site-level mean percentage cover for all plants within each of the 15 grassland sites
    - Fields: Species, Site, Treatment (I=improved, R=restored, SR=species-rich), Cover_% (continuous)
  - Aphid_2013.csv
    - Aphid counts on sentinel crops (wheat and field bean) by date and site
    - Fields: Date, Days_exp (days sentinel plant exposed), Crop (field bean or wheat), Site, Treatment, Aphid_ave (average aphids across plants)
  - Predator_2013.csv
    - Predator counts by site and predatory species
    - Fields: Species, Site, Treatment, N_average (mean predator count)
  - Herbivore_2013.csv
    - Counts of herbivores feeding on sentinel plants by site and crop
    - Fields: Species, Site, Treatment, Crop, N_average (mean herbivore count)
    - Notes: NA entries present due to deer damage affecting oilseed rape
- Metadata notes
  - Species fields use Latin binomials
  - Treatments encoded as I, R, SR
  - Units: cover percentages and count data as described above

## Quality assurance and provenance
- Data entry QA to identify anomalous values
- Invertebrate identifications verified against museum material (Oxford University Museums of Natural History)

## Usage considerations and potential analyses
- Compare how predator presence and herbivore counts vary across grassland types and sites
- Examine relationships between plant diversity ( Plants_2013.csv ) and pest/predator dynamics
- Assess aphid population growth in relation to local predator communities, across different grassland treatments
- Potential downstream products: site-level summaries, aggregated metrics by grassland type, and dashboards for self-serve exploration of pest-control dynamics

## Limitations and caveats
- Temporal scope limited to 2013 and specific sampling window; counts concentrated around peak aphid growth (late June–July)
- Deer damage affected oilseed rape data, introducing gaps (Herbivore_2013.csv)
- Field-scale replication limited to 5 farms and 15 fields, which may constrain generalization to broader landscapes
- Data are site-level averages; more granular intra-site variability exists but is not captured in the provided metadata