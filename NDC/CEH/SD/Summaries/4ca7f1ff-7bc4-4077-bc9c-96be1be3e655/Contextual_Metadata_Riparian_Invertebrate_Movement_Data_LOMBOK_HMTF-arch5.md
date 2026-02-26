# Mark-Release-Recapture data showing moth and dung beetle movements in riparian reserves within the SAFE project landscape, Malaysian Borneo, 2016-17 [HMTF]. Gray, R.E.J, Slade, E.M., Chung, A.Y.C., Lewis, O.T.

## Overview and scope
- Datasets record mark-release-recapture (MRR) movements of moths and dung beetles in riparian reserves embedded in oil palm matrices, connected to a large block of continuous lowland dipterocarp rainforest (VJR).
- Study area: SAFE project landscape, southeastern Sabah, Malaysia (three focal sites: RR3, RR10, RR18).
- Data collection period: 2016–2017 (moths: November 2016–January 2017; dung beetles: January 2016–April 2017).
- Purpose: to assess whether riparian reserves provide habitat or movement corridors for invertebrates within oil palm landscapes.
- Data products: two CSV files:
  - Moth_Movement.csv
  - Dung_Beetle_Movement.csv
- Authors and context: part of LOmbok (LOMBOK) within the Human Modified Tropical Forests Programme (HMTF); data interpretation by all authors.

## Experimental design and sampling
- Sites and landscape context:
  - Three focal sites with riparian reserves in oil palm, connected to a large continuous rainforest block (VJR).
- Moth experiment:
  - 16 fruit-baited butterfly traps arranged across habitat types; a central release point without a trap.
  - Marking: moths were marked on the wing with unique numbers; release and recapture events recorded.
  - Sampling cadence: daily trap checks with 24-hour accumulation periods; continued for 8–14 days until at least 60 focal recaptures per site.
- Dung beetle experiment:
  - Traps distributed across oil palm, riparian reserve, and forest habitats using 1.5 L inverted plastic bottle traps baited with human faeces.
  - Marking: each focal beetle marked with a unique dot code on the elytra; some individuals sexed.
  - Cadence: traps checked and re-baited every two days for 14 days; both newly marked and recaptured individuals recorded and released at capture point.
- Data capture aims:
  - Record movement between habitats (Forest, Riparian, Oil Palm).
  - Capture movement distance, direction, and timing to evaluate habitat transitions and potential corridor function.

## Data structure and key fields
- Dung_Beetle_Movement.csv
  - Location, Site (RR3; RR10; RR18)
  - Taxa (species or complex; e.g., Catharsius, Onthophagus, Paragymnopleurus, Sisyphus)
  - Before_Habitat / After_Habitat (Forest, Riparian, Oil Palm)
  - Before_Trap / After Trap (trap IDs)
  - Distance (meters between marking and recapture traps)
  - Towards_Forest / Orientation (movement direction relative to forest/landscape)
  - Number_of_Days, Frequency (recaptures; per line)
  - Rate (recapture rate)
  - Movement_Category (F = Continuous forest, R = Riparian reserve forest, OP = Oil palm plantation)
  - Movement_Type (within / between habitats)
  - Habitat_Change, Absolute_Distance, Sex, Burial_Mode, Temporal_Activity, Body_Area, Wing_Loading
  - Additional taxon metadata (taxon name/type, parent taxonomy)
- Moth_Movement.csv
  - Location, Site (RR3, RR10, RR18)
  - Taxa (species or complex)
  - Trap (trap ID being used for capture/recapture)
  - Distance (signed distance from release: negative toward forest, positive away)
  - Absolute_Distance
  - Habitat_Change (Yes/No)
  - Orientation (F = toward forest; R = toward/along riparian reserve; OP = toward oil palm)
  - Number_of_Days, Frequency
  - Rate (recapture rate)
  - Additional fields mirror movement context (Site, Taxa, Location, etc.)

- Notable design choices:
  - Habitat categories standardized as Forest, Riparian, and Oil Palm.
  - Distances provided with directional sign and an absolute value for flexibility in analyses.
  - Movement_Category and Movement_Type capture whether habitat transitions occurred and whether moves were within or between habitats.

## Data quality, provenance, and limitations
- Data provenance:
  - Collected through field protocols described in the methods; explicit marking, release, and recapture steps documented.
  - Coordinates provided for trap locations; site-level identifiers (RR3, RR10, RR18) used for aggregation.
- Quality and consistency considerations:
  - Recapture rates differ markedly between taxa (moths ~38% overall; dung beetles ~4.9% overall), which influences statistical power for movement inferences.
  - Some fields include multiple taxon-specific details (e.g., sex, burial mode, temporal activity for dung beetles; wing markings for moths) that require careful harmonization during cross-dataset analyses.
  - The dataset uses explicit habitat transitions and directional distances, enabling analyses of movement corridors, but missing values or inconsistencies are not detailed in the description.
- Limitations to note for stewardship and reuse:
  - Movement inferences may be constrained by trap layout, sampling duration per site, and varying recapture efficiencies across habitats.
  - Data are site-specific to three Riparian reserves within an oil palm matrix in Sabah, Malaysia; generalization to other landscapes should be done cautiously.
  - Some column names (e.g., Movement_Catgeory) show typographical inconsistencies that analysts should clean during metadata harmonization.

## Usage and potential analyses
- Movement ecology and landscape connectivity:
  - Analyze cross-habitat movement frequencies and distances to evaluate whether riparian reserves function as corridors.
  - Compare movement directions and orientations relative to forest, riparian, and oil palm habitats.
- Habitat-by-habitat transition patterns:
  - Examine proportions of movements that involve habitat change (Yes/No) and categorize transitions (Forest→Riparian, Riparian→Oil Palm, etc.).
- Taxon-specific insights:
  - Contrast moth and dung beetle movement patterns to understand how mobility and behavior influence landscape use.
- Temporal dynamics:
  - Use Number_of_Days and Rate to assess how movement probability changes over time since release.
- Data integration:
  - Combine with external habitat maps or land-use data to quantify landscape resistance and corridor effectiveness.

## References
- ARELLANO, L., LEÓN-CORTÉS, J. L. & OVASKAINEN, O. 2008. Patterns of abundance and movement in relation to landscape structure: a study of a common scarab (Canthon cyanellus cyanellus) in Southern Mexico. Landscape Ecology, 23, 69-78.
- BATES, A. J., SADLER, J. P. & FOWLES, A. P. 2006. Condition-dependent dispersal of a patchily distributed riparian ground beetle in response to disturbance. Oecologia, 150, 50-60.
- BETZHOLTZ, P.-E. 2002. Population structure and movement within an isolated population of Dysauxes ancilla L.: implications for conservation. Journal of Insect Conservation, 6, 57-66.
- EWERS, R. M. et al. 2011. A large-scale forest fragmentation experiment: the Stability of Altered Forest Ecosystems Project. Phil. Trans. R. Soc. B, 366, 3292-3302.
- LARSEN, T. H. & FORSYTH, A. 2005. Trap spacing and transect design for dung beetle biodiversity studies. Biotropica, 37, 322-325.
- GRAY, C. L. et al. 2014. Do riparian reserves support dung beetle biodiversity and ecosystem services in oil palm-dominated tropical landscapes? Ecology and Evolution, 4, 1049-1060.
- LARSEN, T. H., LOPERA, A. & FORSYTH, A. 2006. Extreme trophic and habitat specialization by Peruvian dung beetles. The Coleopterists Bulletin, 60, 315-324.
- MARSH, C. J. et al. 2013. Optimising bait for pitfall trapping of Amazonian dung beetles. PLoS ONE, 8, e73147.
- SLADE, E. M. et al. 2011. Biodiversity and ecosystem function of tropical forest dung beetles under contrasting logging regimes. Biological Conservation, 144, 166-174.
- TRUXA, C. & FIEDLER, K. 2012. Attraction to light—how far do moths return to weak artificial sources of light? European Journal of Entomology, 109, 77.