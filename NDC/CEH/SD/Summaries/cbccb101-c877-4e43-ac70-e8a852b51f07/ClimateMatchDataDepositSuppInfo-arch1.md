# Experimental Field Sites.

- Location and scope
  - Conducted at two UK field sites: Hucking, Kent (South East England) and Hartshorne, Derbyshire (East Midlands).
  - Part of TreeDivNet, a global network of tree diversity experiments.
  - Focused on Quercus robur (oak) with four provenances; trial includes climate-matched provenances from France and Italy and local UK provenance variants.

- Experimental design
  - Planting year: 2011 using two-year-old saplings.
  - Layout: three experimental blocks per site; plots within blocks contain either monocultures or mixtures of provenances/species.
  - Treatments for oak only (within plots)
    - Monocultures: Local, French, Italian provenances.
    - 50:50 mixtures: Local:French; Local:Italian.
    - 75:25 mixtures: Local:French; Local:Italian.
    - 33:33:33 mixture: Local:French:Italian.
    - Mixed species plots: Local and Italian provenances for each of the four species (in this study focusing on oak).

- Planting geometry and plot sizes
  - Monocultures and mixed provenance plots: 12 m x 12 m, 36 trees per plot (4 m spacing, 6 rows of 6).
  - Mixed species plots: 36 m x 32 m, 288 trees (16 rows of 18).
  - Design ensures different provenances/species are interspersed within plots.

- Study system and measured organisms
  - Insect guilds: cynipid gallwasps (gallers), leaf miners, and leaf manipulators (free-feeding herbivores, including generalists and specialists).
  - Pathogen: oak powdery mildew (biotrophic pathogen) caused by Erysiphe species; focus on E. alphitoides as prevalent in the UK.
  - Temporal dynamics: herbivory on primary shoots in late spring; powdery mildew on lammas shoots (second flush) in June–August. Leaves on primary shoots are typically uninfected when mildew peaks on lammas shoots.

- Sampling and tree selection
  - Nine oak trees of each provenance per plot chosen for data collection.
  - Sampling across plot core outward at each site/year.
  - Sampling years: 2016 (Hucking) and 2017 (Hucking and Hartshorne); total trees sampled: 411 (Hartshorne), 420 (Hucking in 2016), 416 (Hucking in 2017).
  - Mortality influenced the final counts at Hucking.

- Measurements and covariates
  - Oak powdery mildew
    - Timing: August; 10 lammas shoots per tree scored.
    - Scoring: 0–3 severity scale based on percent of leaf material infected (0 = 0%, 1 < 50%, 2 51–75%, 3 76–100%).
    - Covariate: lammas shoot length (mm).
  - Insect herbivores
    - Timing: August; 10 primary shoots per tree surveyed.
    - Counts: leaf mines, galls (on leaves and buds), and incidences of leaf skeletonisers, leaf rollers, and leaf webbers on all leaves of the sampled shoots.
    - Covariate: primary shoot length (mm).
  - Tree height and apparency
    - End of August 2017: height measured for focal trees and 27 additional random trees per plot.
    - Apparency index: ((Height of focal tree – Average height in plot) / Average height in plot) × 100.

- Data structure and recorded variables
  - Site: Hartshorne or Hucking.
  - Year: 2016 or 2017.
  - Provenance: codes include Local_UK2404, UK provenance 404, Local_Kent, French, Italy_Tuscany, Italy Ravenna (and related variants).
  - Block: experimental block within site.
  - Plot: plot within block.
  - Treatment: provenance-based and mixture treatments (e.g., Mono, P1P2_50, P1P2_75, P1P3_50, P1P3_75, Thirty-33_33_33, MixSp).
  - Tree Number: identifier within a plot.
  - PShootLength: mean primary shoot length (mm) across 10 shoots per tree.
  - LShootLength: mean lammas shoot length (mm) across 10 lammas shoots per tree.
  - LShootPM: mean powdery mildew infection score across 10 lammas shoots per tree.
  - Leaf.Manip: total leaf manipulator abundance across 10 shoots.
  - Leaf.Gallers: total leaf gall abundance across 10 shoots.
  - Leaf.Miners: total leaf miner abundance across 10 shoots.
  - TreeHeight: height of focal tree (cm).
  - MeanHeight: average height of a random sample of 28 trees per plot.
  - Apparency: apparency index as defined above.