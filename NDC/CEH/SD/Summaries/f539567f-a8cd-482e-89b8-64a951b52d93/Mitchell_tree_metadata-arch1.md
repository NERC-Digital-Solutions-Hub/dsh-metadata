# Functional and epiphytic biodiversity differences between nine tree species in the UK

- Global concern about pests and pathogens in trees and potential functional changes if species decline; study examines how biodiversity and ecosystem functions (through bryophytes and lichens) vary among tree species.
- Uses six sites across the UK with multiple tree species per site to compare functioning and biodiversity for three UK-threatened species (Quercus petraea, Q. robur, Fraxinus excelsior) and six candidate replacements (Acer pseudoplatanus, Castanea sativa, Fagus sylvatica, Quercus cerris, Quercus rubra, Tilia x europaea).

## Study design, sites, and scope

- Sites: six UK locations with historical management and diverse habitats (Knightshayes Court, Bodnant, Dinefwr, Westonbirt, Crathes, Mount Stuart).
- Trees: 230 trees sampled across sites (roughly 35–40 per site); nine species total (three native threatened oaks and ash; six replacement species).
- Habitat around trees: categorized as semi-natural woodland, grassland/parkland, or garden.
- Tree data collection: recorded DBH, height, GPS/grid coordinates, slope/aspect, canopy around tree, and whether bark samples were taken.

## Tree and habitat data collected

- Bark and trunk data: bark pattern, ridges and furrows, bark hardness, bark depth and structure.
- Canopy data: percent canopy cover around tree from four cardinal directions.
- Proximal environment: distance to nearest tree within 30 m and species of that neighbor.
- Additional attributes: whether the tree was in hollow or knoll locations; whether tissue samples (bark) or soil samples were collected.

## Functional and soil measurements

- Decomposition experiments: four Whatman filter papers placed in nylon bags near each tree; monitored burial duration and weight loss to derive decomposition rates (K values).
- Soil temperature: hourly soil temperatures recorded near each tree using i-Buttons (DS1922L) placed 3 m south of the tree.
- Soil sampling: eight soil cores per tree (100 mm depth) around the trunk; samples split for mineralized N analysis and for pH, total C and N, and related measures.
- Soil analyses: 
  - pH in water (pHH2O) and CaCl2 (pHCaCl2)
  - Loss on ignition (LOI) at 450°C
  - Total C and N
  - Mineralizable N (N-Min), and inorganic N forms (TON-N_BI, NH4-N_BI, TON-N_AI, NH4-N_AI)
- FTIR: Fourier-transform infrared spectroscopy on ball-milled soil samples with pre-processing to enhance discrimination of species and locations; data stored per tree.
- Bark chemistry: assessment of bark water holding capacity, pH, and conductivity via bark samples processed and analyzed in lab.
- Bark physical characteristics: per-quadrat measurements around trunk (30x30 cm) at four heights; recorded bark pattern, fissures/ridge shapes, bark hardness (durometer), and related structural features.

## Lichen and bryophyte biodiversity data

- Lichen and bryophyte surveys conducted on the trunk from ground level to 1.75 m, with supplementary data on branches where possible.
- Presence/absence data collected for bryophytes and lichens; species names and authorities maintained in separate reference files; data linked to trees via taxon codes.

## Data organization and metadata

- Data structured as a relational database (Microsoft Access) with:
  - Central table: Trees (ANS_Tree_code)
  - Linked tables: Habitat_structure, Decomposition, Temperature, Soil, FTIR, Bark_chemistry, Bark_plot, Bryophytes, Lichens
  - Names tables: Bryophyte_names, Lichen_names
- Each table includes metadata describing variables (Tables 1–14 describe data contents and variable definitions).
- A schematic (Figure 1) illustrates the relationships between files and how to recreate the relational database.

## Key data tables and contents (overview)

- Table 1: Site details (location, soil type, climate data)
- Table 2: Counts of trees by species per site
- Table 3: Tree description fields (species, tags, GPS, DBH, height, date, notes)
- Table 4: Habitat structure data around each tree
- Table 5: Decomposition data (litter bag experiments and measurements)
- Table 6: Soil temperature data
- Table 7: Soil chemistry data (pH, LOI, N and C metrics, inorganic N and mineralizable N)
- Table 8: FTIR data descriptors
- Table 9: Bark chemistry metrics (water holding capacity, pH, conductivity)
- Table 10: Bark plot measurements (pattern, fissures, ridges, durometer, etc.)
- Table 11–14: Bryophyte and Lichen taxon references and presence data per tree

## Access, acknowledgments, and references

- Access: Data organized for discoverability and reuse via the relational database framework; metadata available to interpret and reuse datasets.
- Funding: Defra through the PuRpOsE BBSRC grant; additional Scottish Government support for RJM.
- References: Key methodological and ecological sources cited for soil, bark, and decomposition analyses (e.g., Allen 1989; McLean 1982; Pella & Colombo 1973; Ellis et al. 2015).