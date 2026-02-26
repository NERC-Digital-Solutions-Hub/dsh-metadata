# Mark-Release-Recapture data showing moth and dung beetle movements in riparian reserves within the SAFE project landscape, Malaysian Borneo, 2016-17 [HMTF]. Gray, R.E.J, Slade, E.M., Chung, A.Y.C., Lewis, O.T.

## Overview
- Mark-release-recapture (MRR) datasets for moths and dung beetles in riparian reserves embedded within an oil palm matrix, connected to a large block of continuous lowland rainforest.
- Data collected Nov 2016–Apr 2017 to assess whether riparian reserves provide habitat or movement corridors through oil palm landscapes.
- Part of the LO[M]BOK project within the Human Modified Tropical Forests Programme (HMTF); authors responsible for data interpretation.

## Experimental design and sampling regime
- Three focal sites with riparian reserves embedded in oil palm and connected to a large virgin jungle reserve (VJR) of lowland dipterocarp rainforest.
- Moths: network of traps with a central release point; sampling Nov 2016–Jan 2017; 16 fruit-baited traps; spacing at least 50 m; minimum 60 recaptures accumulated per site across 8–14 days.
- Dung beetles: traps distributed across oil palm, riparian reserve, and continuous forest; sampling Jan 2016–Apr 2017; traps checked every second day for 14 days; marking conducted after capture.

## Data collection methods
- MOTH experiment
  - Six traps in oil palm, six in riparian reserve, four in continuous forest.
  - Traps baited with fermented banana; moths marked on wings with unique numbers; released at a central point; data collected on species, trap, release date, and recaptures.
  - Daily bait replacement; marking of focal moths only; continued until a target recapture effort completed.
- DUNG BEETLE experiment
  - Traps: inverted 1.5 L bottles baited with human feces; traps checked every two days for 14 days.
  - Marking with color-coded dot codes; individuals identified to species and sometimes sexed; released at capture point after marking.
  - After marking, traps closed to allow dispersion before bait replacement.

## Data files and structure
- Two CSV files provided:
  - Dung_Beetle_Movement.csv
  - Moth_Movement.csv
- Dung beetle dataset (Dung_Beetle_Movement.csv) includes:
  - Location, Site (riparian reserve codes), Taxa, Before_Habitat, After_Habitat, Before_Trap, After_Trap
  - Distance, Towards_Forest, Number_of_Days, Frequency, Movement_Category, Movement_Type
  - Additional attributes: Orientation, Sex, Burial_Mode, Temporal_Activity, Body_Area, Wing_Loading
  - Detailed records of each recapture (one line per recapture)
- Moth dataset (Moth_Movement.csv) includes:
  - Location (trap ID), Site, Taxa
  - Spatial coordinates for trap locations
  - Recapture information (frequency per line), and movement-related fields such as Habitat, Distance, Orientation, Number_of_Days, Rate (recaptures per day)
  - Trap identifiers (e.g., F180a, F100a, etc.) and site codes (RR3, RR10, RR18)
  - Each line represents a recapture event with associated trap and timing data
- Both datasets capture movement across habitat types (Forest, Riparian, Oil Palm) and track whether movement was within or between habitats, with directionality indicators (e.g., Distance sign for movement toward forest or oil palm)

## Key variables and interpretation
- Habitat transitions: Before_Habitat/After_Habitat and Habitat_Change indicate whether movement crossed habitat boundaries (Forest, Riparian, Oil Palm).
- Movement direction and distance: Distance, Absolute_Distance, Orientation, and Towards_Forest provide directional movement context (toward continuous forest vs. oil palm).
- Temporal dynamics: Number_of_Days between release and recapture; Frequency and Rate capture recapture intensity and dispersion over time.
- Species and morphology: Taxa, Sex (where available), and physical traits (Body_Area, Wing_Loading) for dung beetles; taxa notes for moths.
- Site-level context: Site codes RR3, RR10, RR18 representing riparian reserves; trap locations and coordinates are provided for spatial analyses.

## Outputs and use for environmental monitoring
- Enables assessment of riparian reserve effectiveness as habitat and movement corridors within oil palm-dominated landscapes.
- Facilitates standardized outputs such as maps and charts illustrating movement paths, habitat transitions, and connectivity.
- Data quality and standardization align with common monitoring practices: verification, cleaning, and transformation of established-source data; storage and portal submission recommended.

## Provenance, references, and notes
- Detailed methodology and supporting literature cited, including:
  - Arellano et al. 2008; Bates et al. 2006; Betzholz 2002; Ewers et al. 2011; Larsen & Forsyth 2005; Gray et al. 2014; Larsen et al. 2006; Marsh et al. 2013; Slade et al. 2011; Truxa & Fiedler 2012.
- Recaptures and rates: Moths ~38% overall recapture frequency (404/1074); Dung beetles ~4.9% overall recapture frequency (425/8689).
- Data produced under LO[M]BOK project and HMTF program, with authors responsible for interpretation of results.