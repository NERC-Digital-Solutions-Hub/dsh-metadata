# Mark-Release-Recapture data showing moth and dung beetle movements in riparian reserves within the SAFE project landscape, Malaysian Borneo, 2016-17 [HMTF]. Gray, R.E.J, Slade, E.M., Chung, A.Y.C., Lewis, O.T.

## Overview
- Two mark-recapture datasets are provided: Moth_Movement.csv and Dung_Beetle_Movement.csv.
- Purpose: examine movement of moths and dung beetles within riparian forest reserves embedded in oil palm landscapes, connected to a large block of continuous lowland rainforest, to assess whether riparian reserves act as habitat or movement corridors.
- Timeframe: data collected between November 2016 and April 2017.
- Project context: part of the LOMBOK (Land use Options of Maintaining Biodiversity and eKosystem functions) within the Human Modified Tropical Forests Programme (HMTF); authors collectively interpreted the data.

## Experimental design and sampling regime
- Setting: Stability of Altered Forest Ecosystems (SAFE) project landscape in SE Sabah, Malaysia; three focal sites with riparian reserves embedded in oil palm and connected to large blocks of virgin jungle reserve (VJR).
- Moth experiment: conducted November 2016–January 2017; network of baited traps established; 60+ recaptures targeted per site across focal taxa.
- Dung beetle experiment: conducted January 2016–April 2017; traps baited with human feces; repeated marking and recapture over a 14-day period per site.
- Trap layout and data capture: separate trap arrays for moths and dung beetles, with multiple habitat types represented (oil palm, riparian reserve, continuous forest). Recapture data used to infer movement between habitats and distances traveled.

## Data collection methods
- Moths
  - Trap setup: six traps in oil palm, six in riparian reserve, four in continuous forest per site; 16 fruit-baited butterfly traps and a central release point without a trap.
  - Marking: focal moths wing-marked with a unique number; released at the release point after marking.
  - Sampling cycle: traps allowed to accumulate moths for 24 hours; recapture data collected over days 2–3 and repeated until sufficient recaptures were accumulated (minimum 60 across focal taxa per site).
  - Data captured: species, trap of capture, release date, recaptures, and associated metadata.
- Dung beetles
  - Trap setup: six traps in oil palm matrix, seven/eight in riparian reserve, four in VJR per site; traps baited with human feces.
  - Marking: individuals marked with unique codes using dot patterns; sexing recorded for some species.
  - Sampling cycle: traps checked and re-baited every two days for 14 days; both newly marked and recaptured individuals recorded and released at capture point.
  - Data captured: species, sex, trap of marking and recapture, habitat of marking/recapture, distance moved, directionality, days between release and recapture, and movement categorization.

## Data structure
- Dung_Beetle_Movement.csv
  - Location, Site, Taxa
  - Before_Habitat, After_Habitat (habitat where marked vs recaptured)
  - Before_Trap, After_Trap
  - Distance, Towards_Forest, Number_of_Days, Frequency
  - Movement_Category (F = Continuous forest, R = Riparian reserve forest, OP = Oil palm plantation)
  - Movement_Type (within, between)
  - Orientation, Sex, Burial_Mode, Temporal_Activity
  - Body_Area, Wing_Loading
  - Taxon metadata (taxon name, taxon type, parent name/type)
- Moth_Movement.csv
  - Location, Site, Taxa
  - Habitat/Trap identifiers and coordinates (Location with latitude/longitude references)
  - Before_Habitat, After_Habitat
  - Distance, Absolute_Distance
  - Habitat_Change, Orientation
  - Number_of_Days, Frequency, Rate
  - Movement_Category and other movement-related fields
  - Taxon-level details (as above for moths)
- Sites: RR3, RR10, RR18 (riparian reserves where trapping occurred)
- Taxa: multiple dung beetle species (e.g., Catharsius, Onthophagus, Paragymnopleurus, Sisyphus, Erebus spp. among moths) with genus/species-level classifications
- Additional notes: coordinates and trap identifiers included for movement between release and recapture locations; several fields describe movement direction, habitat changes, and ecological context

## Potential analyses and uses
- Quantify movement probabilities between habitats (oil palm, riparian reserve, continuous forest) for moths and dung beetles.
- Assess effectiveness of riparian reserves as movement corridors or habitats by comparing directionality (Towards forest vs towards oil palm) and distances traveled.
- Explore how habitat changes (habitat_change variable) relate to movement category and distance.
- Model factors influencing recapture rate and movement distance (Number_of_Days, Rate, Frequency).
- Compare movement patterns across taxa, sites, and habitat configurations.
- Integrate with landscape structure to infer landscape-scale connectivity and potential conservation value of riparian reserves in oil palm matrices.

## Data quality and notes
- Data are provided as two CSV files with explicit metadata and column definitions; careful handling required for some formatting variations in the excerpt (e.g., coordinate notation and mixed field representations).
- Site-level details and trap distributions are explicitly linked to three focal riparian reserves within a larger tropical forest landscape in Sabah, Malaysia.
- The datasets support reproducible movement analyses and can be used to inform management decisions regarding riparian reserve design and biodiversity corridors in agro-forest mosaics.

## References
- ARELLANO, L., LEÓN-CORTÉS, J. L. & OVASKAINEN, O. 2008. Patterns of abundance and movement in relation to landscape structure: a study of a common scarab Canthon cyanellus cyanellus. Landscape Ecology, 23, 69-78.
- BATES, A. J., SADLER, J. P. & FOWLES, A. P. 2006. Condition-dependent dispersal of a patchily distributed riparian ground beetle in response to disturbance. Oecologia, 150, 50-60.
- BETZHOLTZ, P.-E. 2002. Population structure and movement within an isolated population of Dysauxes ancilla L.: implications for conservation. Journal of Insect Conservation, 6, 57-66.
- EWERS, R. M. et al. 2011. A large-scale forest fragmentation experiment: the Stability of Altered Forest Ecosystems Project. PNAS/Biol Sci, 366, 3292-3302.
- LARSEN, T. H. & FORSYTH, A. 2005. Trap spacing and transect design for dung beetle biodiversity studies. Biotropica, 37, 322-325.
- GRAY, C. L. et al. 2014. Do riparian reserves support dung beetle biodiversity and ecosystem services in oil palm-dominated landscapes? Ecology and Evolution, 4, 1049-1060.
- LARSEN, T. H. et al. 2006. Extreme trophic and habitat specialization by Peruvian dung beetles. The Coleopterists Bulletin, 60, 315-324.
- MARSH, C. J. et al. 2013. Optimising bait for pitfall trapping of Amazonian dung beetles. PLoS ONE, 8, e73147.
- SLADE, E. M. et al. 2011. Biodiversity and ecosystem function of tropical forest dung beetles under contrasting logging regimes. Biological Conservation, 144, 166-174.
- TRUXA, C. & FIEDLER, K. 2012. Attraction to light—how far do moths return to weak artificial sources of light? European Journal of Entomology, 109, 77.