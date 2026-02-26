# Mark-Release-Recapture data showing moth and dung beetle movements in riparian reserves within the SAFE project landscape, Malaysian Borneo, 2016-17 [HMTF]. Gray, R.E.J, Slade, E.M., Chung, A.Y.C., Lewis, O.T.

## Overview
- Two CSV data files: Moth_Movement.csv and Dung_Beetle_Movement.csv.
- Purpose: examine movement of invertebrates (moths and dung beetles) within riparian reserves embedded in an oil palm matrix, to assess whether riparian reserves provide habitat or movement corridors into/within large forest blocks.
- Timeframe: data collected between November 2016 and April 2017.
- Project context: part of the LOmbok project within the Human Modified Tropical Forests Programme (HMTF), within the SAFE landscape in southeastern Sabah, Malaysia.
- Data origin: collected and marked by R. E. J. Gray and collaborators; authors responsible for data interpretation.

## Experimental design and sampling regime
- Study area: three focal sites within the Stability of Altered Forest Ecosystems (SAFE) project landscape; each site includes a riparian forest reserve embedded in an oil palm matrix and connected to a large block of continuous virgin jungle reserve (VJR).
- Moths (MRR): network of 16 fruit-baited butterfly traps plus a central release point (no trap at release). Sampling from November 2016 to January 2017.
- Dung beetles (MRR): pitfall traps (six in oil palm, seven/eight in riparian reserve, four in forest) baited with human feces; marking and recapture occurred Jan 2016–April 2017.
- Trap spacing: at least 50 m apart.
- Marking and release:
  - Moths: wings marked with a unique number; released at the release point after capture.
  - Dung beetles: unique dot-based codes on elytra; sexed for some species.
- Sampling duration and goals:
  - Moths: continued for 8–14 days per site until a minimum of 60 recaptures across focal taxa were achieved.
  - Dung beetles: 14-day period of marking/recapture, with post-marking dispersal allowed before bait replacement.

## Data collection methods
- Moths:
  - Traps: Bugdorm butterfly traps placed across oil palm, riparian reserve, and continuous forest.
  - Procedure: traps set for 24 hours per round; focal moths marked and released; subsequent recaptures recorded; daily bait replacement; non-focal species removed from traps.
- Dung beetles:
  - Traps: baited pitfall traps (1.5 L bottles inverted to form a funnel) placed across habitat types.
  - Bait: 25 g human feces per trap.
  - Marking: durable markers used; individuals identified to species and coded; some sexing performed.
  - Procedure: traps checked and re-baited every two days for 14 days; both newly marked and recaptured beetles recorded and released at capture point.

## Data structure and fields
- Dung_Beetle_Movement.csv includes (illustrative fields):
  - Location, Site (Riparian reserves: RR3, RR10, RR18)
  - Taxa (species or genus)
  - Before_Habitat, After_Habitat (habitat at marking vs. recapture: Forest, Riparian, Oil Palm)
  - Before_Trap, After_Trap
  - Distance (m) between mark and recapture trap
  - Towards_Forest (Yes/No)
  - Number_of_Days
  - Frequency (recaptures)
  - Movement_Catgeory (F = Forest, R = Riparian, OP = Oil Palm)
  - Movement_Type (within/between)
  - Orientation
  - Sex, Burial_Mode, Temporal_Activity
  - Body_Area, Wing_Loading
- Moth_Movement.csv includes (illustrative fields):
  - Location (trap ID with coordinates)
  - Site (RR3, RR10, RR18, etc.)
  - Taxa (species or complex)
  - Habitat-related fields (e.g., trap location; habitat category per trap)
  - Distance and Absolute_Distance from release point
  - Orientation and Habitat_Change indicators
  - Number_of_Days
  - Frequency (recaptures)
  - Rate (recapture rate = frequency / days)
  - Links to release/recapture events via trap identifiers and coordinates
- Both datasets provide trap coordinates (latitude/longitude) and site-level context, enabling movement path analysis across habitat types.

## Key results and statistics (data context)
- Moths: 1,074 individuals marked; 404 recaptured across all sites and taxa; overall recapture rate ~38%.
- Dung beetles: 8,689 individuals marked; 425 recaptured across all sites and taxa; overall recapture rate ~4.9%.
- Data enable assessment of movement patterns across habitat boundaries (Forest ↔ Riparian ↔ Oil Palm) and evaluation of riparian reserve effectiveness as habitat or corridor.

## Potential uses for Data Support
- Analyze movement ecology and habitat connectivity for invertebrates in fragmented tropical landscapes.
- Assess the effectiveness of riparian reserves as movement corridors or refuges within oil palm-dominated matrices.
- Combine with other LOmbok/HMTF datasets to build broader insights on biodiversity and ecosystem function in transformed tropical forests.
- Develop self-serve data products (dashboards, pivot analyses) to explore how movement varies by habitat, site, taxon, and time.
- Support data quality assurance, harmonization, and integration with related spatial or ecological datasets.

## Data provenance and references
- Core references informing methods and interpretation include:
  - Arellano et al. 2008; patterns of abundance and movement in a scarab species.
  - Bates et al. 2006; dispersal in riparian beetles.
  - Betzholtz 2002; moth movement and population structure.
  - Ewers et al. 2011; SAFE project design and large-scale fragmentation experiment.
  - Larsen & Forsyth 2005; dung beetle trap design and spacing.
  - Gray et al. 2014; dung beetles, riparian reserves, and oil palm landscapes.
  - Larsen et al. 2006; extreme trophic/habitat specialization in dung beetles.
  - Marsh et al. 2013; optimizing bait for pitfall trapping.
  - Slade et al. 2011; biodiversity under contrasting logging regimes.
  - Truxà & Fiedler 2012; moth responses to light traps.