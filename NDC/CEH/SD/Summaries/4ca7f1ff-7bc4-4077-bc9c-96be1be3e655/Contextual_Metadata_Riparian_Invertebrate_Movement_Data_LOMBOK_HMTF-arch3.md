Mark-Release-Recapture data showing moth and dung beetle movements in riparian reserves within the SAFE project landscape, Malaysian Borneo, 2016-17 [HMTF]. Gray, R.E.J, Slade, E.M., Chung, A.Y.C., Lewis, O.T.

# Overview

- Datasets: Moth_Movement.csv and Dung_Beetle_Movement.csv
- Purpose: examine movement of invertebrates (moths and dung beetles) within riparian reserves embedded in oil palm matrices to evaluate whether riparian reserves function as habitat or movement corridors.
- Timeframe: data collected Nov 2016–Apr 2017 (moths Nov 2016–Jan 2017; dung beetles Jan 2016–Apr 2017).
- Context: part of the LOMBOK project within the Human Modified Tropical Forests Programme (HMTF); conducted in the SAFE project landscape, SE Sabah, Malaysia.
- Study design: three focal sites with riparian reserves connected to a large block of continuous virgin jungle reserve (VJR). Networks of baited traps used for mark-release-recapture (MRR).
- Key metrics: overall recapture rates – moths 38% (404/1074); dung beetles 4.9% (425/8689).

# Experimental Design and Sampling Regime

- Study sites: three locations where riparian reserves adjoin oil palm and connect to continuous rainforest.
- Moths:
  - Traps: six in oil palm, six in riparian reserve, four in continuous forest.
  - Trapping: BugDorm butterfly traps baited with fermented banana; central release point (no trap).
  - Protocol: mark on wings with unique numbers; release at the release point; recapture and marking repeated for 8–14 days until a minimum of 60 recaptures across focal taxa per site.
- Dung beetles:
  - Traps: six in oil palm, seven/eight in riparian reserve, four in continuous forest.
  - Trapping: baited traps using human feces; marked with dot-based codes; some individuals sexed.
  - Protocol: traps checked and re-baited every second day for 14 days; both new marks and recaptures recorded and beetles released at capture point.
- Data captured: species, trap/locations, habitat types, release/recapture dates, and movement between habitats.

# Data Collection Methods

- Moths:
  - Traps positioned in three habitat types; 24-hour accumulation per sampling round.
  - Marking: unique wing numbers; transport to release point; release into vegetation.
  - Follow-up: daily recapture monitoring; additional marking as needed; data recorded per individual.
- Dung beetles:
  - Traps baited with 25 g human feces; traps angled to exclude rain and provide shelter.
  - Marking: color markers; some individuals sexed; marks designed to last at least ~7 days.
  - Protocol: recapture and release at capture point; traps checked every two days.

# Data Structure and Key Variables

- Dung beetle dataset (Dung_Beetle_Movement.csv) includes:
  - Location, Site, Taxa (species or complex), Before_Habitat, After_Habitat (habitat categories), Before_Trap, After_Trap, Distance (m), Towards_Forest (Yes/No), Number_of_Days, Frequency (recapture events), Movement_Category (F = forest, R = riparian, OP = oil palm), Movement_Type (within/between), Orientation, Sex, Burial_Mode, Temporal_Activity, Body_Area, Wing_Loading, plus detailed taxonomic data (e.g., Catharsius spp., O. mulleri, Sisyphus thoracicus, etc.).
- Moth dataset (Moth_Movement.csv) includes:
  - Location, Site, Taxa, Habitat (Forest/Riparian/Oil Palm), Trap, Distance (m) with sign to indicate direction, Absolute_Distance, Habitat_Change (Yes/No), Orientation, Number_of_Days, Frequency, Rate (recapture rate = Frequency/Number_of_Days).
- Taxonomic and trait details are provided for multiple species across Scarabaeidae and Noctuidae families.

# Data Quality, Metadata and Governance Considerations

- Data richness: rich, multi-habitat movement data across three sites with explicit habitat transitions and directional movement metrics.
- Metadata clarity: explicit column definitions and example values; includes trap IDs, site codes (RR3, RR10, RR18), and detailed movement descriptors.
- Potential barriers for monitoring use:
  - Need for standardized metadata conventions when integrating with other datasets (e.g., harmonizing habitat codes, trap identifiers, and temporal stamps).
  - Data sharing and openness considerations in monitoring frameworks; raw datasets are provided, but governance and licensing details are not specified.
  - Spatial accuracy: trap locations and coordinates included; critical for landscape-scale connectivity analyses.
- Data quality signals: relatively low recapture rate for dung beetles (4.9%) compared with moths (38%), which influences statistical power for movement inferences.

# Relevance to Monitoring Frameworks and Policy

- Indicators for policy evaluation:
  - Habitat connectivity effectiveness of riparian reserves within agro-ecosystems.
  - Movement probabilities of key invertebrate taxa across habitat boundaries (oil palm to riparian to continuous forest).
  - Directional movement patterns and barriers to dispersal in fragmented landscapes.
- Data products suitable for monitoring:
  - Movement matrices by habitat transition (Forest ↔ Riparian ↔ Oil Palm).
  - Distance-based movement metrics and orientation trends.
  - Species-specific dispersal tendencies and habitat preferences to inform reserve design and landscape planning.
- Data use considerations:
  - Métier for informing decisions on riparian reserve management, corridor enhancement, and agro-ecosystem biodiversity objectives.
  - Potential integration with other biodiversity monitoring datasets to form a broader policy-relevant evidence base.

# References

- ARELLANO, L., LEÓN-CORTÉS, J. L. & OVASKAINEN, O. 2008. Patterns of abundance and movement in relation to landscape structure: a study of a common scarab (Canthon cyanellus cyanellus) in Southern Mexico. Landscape Ecology, 23, 69-78.
- BATES, A. J., SADLER, J. P. & FOWLES, A. P. 2006. Condition-dependent dispersal of a patchily distributed riparian ground beetle in response to disturbance. Oecologia, 150, 50-60.
- BETZHOLTZ, P.-E. 2002. Population structure and movement within an isolated endangered population of the moth Dysauxes ancilla L. Journal of Insect Conservation, 6, 57-66.
- EWERS, R. M. et al. 2011. A large-scale forest fragmentation experiment: the Stability of Altered Forest Ecosystems Project. Philosophical Transactions of the Royal Society B, 366, 3292-3302.
- LARSEN, T. H. & FORSYTH, A. 2005. Trap spacing and transect design for dung beetle biodiversity studies. Biotropica, 37, 322-325.
- GRAY, C. L. et al. 2014. Do riparian reserves support dung beetle biodiversity and ecosystem services in oil palm-dominated tropical landscapes? Ecology and Evolution, 4, 1049-1060.
- LARSEN, T. H. et al. 2006. Extreme trophic and habitat specialization by Peruvian dung beetles. The Coleopterists Bulletin, 60, 315-324.
- MARSH, C. J. et al. 2013. Optimising bait for pitfall trapping of Amazonian dung beetles. PLoS ONE, 8, e73147.
- SLADE, E. M. et al. 2011. Biodiversity and ecosystem function of tropical forest dung beetles under contrasting logging regimes. Biological Conservation, 144, 166-174.
- TRUXA, C. & FIEDLER, K. 2012. Attraction to light—From how far do moths return to weak artificial sources of light? European Journal of Entomology, 109, 77.