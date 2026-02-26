# Time-activity budgets and energetics of common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake

## Overview
- Describes a dataset of key behavioural and physiological traits for four seabird species: common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake.
- Focuses on daily time allocation to core activities and metabolic costs during chick-rearing, a period critical for population demography.
- Links energy requirements to prey fish intake and diets (primarily UK & British Isles breeding birds).
- Parameter values drawn from Isle of May long-term study (IMLOTS) and the Future of the Atlantic Marine Environment (FAME) project (2010–2014), with broader literature sources.
- Data support understanding of energetic demands and how they scale with body mass, diet, and chick provisioning; intended for integration into broader seabird energetics and population models.

## Data structure
- Single .csv file: Seabird_energetics_parameters.csv with five columns:
  - parameter (name)
  - Guillemot
  - Razorbill
  - Kittiwake
  - Puffin
- Table 1 describes parameter names, details, and units.
- Values include means (μ) and standard deviations (sd) where applicable.

## Key parameters (names, meaning, units)
- TB_foraging, TB_foraging_sd: Time budget for foraging (%time per 24 h) and its sd.
- TB_flying, TB_flying_sd: Time budget for flight (%time) and sd.
- TB_resting_sea, TB_resting_sea_sd: Time at sea rest (%time) and sd.
- TB_nest, TB_nest_sd: Time at nest (%time) and sd.
- ER_foraging: Energetic cost of foraging (kJ day^-1).
- ER_flying: Energetic cost of flight (kJ day^-1).
- ER_resting_sea: Energetic cost of resting at sea (kJ day^-1).
- ER_nest: Energetic cost of nest time (kJ day^-1).
- ER_warming_food: Energetic cost of warming food (kJ day^-1).
- chick_ER, chick_ER_sd: Energetic cost of provisioning per chick (kJ day^-1) and its sd.
- CR_duration: Chick-rearing duration (days).
- init_mass, init_mass_sd: Adult body mass (g) and sd.
- mass_change: Proportional change in adult body mass during chick-rearing (%).
- tissue_en_dens: Seabird tissue energy density (kJ g^-1).
- energy_prey_conv: Prey energy density (kJ g^-1).
- assim_effic, assim_effic_sd: Digestive assimilation efficiency (%).
- BMR: Basal metabolic rate (kJ day^-1).

## Time-activity budgets (middle section)
- Budgets are derived from species-specific data sources:
  - Guillemot and razorbill: full budgets from activity loggers (Thaxter et al., 2010, 2013).
  - Kittiwake: combination of foraging trip timing (flight, foraging, rest) with nest vs. foraging time allocation (Daunt et al., 2002; 2006).
  - Puffin: budgets based on flight, foraging, resting at sea from activity data (Harris et al., 2012; Harris & Wanless references).

## Energetic costs of core behaviours (middle section)
- Foraging: calculated as an average of diving and rest-at-sea costs, weighted by foraging time; uses 5.25 × BMR as a baseline for pursuit-diving costs (varies by species data sources).
- Flight: species-specific costs drawn from Enstipp et al. (2006), Thaxter et al. (2013), Searle et al. (2014).
- Rest at sea: calculated from BMR with an adjustment factor (1.39) based on guillemot data (revised for consistency with other sources).
- Nest: cost approximated as 2 × BMR.
- Warming food: available for great cormorant (scaled to seabird intake ratios by body mass using Nagy 2001).
- Provisioning per chick: species-specific values from Thaxter et al. (2013), Harris & Wanless (1986), Harris (1979), and Enstipp et al. (2006).
- Chick-rearing duration: typical days from Isle of May long-term data (IMLOTS, Newell et al., 2022).

## Additional parameters and sourcing (middle to end)
- Adult body mass (init_mass, init_mass_sd): breeding masses for each species from literature (Thaxter et al., 2013; Enstipp et al., 2006; Harris, 1979).
- Mass change during chick-rearing: species-specific estimates where available (guillemot: 0.41% daily; kittiwake: IMLOTS data; puffin: May–July mass change; razorbill: not available).
- Seabird tissue energy density (tissue_en_dens): available for guillemots (Gabrielsen, 1996).
- Prey energy density (energy_prey_conv): derived from diet data; prey categories include 0-group sandeel, 1-group sandeel, clupeids, and others (Wanless et al., 2018); energy densities calculated using length-based conversions (Harris & Hislop, 1978) and fixed values for other prey.
- Diet composition: Isle of May Long Term Study data used to weight energy densities by diet representation (2010–2014).
- Assimilation efficiency (assim_effic, assim_effic_sd): Hilton, Furness, Houston (2000).
- Basal metabolic rate (BMR): Bryant & Furness (1995).

## Data provenance and quality
- Data sources include IMLOTS (Isle of May), FAME (2010–2014), and multiple peer-reviewed studies.
- Data stored in a single secure CSV with no shared access, supporting reproducibility and controlled use.

## Usage notes and limitations
- Values may reflect period-specific contexts (e.g., 2010–2014 for FAME) and long-term observational data.
- Some parameters have missing values for certain species (e.g., mass change not available for razorbill; puffin estimates limited by May–July data), requiring careful interpretation when cross-species comparisons are made.
- Methodologies for deriving budgets and costs vary by species and source, with explicit notes on how costs were calculated (e.g., dive-to-pause ratios, BMR-based scaling).

## Relevance for data leadership and data strategy
- Demonstrates a structured, multi-source data integration effort spanning field observations, literature synthesis, and model-based calculations to produce a cohesive energetics dataset.
- Highlights crucial data-system considerations:
  - Clear data structure and a single source file to improve discoverability and governance.
  - Explicit documentation of parameters, units, and calculations to support reuse.
  - Provenance trails linking to diverse data origins (long-term studies and literature) for transparency.
- Illustrates common data access barriers and gaps observed in broader data ecosystems (e.g., limited per-species data for some parameters, reliance on historical datasets, need for standardized metadata and harmonization across studies).

## Funding and acknowledgements
- Funding from NERC ECOWINGS (NE/X009068/1) and UKCEH National Capability for UK Challenges (NE/Y006208/1).
- Acknowledges contributions from numerous researchers and institutions involved in data collection and analysis, including Isle of May access.