# Time-activity budgets and energetics of common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake

## Summary
- Presents key behavioral and physiological traits for four seabird species during chick-rearing, focusing on daily time allocation to core activities and metabolic costs.
- Links energy requirements to prey intake rates for different prey classes; UK & British Isles breeding context.
- Data sources include the Isle of May long-term study (IMLOTS) and the Future of the Atlantic Marine Environment (FAME) project (2010–2014), with species-specific parameter values described and sourced.
- Data are organized in a single CSV file (Seabird_energetics_parameters.csv) with five columns: parameter, Guillemot, Razorbill, Kittiwake, Puffin.
- Designed to support analysis, modelling, and comparison of energetic costs across species, aiding population demography understanding and potential management implications.

## Data structure
- File: Seabird_energetics_parameters.csv
- Columns: parameter, Guillemot, Razorbill, Kittiwake, Puffin
- The dataset corresponds to 24 parameters capturing time budgets, energetic costs, provisioning costs, life-history traits, and physiological metrics.
- Table 1 (in the document) lists parameter names, details, and units.

## Parameters and measurements (with units)
- Time budgets (percent time per 24 h):
  - TB_foraging (time foraging)
  - TB_foraging_sd
  - TB_flying (time in flight)
  - TB_flying_sd
  - TB_resting_sea (rest at sea)
  - TB_resting_sea_sd
  - TB_nest (nesting time)
  - TB_nest_sd
- Energetic costs of core behaviours (kJ day-1):
  - ER_foraging
  - ER_flying
  - ER_resting_sea
  - ER_nest
  - ER_warming_food
- Provisioning and chick-related:
  - chick_ER (provisioning energy per chick, μ)
  - chick_ER_sd
  - CR_duration (chick-rearing duration, days)
- Life-history and physiology:
  - init_mass (adult body mass, g)
  - init_mass_sd
  - mass_change (%)
  - tissue_en_dens (kJ g^-1)
  - energy_prey_conv (kJ g^-1)
  - assim_effic (digestive assimilation efficiency, %)
  - assim_effic_sd
  - BMR (basal metabolic rate, kJ day^-1)

## Data sources and calculations
- Time budgets:
  - Guillemot and razorbill: full budgets derived from activity loggers (Thaxter et al., 2010, 2013).
  - Kittiwake: combined foraging-trip time (flight, foraging, rest) with nest vs. foraging time shares (Daunt et al., 2002; 2006).
  - Puffin: budgets derived from flight, foraging, resting-at-sea data (Harris et al., 2012).
- Energetic costs:
  - Foraging: weighted average of diving/resting-at-sea costs; based on 5.25 × BMR for pursuit-diving (varying by species and data availability).
  - Flight: species-specific costs from Enstipp et al. (2006), Thaxter et al. (2013), Searle et al. (2014).
  - Rest at sea: based on BMR scaling (with adjustments for guillemot).
  - Nest: 2 × BMR (per Thaxter et al., 2013).
  - Warming food: scaled from great cormorant values to seabirds using body-mass–based intake equations (Nagy, 2001).
- Provisioning per chick and chick-rearing duration:
  - Species-specific provisioning costs (Thaxter et al., 2013; Harris & Wanless, 1986; Harris & Wanless, 1988; Harris, 1979).
  - CR_duration sourced from Isle of May (Newell et al., 2022).
- Body mass and growth:
  - Adult body masses sourced per species (Thaxter et al., 2013; Enstipp et al., 2006; Harris, 1979).
  - Mass change during chick-rearing (guillemot: 0.41% daily decrease; kittiwake from IMLOTS; puffin estimated from May–July mass difference; razorbill not available).
- Diet energy and assimilation:
  - Seabird tissue energy density (guillemots; Gabrielsen, 1996).
  - Prey energy density derived from Isle of May diet data (2010–2014) using length-based conversions for sandeel and clupeids; other category prey fixed at 5.1 kJ g^-1 (Langton et al., 2014; Nagy, 2001).
  - Assimilation efficiency and its standard deviation (Hilton et al., 2000).
- Basal metabolic rate:
  - BMR values (Bryant & Furness, 1995).

## Geographic and temporal scope
- Geographic focus: breeding seabirds in the UK & British Isles.
- Temporal scope for parameter derivation: primarily 2010–2014 (FAME study period) with supplementary long-term data from Isle of May (IMLOTS) and other literature.

## Data quality and access
- Quality control: data stored in a single CSV file with restricted access.
- Funding and acknowledgments: supported by NERC ECOWINGS and UKCEH; acknowledgments to Isle of May collaborators and NatureScot.

## Applications and considerations for analysts
- Enables cross-species comparison of foraging effort, flight costs, nesting costs, and chick provisioning requirements.
- Supports modelling energy budgets to predict prey needs and potential population-demography outcomes under changing environmental conditions.
- Most parameters are UK/breeding-colony specific; applicability to other regions requires careful consideration of local diets and metabolic rates.

## Funding and references
- Funding: NERC ECOWINGS NE/X009068/1; UKCEH NE/Y006208/1.
- Key references span Thaxter, Harris, Wanless, Newell, Wakefield, Searle, Enstipp, Hulot, Nagy, and others (listed in the document).