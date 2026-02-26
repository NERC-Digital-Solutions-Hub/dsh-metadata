# Time-activity budgets and energetics of common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake

## Aim and scope
- Provides key behavioural and physiological parameters for four seabird species during chick-rearing, an energetically demanding period influencing population demography.
- Aims to support monitoring and evaluation by linking energy requirements to prey intake and informing future decisions.

## What is in the dataset
- A single CSV file named Seabird_energetics_parameters.csv.
- Five columns: parameter (name) and one value column for each species (Guillemot, Razorbill, Kittiwake, Puffin).
- 24 parameters covering:
  - Time budgets: TB_foraging, TB_foraging_sd, TB_flying, TB_flying_sd, TB_resting_sea, TB_resting_sea_sd, TB_nest, TB_nest_sd.
  - Energetic costs: ER_foraging, ER_flying, ER_resting_sea, ER_nest, ER_warming_food, chick_ER, chick_ER_sd.
  - Life-history and body metrics: CR_duration, init_mass, init_mass_sd, mass_change, tissue_en_dens, energy_prey_conv, assim_effic, assim_effic_sd, BMR.
  - Additional context: energy costs for provisioning per chick, among others.
- Units are stippled per parameter (e.g., %time for budgets; kJ day-1 for costs; days for duration; g for masses).

## How parameters are defined and derived
- Time budgets (1-8): mean hours per 24-hour period for each activity, derived from species-specific activity data or integration of foraging and nesting time allocations.
- Core-behaviour energy costs (9-12, 13-15): fictive 24-hour costs synthesized from literature and species-specific body masses:
  - Foraging: weighted average of diving/resting costs (approx. 5.25 × BMR for pursuit-diving species).
  - Flight: species-specific values from prior studies.
  - Rest at sea: BMR-based estimate with a scaling factor (ratio ~1.39) to nest-rest costs; adjustments made for guillemot.
  - Nest: ~2 × BMR.
  - Warming food: scaled from other species based on predicted intake relative to body mass.
  - Provisioning per chick: species-specific provisioning energy.
- Chick-rearing duration (CR_duration) and adult body mass (init_mass, init_mass_sd): sourced from long-term or published datasets.
- Mass change (mass_change) and prey energy (energy_prey_conv, tissue_en_dens): calculated from long-term diet data and tissue energy values; prey energy densities estimated from fish length data and diet composition (sandeels, clupeids, other).
- Digestive assimilation efficiency (assim_effic, assim_effic_sd) and basal metabolic rate (BMR): drawn from published comparative studies.

## Data sources and provenance
- Isle of May long-term study (IMLOTS) primary data source for many body-mass and chick-rearing parameters.
- FAME project (2010-2014) for period-specific parameters linked to UK & Ireland seabirds.
- Supporting literature for species-specific metabolic rates, prey energy densities, and digestion efficiency.
- Diet data include yearly prey composition and energy densities (sandeel and clupeid scaling from observed lengths).

## Data governance, access, and quality
- Quality control: dataset stored in a single CSV with no shared access.
- Metadata depth is limited within the document; full provenance and calculation steps are described but not necessarily externally accessible.
- Acknowledges broader data-sharing barriers common in monitoring work (public release of underlying datasets may be restricted).

## Relevance for monitoring and decision-making
- Enables cross-species comparison of chick-rearing energetics and time allocations.
- Facilitates modeling of energy requirements against prey availability to inform management decisions (e.g., disturbance thresholds, marine planning, and impact assessments during chick-rearing).
- Provides a structured, comparable set of parameters to support population viability analyses and policy evaluations during energetics-related stress periods.

## Limitations and caveats
- Geographic and temporal scope is UK/British Isles-focused and centered on 2010-2014 (FAME) and IMLOTS periods; applicability to other regions/times may be limited.
- Some parameters rely on literature-derived values or adjustments (e.g., guillemot BMR, rest-at-sea costs); cross-species applicability should be tested.
- Data access restrictions may hinder transparency and reproducibility unless data governance is addressed.

## References and sources
- A comprehensive list of supporting studies and data sources is provided, including works on foraging energetics, dive costs, BMR relationships, prey energy densities, and long-term seabird monitoring programs (e.g., Thaxter et al., Wakefield et al., Harris & Wanless, Newell et al., Searle et al., Wanless et al., etc.).