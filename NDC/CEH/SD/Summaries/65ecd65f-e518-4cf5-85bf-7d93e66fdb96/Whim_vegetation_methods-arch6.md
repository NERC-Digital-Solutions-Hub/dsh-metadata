# Vegetation change at whim Moss (2002 -2016) Materials and methods

## Overview
- Long-term nitrogen deposition experiment conducted at Whim bog, Scottish Borders, combining dry NH3 deposition and wet NH4+/NO3- deposition with vegetation monitoring from 2002 onward.
- aims to understand how elevated nitrogen affects peatland vegetation composition and structure.

## Field site
- Location: Whim bog, Scottish Borders (3◦16′W, 55◦46′N).
- Environment: transition between lowland raised bog and blanket bog, 3–6 m peat depth.
- Climate and hydrology (2002–2016 means): mean air temp 7.9°C, soil temp at 10 cm 7.6°C; annual rainfall 1141 mm (range 734–1486 mm); water table typically ~10 cm below surface (drier in drought 2013, ~24 cm).
- Peat and vegetation: highly acidic peat (pH ~3.4); vegetation includes Calluna vulgaris and Eriophorum vaginatum with mosaics of Sphagnum species; communities include Calluna-dominated blanket mire with variable age/structure.

## Experimental design and treatments
- Nitrogen deposition treatments:
  - Dry deposition: controlled NH3 via a free-air release system; NH3 released when wind from SW, above-freezing temps, wind >2.5 m s-1; NH3 concentrations sampled 0.1 m above vegetation along transects (8–60 m from source); deposition estimated from concentrations and deposition velocities.
  - Wet deposition: replicated plots receive NH4+ or NO3- in rainwater via a sprayer system; target total N deposition rates: 0.8 (ambient control), 1.6, 3.2, 6.4 g N ha-1 y-1; PK (K2HPO4) added at the lowest and highest N levels; rainfall increased by ~10% with N additions.
- Experimental layout:
  - Four blocks; 11 treatment combinations per block (including control and various NH4+/NO3- levels, with and without PK) -> 44 plots total.
  - Sprayer triggered automatically ~every 15 minutes during rain, provided rainwater available, temperature >0°C, wind >5 m s-1; ~120 applications per year; applications spread across the year except mid-winter.
- Data captured per plot include both dry and wet deposition forms, with detailed tracking of deposition fluxes.

## Vegetation survey and data collection
- Vegetation surveys conducted in all plots, typically every two years.
- Within each plot: three permanent quadrats (40 × 40 cm) subdivided into 16 sub-quadrats (10 × 10 cm).
- For each survey, percent cover of all species recorded per sub-quadrat; mean cover calculated per quadrat.
- Species list: bespoke to the study.
- Key data collected per survey include plot, quadrat, sub-square covers, survey date, and species identities.

## Nature and units of recorded values (data schema)
- Core dataset: Whim_veg_2002-2006.csv (and related data across years as available).
- Variables and meanings:
  - year, ASSESSMENT.DATE: survey timing
  - PLOT, QUADRAT: plot and quadrat identifiers
  - SUB.SQUARE.1-16: percent cover of each species in each sub-square
  - SPECIES.LIST.NUMBER, SPECIES.LIST.NAME: species identifiers and Latin names
  - distance_m: distance from NH3 source (for transect plots)
  - Expt: deposition form ("Wet" or "Dry")
  - PK: PK addition status ("PLUSPK" or "MINUSPK"/"0")
  - BLOCK: experimental block identifier
  - TREATMENT: code indicating N form, dose, and PK addition
  - FORM: "Ammonia", "Nitrate" or "Ammonium"
  - Fnh3, Fnh4, Fno3: fluxes of NH3, NH4+, and NO3- to each plot (kg N ha-1 y-1)
  - DOSE: total N deposition to each plot (kg N ha-1 y-1)
- Purpose: enable analysis of N deposition effects on vegetation composition and structure over time.

## Data quality and usage considerations
- Data integrate atmospheric deposition (dry and wet) with plot-level vegetation responses and soil chemistry (monthly soil water sampling for ions).
- Measurements include detailed deposition fluxes, PK treatments, and spatial information (distance to NH3 source) to support analyses of deposition gradients and treatment effects.
- The dataset supports self-serve exploration of temporal trends, treatment responses, and species-level changes under different N deposition regimes.

## References (methods and instrumentation)
- Cape et al. 2008; Leith et al. 2004; Sheppard et al. 2004; Tang et al. 2001; Leeson et al. 2017; Rodwell 1998.