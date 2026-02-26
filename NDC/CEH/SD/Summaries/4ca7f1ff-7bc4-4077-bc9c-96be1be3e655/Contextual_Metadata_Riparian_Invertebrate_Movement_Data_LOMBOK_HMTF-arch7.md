# Mark-Release-Recapture data showing moth and dung beetle movements in riparian reserves within the SAFE project landscape, Malaysian Borneo, 2016-17 [HMTF]. Gray, R.E.J, Slade, E.M., Chung, A.Y.C., Lewis, O.T.

## Overview
- Two CSV datasets are provided: Moth_Movement.csv and Dung_Beetle_Movement.csv, collected 2016–2017 in the SAFE project landscape, southeastern Sabah, Malaysia.
- Objective: examine movement of moths and dung beetles within riparian reserves embedded in oil palm landscapes to assess habitat value and movement corridors.
- Study context: three focal sites with riparian reserves connected to a large virgin jungle reserve (VJR) of lowland dipterocarp rainforest.
- Key results summarized:
  - Moths: 1074 marked; 404 recaptured; overall recapture rate of 38%.
  - Dung beetles: 8689 marked; 425 recaptured; overall recapture rate of 4.9%.

## Experimental design and sampling regime
- Three focal sites with riparian reserves embedded in oil palm matrix, linked to continuous VJR rainforest.
- Moth experiments: traps established across habitat types; 16 fruit-baited butterfly traps with a central release point (no trap there). Mark-release-recapture conducted November 2016–January 2017; daily bait replacement and marking of focal moths; sampling continued for 8–14 days per site until ≥60 recaptures across focal taxa.
- Dung beetle experiments: traps distributed as six in oil palm, seven–eight in riparian reserves, four in forest; marked with dot codes after capturing; trapping and re-baiting every two days for 14 days; beetles released after marking to disperse before bait replacement; records include both newly marked and recaptured individuals.
- Traps spaced at least 50 m apart; traps designed to sample across habitat types: continuous forest, riparian reserve forest, and oil palm plantations.

## Data collection methods
- MOTH EXPERIMENT
  - Trap setup: six traps in oil palm, six in riparian reserve, four in continuous forest.
  - Traps: Bugdorm butterfly bait traps baited with fermented banana, suspended ~1 m above ground.
  - Marking: focal moths wing-marked with unique numbers; transport to release point for manual release.
  - Data: species, trap of capture, release date, recapture data; daily bait replacement; ongoing recaptures over 8–14 days per site to meet recapture targets.
- DUNG BEETLE EXPERIMENT
  - Trap setup: six traps in oil palm, seven/eight in riparian reserve, four in forest.
  - Traps: inverted plastic bottle traps with bait; human feces as bait.
  - Marking: focal species identified to species; unique dot-code marks on elytra; some sexes recorded.
  - Data: trap identity, capture/recapture events, marking status (new vs recaptured), movement between habitats, distance metrics, orientation, days between release and recapture, and other movement attributes.

## Data structure and fields
- Two CSV files are provided: Dung_Beetle_Movement.csv and Moth_Movement.csv.
- Common structural elements:
  - Location: trap where the dung beetle or moth was recaptured.
  - Site: Riparian reserve site (RR3, RR10, RR18).
  - Taxa: species or species complex (examples include Catharsius, Onthophagus spp., Paragymnopleurus sparsus, Erebus caprimulgus, Hypoprya spp., Ischyja spp., etc.).
  - Habitat-related fields (Dung Beetles): Before_Habitat and After_Habitat (Forest, Riparian, Oil Palm).
  - Trap/Trap-related fields: Before_Trap and After_Trap (trap identifiers); Trap (specific trap code for moths and beetles).
  - Movement and distance fields: Distance (meters between capture and recapture trap), Absolute_Distance (exact meters from release), Habitat_Change (Yes/No), Orientation (movement direction preference), Movement_Category (F = Continuous forest, R = Riparian reserve forest, OP = Oil palm), Movement_Type (within/between habitats).
  - Temporal and frequency fields: Number_of_Days (days between release and recapture), Frequency (recapture frequency; one line per recapture), Rate (recapture rate = Frequency / Number_of_Days).
  - For Moths (some fields differ): Before_Habitat / After_Habitat are not always present; instead, fields include Distance, Absolute_Distance, Habitat_Change, Orientation, Number_of_Days, Frequency, Rate.
- Beetle-specific fields (Dung_Beetle_Movement.csv):
  - Orientation: directional movement preference (e.g., toward forest or toward riparian/oil palm).
  - Sex: female/male (and occasionally other coded entries).
  - Burial_Mode: roller or tunneller.
  - Temporal_Activity: diurnal/nocturnal.
  - Body_Area and Wing_Loading: biometric metrics provided (mm^2) derived from body length and thorax width.
  - Additional taxon-specific metadata (Taxon name, Taxon type, Parent name/type).
- Moth-specific fields (Moth_Movement.csv):
  - Absolute_Distance and Distance provide both signed and exact spatial movement data (Distance may have directional sign).
  - Rate and Frequency capture recapture dynamics analogous to dung beetles.
  - Trap codes reflect sampling across habitat types and release points.

## Site and taxa context
- Sites: RR3, RR10, RR18 (riparian reserves within oil palm landscapes).
- Taxa included: multiple moth species (e.g., Erebus caprimulgus, Erebus gemmans, Hypoprya spp., Ischyja spp.) and dung beetle species across Scarabaeidae (e.g., Catharsius, Onthophagus, Paragymnopleurus, Proagoderus, Sisyphus).
- Habitat interpretation: data capture movements between continuous forest, riparian reserves, and oil palm plantations, enabling assessments of movement corridors and habitat connectivity.

## Reference context
- Cited literature provides methodological and ecological context for movement, trap design, and habitat studies, including work on riparian reserves, dung beetle ecology, and mark-release-recapture methodologies (Arellano et al. 2008; Bates et al. 2006; Betzholtz 2002; Ewers et al. 2011; Larsen & Forsyth 2005; Gray et al. 2014; Larsen et al. 2006; Marsh et al. 2013; Slade et al. 2011; Truxa & Fiedler 2012).

## Notes for GIS use
- Data are spatially explicit with trap locations, recapture coordinates, and site-level habitat classifications suitable for map-based analyses of movement patterns.
- Movement metrics (Distance, Orientation, Movement_Category, Habitat_Change) enable corridor and connectivity modeling across land-use gradients (forest, riparian reserves, oil palm).
- Biometric and sex data (Dung Beetles) offer potential analyses of dispersal behavior by species, sex, and life-history traits.
- The datasets support cross-habitat movement analysis and can be integrated with other SAFE project landscape layers for broader ecological interpretation.