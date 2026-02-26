# Time-activity budgets and energetics of common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake

- Objective and scope
  - Presents a dataset detailing key behavioral and physiological traits for four seabird species (guillemot, razorbill, Atlantic puffin, black-legged kittiwake) during chick-rearing.
  - Captures core metabolic costs and time allocations, with links to prey fish energy intake.
  - Primary geographic focus on the UK & British Isles; data largely from the Isle of May long-term study and the Future of the Atlantic Marine Environment (FAME) project (2010–2014).

- Data structure
  - A single CSV file named Seabird_energetics_parameters.csv.
  - Five columns: one parameter name, plus four species-specific value columns (Guillemot, Razorbill, Kittiwake, Puffin).
  - Includes 24 parameters detailing time budgets, energetic costs, provisioning, life history, and prey/diet metrics.

- Parameters overview (categories)
  - Time-activity budgets (percent time or hours per 24 h): 
    - TB_foraging, TB_foraging_sd, TB_flying, TB_flying_sd, TB_resting_sea, TB_resting_sea_sd, TB_nest, TB_nest_sd.
  - Energetic costs of core behaviors (kJ day-1; inferred from 24 h of activity):
    - ER_foraging, ER_flying, ER_resting_sea, ER_nest, ER_warming_food.
  - Provisioning and chick-rearing:
    - chick_ER, chick_ER_sd, CR_duration.
  - Adult body mass and changes:
    - init_mass, init_mass_sd, mass_change.
  - Body/energy densities and efficiencies:
    - tissue_en_dens, energy_prey_conv, assim_effic, assim_effic_sd.
  - Basal metabolic rate:
    - BMR.
  - Also included are dietary energy considerations:
    - energy density of prey components (derived from prey lengths) and weighted mean prey energy density for each year (2010–2014).

- Values and units
  - Time budgets: mean hours per activity per 24 hours or percentages.
  - Energetic costs: kJ per day (per core behavior and provisioning).
  - Mass and density metrics: grams (g) and kJ g^-1.
  - Chick-rearing duration: days.
  - Assimilation efficiencies and BMR expressed as percentages or kJ day^-1 as appropriate.

- Calculation methods and data sources
  - Time budgets derived from body- and device-based observations:
    - Guillemot and razorbill: activity logger data; puffin and kittiwake methods summarized from literature.
  - Energetic costs:
    - Foraging and flight costs compiled from literature; foraging costs weighted by diving vs. surface rest.
    - Rest-at-sea costs based on BMR ratios, with adjustments to guillemot values.
    - Nest costs set to 2×BMR per day; warming costs scaled from great cormorants using predicted intake based on body mass.
  - Diet and prey energy:
    - Diet composition from Isle of May Long Term Study (2010–2014); prey energy densities for sandeel and clupeids derived from length-based conversions; other prey set to a nominal energy density.
    - Overall diet energy density calculated as a mean, weighted by prey category representation across years.
  - Additional parameters:
    - Provisioning costs per chick drawn from species-specific studies.
    - Chick-rearing duration from IMLOTS data.
  - Sourcing summary:
    - Key references include Thaxter et al., Daunt et al., Harris and Wanless, Newell et al., Searle et al., Wakefield et al., Wanless et al., and others (covers long-term datasets and specific energetic estimates).

- Geographic and temporal scope
  - Species breeding in UK & British Isles with parameter values tied to the study period 2010–2014 (FAME) and Isle of May data; some mass and rate values sourced from other period studies.
  - Long-term context provided by IMLOTS data for life-history parameters.

- Data quality and access
  - Data stored in a single CSV file with restricted access (secure, no shared access).
  - Quality control implied by consolidation from multiple peer-reviewed sources and long-term datasets.

- Potential applications (Data Support perspective)
  - Supports analyses linking seabird energetics to prey availability and demographic outcomes.
  - Useful for population modeling, ecological forecasting, and assessments of environmental change impacts on energy budgets.
  - Provides a standardized, cross-species parameter set for comparative energetics and for informing management decisions related to UK seabird populations.

- Funding and acknowledgments
  - Funded by NERC ECOWINGS, UKCEH National Capability for UK Challenges programme; acknowledgments credit Isle of May access and various collaborators.

- References for context
  - Integrates data and methods from foundational seabird energetics and foraging literature (e.g., Thaxter et al., Harris & Wanless, Wakefield et al., Newell et al., Searle et al., Wanless et al.).