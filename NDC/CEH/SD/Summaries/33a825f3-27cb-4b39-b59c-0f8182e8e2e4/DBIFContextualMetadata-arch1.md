# Summary

- A subset of the Database of Insect and their Food Plants (DBIF) is presented: 13,277 interactions at the species level, GB-only, expertly verified.
- Data are provided in two formats:
  - DBIFInteractionFrequencies.csv: frequency of interactions between insect species x and plant species y as reported by source z.
  - DBIFSummaryWithPlantTraits.csv: total number of insect species interacting with each plant species, plus plant trait information.
- Included plant traits in the summary data:
  - Native statuses: native, archaeophyte (pre-1500 non-native), neophyte (post-1500 non-native).
  - Plant distribution size (number of hectads, 1987–1999).
  - Time since introduction for neophytes.
  - Four phylogenetic isolation metrics for plants.
  - Distinctiveness of the insect community on non-native plants (relative to natives) for a subset with insect richness ≥ 10.

## DBIF overview and data products

- DBIF background: a comprehensive, historically curated list of British herbivorous invertebrates and their foodplants, drawing on major checklists, literature, and institutional resources; the database and its updates are maintained by the Centre for Ecology & Hydrology and partners.
- Subset scope: 4,397 insect species associated with 679 native plant species, 120 archaeophytes, and 234 neophytes after cleaning and trait assignment.
- Data products:
  - DBIFInteractionFrequencies.csv: records interaction frequency between each insect–plant pair by source.
  - DBIFSummaryWithPlantTraits.csv: per-plant summary with total insect richness and plant traits (native status, phylogenetic isolation metrics, distribution, introduction years, and distinctiveness).

## Plant traits and metrics included

- Native statuses:
  - N (native), ARCH (archaeophyte), NEO (neophyte).
  - Introduction dates used to compute “Years Since Plant Introduction” (for neophytes).
  - 78 plant species could not be reliably classified and were excluded; 19 hybrids excluded.
- Distribution size:
  - Measured as hectads (10 x 10 km grid squares) inhabited between 1987–1999 (Great Britain including the Isle of Man).
  - Plants with no data assigned a distribution size of zero (12 species).
- Phylogenetic isolation (four measures):
  - PI: mean divergence time from a plant to every other plant in the phylogeny.
  - NPN: nearest phylogenetic neighbour distance.
  - PIN: mean divergence time from a non-native plant to every native plant.
  - NPNN: nearest native phylogenetic neighbour distance.
- Insect community distinctiveness:
  - Chao-Sorensen abundance-based dissimilarity between the insect community on a non-native host and the insect pool on native plants.
  - Calculated only for plants with insect richness ≥ 10; includes natives (206), archaeophytes (30), neophytes (26).

## Data processing, curation, and scope considerations

- Taxonomic standardization:
  - Focus on higher plants (seed plants and ferns); records upgraded to species level; captivity/exclusion criteria applied to ensure natural occurrences.
  - Synonyms reconciled using BSBI, Stace, UKSI, Fauna Europaea, EPPO, etc.
- Native status and dating:
  - Native status assignment drawn from Stace & Crawley, PlantAtt, Stace (2010), with additional checks to resolve uncertainties.
- Phylogeny and sampling:
  - Phylogenetic relationships sourced from a global megaphyly to produce the plant phylogeny; some species replaced by polytomies if not in the base tree; a minority excluded due to missing phylogenetic placement.
  - Insect community distinctiveness relies on sufficiently sampled non-native host plants (insect richness ≥ 10) to be robust.
- Source consolidation:
  - DBIF data sources trimmed to article level (no page numbers) to support reproducibility; variable reporting across many sources (mean 6; median 3).

## Dataset scale (key figures)

- Interactions: 13,277 (subset from ~60,000 in DBIF).
- Insect species: 4,397.
- Plant species:
  - Native: 679
  - Archaeophytes: 120
  - Neophytes: 234

## Variable definitions (selected highlights)

- DBIFSummaryWithPlantTraits.csv:
  - Plant Species Name
  - Associated Insect Richness
  - Native Status (N, ARCH, NEO)
  - PI (mean plant–plant divergence time)
  - NPN (nearest plant neighbor distance)
  - PIN (mean divergence from non-native to natives)
  - NPNN (nearest native neighbor distance)
  - Hectads (GB hectads recorded)
  - Years Since Plant Introduction
  - Sources (count of articles reporting on the plant)
  - Distinctiveness (Chao-Sorensen dissimilarity vs native insect pool)
- DBIFInteractionFrequencies.csv:
  - Plant Species Name
  - Insect Species Name
  - DBIF Source
  - Interaction Frequency (count of reports by source)

## Data sources and references

- The dataset integrates numerous sources including:
  - Chao et al. 2005 (Chao-Sorensen dissimilarity)
  - de Jong et al. 2014 (Fauna Europaea)
  - EPPO Global Database
  - Hill et al. 2004 (PLANTATT)
  - Pearse et al. 2015 (pez phylogenetics)
  - Pescott et al. 2018 (British/Irish plant data guide)
  - Qian & Jin 2016 megaphylogeny
  - Ward et al. series (insect-host plant literature)
  - Stace 2010; Stace & Crawley 2015
  - Ward, Smith & Roy (DBIF foundational papers)
- Full references are provided with DOIs and access details in the document.

## Potential uses and analyst considerations

- Suitable for analyses of:
  - Correlations between plant native status or introduction timing and insect interaction richness.
  - Impact of plant phylogenetic isolation on associated insect communities.
  - Differences between insect communities on native versus non-native plants.
  - Predictive modelling of how future plant introductions could reshape insect-plant networks.
- Considerations and limitations:
  - Subset excludes many plants due to unknown native status or hybrids; potential bias in composition.
  - Phylogenetic placement challenges lead to some species being polytomous or excluded.
  - Distinctiveness metric requires adequate sampling (richness ≥ 10) on non-native hosts.
  - Data compiled from diverse sources with varying levels of detail; careful metadata tracking is advised.

## Access and reproducibility

- Data are hosted as part of the DBIF project; collection methods, trait assignments, and processing steps are detailed to support reproducibility and potential updates.