# Avifauna occurrence data from a longitudinal experiment in human-modified Amazonian forests affected by the 2015-16 El Niño drought and associated fires

## Data scope and purpose
- Longitudinal bird occurrence data across 36 forest plots in the Brazilian Amazon, collected before (2010–11) and after (2016) the 2015–16 El Niño drought and associated fires.
- Part of the NERC Human-Modified Tropical Forest (HTMF) programme; aims to quantify how human disturbance and climate-induced stressors influence tropical forest biodiversity.

## Study region
- Santarém/Belterra/Mojuí dos Campos municipalities, Pará state, Northeastern Brazilian Amazon.
- Undisturbed primary forests typically have canopy heights of 30–40 m (emergents up to ~50 m).

## Experimental design and sampling regime
- 36 plots across a disturbance gradient: undisturbed (N=10), logged (N=10), logged-and-burned (N=10), and secondary forests (N=6).
- Plots selected based on prior disturbance assessed via canopy disturbance in time-series satellite images (1988–2010) and previous field assessments of fire scars and logging/charcoal.
- Two surveys per plot, one in 2010–11 (pre-El Niño) and one in 2016 (post-El Niño), with identical locations and methods for both periods.

## Data collection methods
- Faunal sampling conducted along 300-m forest plots at three sampling points (0, 150, 300 m).
- Bird records from two repetitions of three 15-minute, 75-m fixed-width point counts per plot per survey.
- Surveys conducted from 15 minutes before dawn to 09:30, under suitable weather; audio and visual observations recorded.
- Systematic rotation of repetitions across catchments and plots to minimize temporal biases.
- Verbal permits from landowners; surveys in protected areas conducted under Brazilian legislation and permits (SISBIO).

## Data content and structure
- Data file: ECOFOR_AFIRE_RAS_birds.csv.
- Field details (Table 1):
  - CAMP_1: 2010–11 (pre-El Niño)
  - CAMP_2: 2016 (post-El Niño)
  - Plot code, Point (within-plot sampling location), Date, Time
  - Observer (names listed)
  - Family (taxonomic family; per Piacentini et al. 2015)
  - Binomial (genus and species)
  - Auditory (whether recorded by sound)
  - Visual (whether observed visually)
- Geographic coordinates for plots (Table 2) include:
  - Municipality, UTM_X, UTM_Y
  - Plot identifiers (e.g., 112_12, 112_8, etc.)
  - 36 plots spread across Santarém, Belterra, and Mojuí-dos-Campos
  - UTM zone 21M coordinates

## Data access, licensing, and provenance
- Data access and reuse details available via the DOI: https://doi.org/10.5285/4b05caee-a3c8-46a7-b675-e5a94554bd9f
- Supporting information and metadata are provided through the NERC Environmental Information Data Centre.
- Project funding and contributors:
  - HTMF program with support from NERC, Darwin Initiative, EMBRAPA, CNPq, CAPES/CNPq/PELD-RAS, Instituto Nacional de Ciência e Tecnologia Biodiversidade e Uso da Terra na Amazônia, and Swedish Formas.
  - Authorship roles span study design, plot selection, data collection, and data interpretation.

## Potential analytical uses
- Assess changes in avifauna occurrence attributable to:
  - Fire disturbance and ENSO-related stress
  - Varying historical human disturbance (undisturbed, logged, burned, secondary)
- Model species-habitat associations and detectability across time and disturbance classes.
- Integrate with plot-level disturbance data and environmental covariates to test predictions about biodiversity responses to drought, fire, and habitat modification.

## Considerations and limitations
- Only two time points (pre- and post-disturbance), which may limit inference about longer-term trends.
- Detectability biases and observer effects mitigated by standardized protocols and multiple observers; explicit observers listed per record.
- Spatial scale limited to 36 plots within a defined region; extrapolation should consider local context and habitat heterogeneity.