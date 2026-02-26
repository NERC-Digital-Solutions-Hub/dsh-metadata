# Mark-Release-Recapture data showing moth and dung beetle movements in riparian reserves within the SAFE project landscape, Malaysian Borneo, 2016-17 [HMTF]. Gray, R.E.J, Slade, E.M., Chung, A.Y.C., Lewis, O.T.

## Overview
- Two CSV datasets: Moth_Movement.csv and Dung_Beetle_Movement.csv, from mark-release-recapture (MRR) experiments.
- Purpose: examine movement of moths and dung beetles in riparian forests embedded in oil palm landscapes to assess if riparian reserves provide habitat or movement corridors.
- Timeframe: November 2016–April 2017 (moths Nov 2016–Jan 2017; dung beetles Jan 2016–Apr 2017).
- Location: SAFE project landscape, south-eastern Sabah, Malaysia; coordinates provided for study sites.
- Data collected by R. E. J. Gray as part of LOMBOK/HMTF programs; all authors contributed to data interpretation.
- Recapture rates: moths 38% (404/1074 marked); dung beetles 4.9% (425/8689 marked).

## Experimental design and sampling regime
- Three focal sites with riparian reserves embedded in an oil palm matrix, connected to a large block of continuous virgin jungle reserve (VJR) rainforest.
- Trapping networks:
  - Moths: 16 fruit-baited butterfly traps plus a central release point (no trap at center); traps spaced ≥50 m apart.
  - Dung beetles: 17–18 baited pitfall traps plus 4 traps in the continuous forest.
- Sampling cadence:
  - Moths: 24-hour trap accumulation per round; daily marking of focal moths on wings; releases at the release point; daytime recaptures; continued for 8–14 days per site until ≥60 recaptures accumulated per site.
  - Dung beetles: traps checked and re-baited every two days for 14 days; marked individuals released after bait removal; traps closed temporarily to allow dispersal; recaptures recorded.

## Data collection methods
- Moths:
  - Traps: Bugdorm pop-up butterfly traps with 10 cm cone openings; baited with fermented banana; base held ≥1 m above ground.
  - Marking: focal moths marked on wings with a unique number; transported to release point for release into vegetation.
  - Data captured: species, trap, release date, recapture events; daily bait replacement; non-focal species removed from traps.
- Dung beetles:
  - Traps: inverted 1.5 L plastic bottles with a funnel; baited with human feces; suspended ~5 cm above trap; rain protection and shelter provided.
  - Marking: focal individuals marked with colored dots; some species sexed.
  - Data captured: species, sex, trap, release/recapture dates, habitat of capture and recapture, distance moved, and other movement metrics.
  - Duration: 14 days of marking with checks every two days; post-marking dispersal period allowed before bait replacement.

## Data structure and fields
- Dung_Beetle_Movement.csv (example fields):
  - Location, Site (RR10DB1, RR3, RR18, etc.); Latitude/Longitude; Taxa (species or complex); Before_Habitat and After_Habitat (Forest, Riparian, Oil Palm); Before_Trap and After_Trap; Distance; Towards_Forest; Number_of_Days; Frequency; Movement_Category (F = Forest, R = Riparian, OP = Oil palm); Movement_Type (within/between); Orientation; Sex; Burial_Mode; Temporal_Activity; Body_Area; Wing_Loading; etc.
  - Taxa examples: Catharsius sp.; O. mulleri; Sisyphus thoracicus; Paragymnopleurus sparsus; Proagoderus watanebei, etc.
- Moth_Movement.csv (example fields):
  - Location; Site; Taxa; Habitat (habitat at release/recapture); Trap; Distance (signed, positive toward oil palm or away); Absolute_Distance; Habitat_Change; Orientation; Number_of_Days; Frequency; Rate (recapture rate); etc.
  - Taxa examples: Erebus caprimulgus; Erebus gemmans; Hypoprya spp.; Ischyja spp.
- Notes:
  - The data include detailed habitat transitions (Forest, Riparian, Oil Palm) and directional movement metrics.
  - Some formatting inconsistencies appear in the sample (e.g., mixed separators in some lines), but the intended structure includes trap IDs, coordinates, site/habitat data, and movement metrics.

## Key findings and taxa details
- Moths: 1074 marked, 404 recaptured; movement data linked to trap location and habitat transitions; multiple taxa including Erebus spp. and Hypoprya spp.
- Dung beetles: 8689 marked, 425 recaptured; extensive species list within Scarabaeidae (e.g., Catharsius, Onthophagus, Sisyphus); rich metadata on sex, burial mode, activity, body metrics, and movement between habitats.
- Movement characteristics:
  - Movement categories capture transitions among Forest, Riparian, and Oil Palm habitats.
  - Distance, orientation, and days-to-recapture metrics allow assessment of movement corridors and habitat connectivity provided by riparian reserves.

## Data quality, limitations, and management notes
- Data files are comprehensive movement records with per-recapture entries; subject to data quality concerns due to formatting irregularities in the presented sample (need careful parsing to ensure field integrity).
- Depth of metadata supports cross-habitat movement analyses and ecological corridor assessments.
- Data are suitable for collaboration and synthesis within broader landscape ecology and biodiversity conservation programs.

## References
- ARELLANO, L., LEÓN-CORTÉS, J. L. & OVASKAINEN, O. 2008. Patterns of abundance and movement in relation to landscape structure: a study of a common scarab in Southern Mexico. Landscape Ecology.
- BATES, A. J., SADLER, J. P. & FOWLES, A. P. 2006. Oecologia.
- BETZHOLTZ, P.-E. 2002. Journal of Insect Conservation.
- EWERS, R. M. et al. 2011. Phil. Trans. R. Soc. B.
- LARSEN, T. H. & FORSYTH, A. 2005. Biotropica.
- GRAY, C. L. et al. 2014. Ecology and Evolution.
- LARSEN, T. H., LOPERA, A. & FORSYTH, A. 2006. The Coleopterists Bulletin.
- MARSH, C. J. et al. 2013. PLoS ONE.
- SLADE, E. M. et al. 2011. Biological Conservation.
- TRUXA, C. & FIEDLER, K. 2012. European Journal of Entomology.

## Relevance for Data Leaders
- Illustrates a well-documented, multi-taxa movement dataset across a fragmented landscape, highlighting the importance of comprehensive metadata for data discoverability and reuse.
- Demonstrates how to structure movement data by habitat transitions, trap locations, and temporal dimensions to support cross-site data integration and policy-relevant analyses.
- Emphasizes the need for clear data schemas, consistent field naming, and robust provenance to enable effective data stewardship, sharing, and collaboration across partner networks.