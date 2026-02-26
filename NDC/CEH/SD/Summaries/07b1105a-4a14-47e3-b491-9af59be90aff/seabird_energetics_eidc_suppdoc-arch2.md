# Time-activity budgets and energetics of common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake

## Overview
- Presents a dataset of key behavioural and physiological traits for four seabird species during chick-rearing, a period with high energetic demands.
- Links seabird energy requirements to prey intake rates, with UK and British Isles breeding colonies as the primary context.
- Uses data from long-term studies (e.g., IMLOTS) and large-scale tracking (FAME; 2010–2014) to inform metabolic and energetic calculations.

## Data structure
- Single CSV file: seabird_energetics_parameters.csv
- Five columns total:
  - First column: parameter (name)
  - Four species columns: Guillemot, Razorbill, Kittiwake, Puffin
- Table 1 enumerates parameter names, details, and units (μ, sd, or %time; listed where relevant)

## Parameters and units (key entries)
- Time budgets (percent time per 24 h):
  - TB_foraging, TB_foraging_sd
  - TB_flying, TB_flying_sd
  - TB_resting_sea, TB_resting_sea_sd
  - TB_nest, TB_nest_sd
- Energetic costs (kJ day⁻¹):
  - ER_foraging, ER_flying, ER_resting_sea, ER_nest
- Additional energetic components:
  - ER_warming_food, chick_ER (provisioning per chick), chick_ER_sd
- Life-history and physiology:
  - CR_duration (chick-rearing duration, days)
  - init_mass, init_mass_sd (adult body mass, g)
  - mass_change (proportional mass change during chick-rearing)
  - tissue_en_dens (seabird tissue energy density, kJ g⁻¹)
  - energy_prey_conv (prey energy density, kJ g⁻¹)
  - assim_effic, assim_effic_sd (digestive assimilation efficiency)
  - BMR (basal metabolic rate, kJ day⁻¹)

## Methods and calculations (how values were derived)
- Time budgets:
  - Guillemots and Razorbills: derived from activity logger data; kittiwake combining foraging trip timing with nest/foraging time split (approx. 51% nest, 49% foraging); puffin budgets from activity data (flight, foraging, resting at sea).
- Energetic costs for core behaviours (hypothetical 24 h cycle):
  - Foraging: weighted average of diving and rest-at-sea costs; based on dive-to-pause ratios and 5.25 × BMR (where applicable)
  - Flight: species-specific costs from published studies
  - Rest at sea: BMR-derived, using a guillemot ratio (1.39) and adjustments to published values
  - Nest: 2 × BMR
  - Warming food: scaled from other species (e.g., great cormorant) by predicted daily intake versus body mass
- Provisioning per chick: species-specific values from Thaxter et al. (2013), Harris & Wanless (1986), Harris (1979), etc.
- Chick-rearing duration and adult body masses:
  - Sourced from Isle of May long-term data and other literature
- Mass change during chick-rearing:
  - Guillemots: 0.41% daily decrease over 21 days
  - Kittiwake: based on IMLOTS data
  - Puffin: estimated from May–July mass differences
  - Razorbill: not available
- Diet and prey energy densities:
  - Diet comprises primarily 0-group sandeel, 1-group sandeel, clupeids, and other; energy densities derived from lengths using specific equations; other category fixed at 5.1 kJ g⁻¹
  - Diet-wide energy density calculated as a weighted mean by yearly diet composition (2010–2014)
- Assimilation efficiency and BMR:
  - Assimilation efficiency and BMR values drawn from cited sources and applied across species

## Geographic and temporal scope
- Focus on seabirds breeding in the UK & British Isles.
- Temporal context linked to 2010–2014 (FAME project period) with supplementary long-term study data (IMLOTS).

## Data quality and access
- Data stored in a single CSV file with restricted access to ensure quality control.
- Funding sources include NERC ECOWINGS and UKCEH National Capability; Isle of May access acknowledged.

## Practical relevance for Environmental Monitoring
- Enables consistent, cross-species comparison of energy budgets during chick-rearing, aiding interpretation of population demography and responses to environmental change.
- Connects energetic requirements to prey availability and diet composition, supporting assessments of how wind farms, climate shifts, and prey dynamics may affect seabird provisioning and colony success.
- Provides a standardized parameter set (with explicit sources) suitable for integration into monitoring dashboards, policy evaluations, and ecological models.