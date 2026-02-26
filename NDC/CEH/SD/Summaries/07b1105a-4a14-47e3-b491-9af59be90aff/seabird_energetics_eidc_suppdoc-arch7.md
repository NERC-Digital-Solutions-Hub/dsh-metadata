# Time-activity budgets and energetics of common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake

- A dataset describing key behavioural and physiological traits for four seabird species during chick-rearing, focusing on daily time allocation and metabolic costs.
- Primary aim: enable map-based understanding of energy requirements and how they relate to prey intake and colony dynamics.

## Data structure and contents

- Single CSV: Seabird_energetics_parameters.csv
  - Columns: parameter (name) + four species columns: Guillemot, Razorbill, Kittiwake, Puffin
  - 24 parameters detailing time budgets and energetics, plus body mass, prey energy, and efficiencies.
- Parameter categories
  - Time budgets (percent time per 24 h): TB_foraging, TB_foraging_sd, TB_flying, TB_flying_sd, TB_resting_sea, TB_resting_sea_sd, TB_nest, TB_nest_sd
  - Energetic costs (kJ day-1): ER_foraging, ER_flying, ER_resting_sea, ER_nest, ER_warming_food
  - Provisioning and life-history: chick_ER, chick_ER_sd, CR_duration
  - Morphometrics: init_mass, init_mass_sd, mass_change
  - Diet and physiology: tissue_en_dens, energy_prey_conv, assim_effic, assim_effic_sd, BMR
- Units and interpretation
  - Time budgets: %time per activity (mean and SD where provided)
  - Energetic costs and provisioning: kJ day-1
  - Other metrics: days (CR_duration), grams (body mass), kJ g-1 (tissue and prey energy densities)

## Spatial and temporal context

- Focus region: UK & British Isles; data linked to UK seabird populations and diet.
- Temporal scope: primarily 2010–2014 for the FAME project; chick-rearing period (energetics during chick provisioning) and Isle of May long-term study context.
- Data sources for parameters span multiple studies and years (e.g., IMLOTS, Thaxter et al., Wakefield et al., Harris & Wanless, etc.).

## Key parameters and their significance for GIS use

- Time budgets
  - TB_foraging, TB_flying, TB_resting_sea, TB_nest (and SDs): enable spatial mapping of activity allocation across colonies and habitat types.
- Energetic costs
  - ER_foraging, ER_flying, ER_resting_sea, ER_nest, ER_warming_food: support raster or polygon-based energy demand surfaces by species and life stage.
- Life-history and provisioning
  - chick_ER, chick_ER_sd: quantify energy devoted to chick provisioning per day.
  - CR_duration: duration of chick-rearing period (days) for temporal layering in GIS analyses.
- Morphometrics and diet
  - init_mass, init_mass_sd, mass_change: relate body condition dynamics to energy budgets.
  - tissue_en_dens and energy_prey_conv: link energy density of tissues and prey to diet-attribution maps.
  - assim_effic, assim_effic_sd, BMR: underpin assimilation and baseline metabolism across locations and years.
- Diet composition and prey energy
  - energy_prey_conv, prey energy densities (derived for sandeel and clupeids; fixed values for other prey) allow aligning energy budgets with spatial prey distribution datasets.

## Provenance, quality, and notes

- Data provenance: compiled from long-term field studies and published literature; primary sources cited for each parameter (e.g., IMLOTS, FAME, Thaxter et al., Wakefield et al., Harris & Wanless, etc.).
- Quality control: stored in a single CSV file; access restricted to maintain data integrity.
- Limitations and considerations for GIS
  - Some parameters are species- or year-specific and may require careful alignment with local colony data.
  - Data are aggregated across years/contexts where applicable; not all parameters have identical year-by-year resolution.
  - While geospatial coordinates are not embedded in the CSV, the data are meant to be integrated with colony locations, tracking data, prey density maps, and habitat layers for GIS analyses.

## GIS-ready applications and use cases

- Create species- and colony-level energy demand maps to assess spatial patterns in chick-rearing costs.
- Overlay energy budgets with prey-density and diet composition layers to explore spatial mismatches or foraging constraints.
- Build bioenergetic models in GIS that couple time budgets with energy costs to predict colony-level nutrition and population consequences.
- Temporal analyses by aligning CR_duration, provisioning costs, and colony phenology with seasonal habitat changes and wind/oceanographic layers.
- Support environmental impact assessments (e.g., offshore wind developments) by modeling potential changes in energy requirements and provisioning pressure across sites.

## Summary of relevance to GIS Specialists

- The dataset provides structured, parameterized energetics and behavior for four seabird species, suitable for creating map-based visualizations of foraging effort, energy expenditure, and provisioning dynamics.
- Key geospatial value comes from combining these parameters with colony locations, prey-density surfaces, and environmental covariates to produce informative GIS products for policymakers, researchers, and the public.