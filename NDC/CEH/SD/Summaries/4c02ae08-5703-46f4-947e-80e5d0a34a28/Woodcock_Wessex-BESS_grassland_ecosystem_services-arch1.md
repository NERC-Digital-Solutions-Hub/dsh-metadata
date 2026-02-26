# Experimental data on herbivorous pest insects, predatory insect occurrence and population growth rates of artificially established aphids from three crops.

- Aim and context
  - Evaluate whether different grassland types (improved, restored, species-rich) provide natural pest control ecosystem services.
  - Focus on interactions among herbivorous pests, their predators, and aphid population growth on sentinel crops.

- Study design and setting
  - Location and program: Salisbury Plain, UK; 2013; part of the Wessex Biodiversity Ecosystem Services Sustainability (BESS) project within NERC BESS.
  - Farms and fields: five farms, total of 15 fields (3 fields per farm) with three grassland treatments replicated on each farm.
  - Grassland treatments:
    - Agriculturally improved (low diversity) MG6 / MG7
    - Restored to high plant diversity within the last 10 years
    - Species-rich CG2 or CG3 grasslands with no recent agricultural improvement
  - Management: all grasslands grazed (not cut).

- Sentinel plant setup and crops
  - Crops used: oilseed rape, wheat, field beans.
  - Sentinel plants per field: oilseed rape (3 pots), wheat (3 pots with 10 tillers each), field beans (3 pots with 3 plants each).
  - Establishment: greenhouse-grown to align flowering/seed set with field conditions; placed on site starting 2 June 2013.

- Inoculation and observations
  - Aphid inoculation: subset of plants inoculated with aphids on field beans (Aphis fabae) and wheat (Rhopalosiphum padi) to assess aphid population growth under local predator pressure.
  - Aphid monitoring: weekly counts (to nearest 10 due to large numbers) from late June to mid-July 2013.
  - Predator sampling: four sampling dates in June 2013; hand sorting to identify free-living predators (targeting spiders, Coccinellidae, predatory beetles; also other predators).
  - Pest sampling: parallel counts of pest species on sentinel plants on the same dates as predator sampling.
  - Plant diversity: five 1×1 m quadrats per site to estimate percent cover of vascular plants; assessments conducted 16–19 July 2013.

- Data collection and quality assurance
  - Data were checked for anomalous values post-entry; invertebrate IDs verified against museum material (Oxford University Museums of Natural History).

- Datasets and metadata
  - Plants_2013.csv: site-level mean percent cover by plant species; key fields include Species, Site, Treatment (I=improved, R=restored, SR=species-rich), Cover_% (percentage).
  - Aphid_2013.csv: aphid counts on sentinel crops; fields include Date, Days_exp, Crop, Site, Treatment, Aphid_ave (average aphids per site/plant).
  - Predator_2013.csv: mean predator counts per site; fields include Species, Site, Treatment, N_average.
  - Herbivore_2013.csv: mean pest counts feeding on sentinel plants; fields include Site, Treatment, Crop, Species, N_average.
  - Metadata scope: each dataset provides site-level data and explicit treatment classifications to enable cross-dataset analyses and potential integration into data portals with proper metadata.

- Analytical opportunities and relevance
  - Correlate grassland type with predator abundance and aphid/pest dynamics to evaluate natural pest control potential.
  - Assess how plant community diversity relates to predator presence and pest suppression.
  - Enable cross-dataset analyses linking plant composition (Plants_2013.csv) with aphid growth (Aphid_2013.csv) and predator activity (Predator_2013.csv) across field sites (Site) and treatments (Treatment).