# Functional and epiphytic biodiversity differences between nine tree species in the UK

## Overview
- Addresses global concerns about pests and pathogens affecting trees and potential shifts in ecosystem functions as species decline or are replaced.
- Aims to understand how tree species composition influences ecosystem functions and biodiversity, focusing on both functional processes and epiphytic communities (bryophytes and lichens).
- Comparative study across six UK sites, involving nine tree species (three UK taxa currently threatened by disease and six proposed ecological replacements).
- Variables cover soil processes, bark chemistry and physical traits, and epiphytic communities, enabling assessment of potential changes in functions and biodiversity with species turnover.

## Study design and sites
- Six sites across the UK: Knightshayes Court (England), Bodnant (Wales), Crathes (Scotland), Dinefwr (Wales), Westonbirt (England), Mount Stuart (Scotland).
- Sites chosen for historical management and presence of multiple tree species; old trees (often >150 years) in gardens/parks.
- Sampling includes 230 trees in total (roughly 35–40 trees per site) across nine species:
  - Acer pseudoplatanus, Castanea sativa, Fagus sylvatica, Fraxinus excelsior, Quercus cerris, Quercus petraea, Quercus robur, Quercus rubra, Tilia x europaea.
- For each tree: DBH and height measured; GPS coordinates recorded; surrounding habitat categorized; trees distributed across four cardinal sectors for local context.

## Data collected and variables
- Tree and site data
  - Tree species, unique ANS_Tree_code, site, GPS/grid coordinates, DBH, height, date of recording, observer, and habitat context (semi-natural woodland, grassland/parkland, garden).
  - Bark sampling flag and litter decomposition setup (litter bags and sticks buried near each tree).
- Habitat structure
  - Distance to nearest neighboring tree within 30 m; girth of nearby tree; sectoral context around each tree.
- Decomposition
  - Litter bags containing four filter papers buried 3 m south of each tree; time buried, paper and stick weights, decomposition rates (K_paper, K_stick), and notes.
- Soil temperature
  - Hourly soil temperature near decomposition site (3 m south of each tree) using temperature loggers.
- Soil chemistry and nutrients
  - Eight soil samples per tree, analyzed for:
    - Loss on ignition (LOI), pH (H2O and CaCl2), total carbon (C) and nitrogen (N).
    - Mineralizable nitrogen (N-Min) and related oxidized nitrogen (TON-N_BI, NH4-N_BI, TON-N_AI, NH4-N_AI).
    - Total N and C by weight.
- FTIR
  - Fourier-transform infrared (FTIR) spectra of ball-milled soil samples, processed with derivatives and baseline corrections; data and metadata provided.
- Bark chemistry and physical characteristics
  - Bark samples analyzed for water holding capacity, pH and conductivity of bark slurry, density; bark chemistry data stored.
  - Bark physical traits recorded in a 30 x 30 cm quadrat at four heights per tree, including:
    - Bark pattern, fissure types and shapes, furrow and ridge measurements (width, depth), ridge pattern, bark hardness (durometer), and related notes.
- Lichen and bryophyte data
  - All bryophyte and lichen species on the trunk from ground to 1.75 m recorded; limited branch/ twig sampling where accessible.
  - Taxon names and authorities maintained; presence/absence data for trunk, branches, twigs, and occurrences limited by accessibility.
- Data structure and access
  - Data organized as a relational database with multiple tables linked to a central Trees table via ANS_Tree_code.
  - Key files/tables include Trees, Habitat_structure, Decomposition, Temperature, Soil, FTIR, Bark_chemistry, Bark_plot, Bryophytes, Lichens, along with taxon name tables (Bryophyte_names, Lichen_names).
  - Access via a Microsoft Access database diagram and metadata tables describing each dataset.

## Data management and access
- The dataset is designed for standardized cross-site comparisons and reproducibility.
- Acknowledges the importance of storing and enabling access to underlying data to support outputs and policy-relevant interpretation.
- Funded by Defra through PuRpOsE (plus additional Scottish Government support).

## Relevance for environmental monitoring and policy
- Provides a comprehensive, standardized dataset to monitor how tree species composition affects ecosystem functions (soil processes, decomposition, bark traits) and epiphytic biodiversity (lichens and bryophytes).
- Supports evaluation of ecological replacements for disease-threatened UK oaks and ash, informing policy on forest management and biodiversity conservation.
- Enables time-series style assessments and spatial comparisons to detect environmental health trends and the implications of species turnover on function and biodiversity.

## Challenges and considerations for analysts
- Emphasizes increasing the value of datasets by integrating with other relevant environmental data.
- Highlights the need to enable access to underlying datasets used to produce final monitoring outputs.