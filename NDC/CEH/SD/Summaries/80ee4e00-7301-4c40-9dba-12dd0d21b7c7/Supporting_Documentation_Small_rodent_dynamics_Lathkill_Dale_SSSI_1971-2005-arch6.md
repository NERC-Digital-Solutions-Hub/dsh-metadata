# Dataset: Small rodent dynamics at Lathkill Dale SSSI, Derbys, 1971-2005

## Overview
- 35-year dataset (1971–2005) of 6-monthly population sampling for bank voles (Myodes glareolus) and wood mice (Apodemus sylvaticus) in a Derbyshire ash woodland.
- Includes environmental proxies: annual ash fruit-fall (Sept–Dec and Jan–Mar) and winter severity (mean minimum daily temperature Dec–Mar).
- Contains a 4-year experimental subarea where supplementary ash fruit was added in two winters, with parallel data from a nearby control area.
- Populations estimated via catch-mark-release live-trapping (90 Longworth traps on a 0.45 ha grid) during two 24-hour periods per session; additional data on fruit-fall collection and winter temperature.
- Data collected to explain between-year demographic changes using a state-space modelling approach; density indices validated against model-generated population estimates.

## Study design and data collection
- Location: Lathkill Dale, Derbyshire (0.45 ha grid; ash Fraxinus excelsior dominated woodland; moderate slope, NNW aspect).
- Study areas: Control area and an experimental area ~150 m away with similar vegetation and aspect.
- Trapping regime: Two 24-hour trapping periods per session, approximately every six months from 1971–2005; 90 traps arranged in a 6×5 grid at 3-trap groups.
- Population data: 
  - Adults and juveniles captured and counted; data include counts per trapping session and density indices (e.g., Zippin estimates for abundance).
  - Separate datasets for November/December (winter) and May/June (summer) sampling.
- Environmental data:
  - Winter severity: mean minimum daily temperature Dec–Mar (from Buxton Met Station).
  - Ash fruit-fall: dry-weight edible ash seeds (g m^-2) split into Sept–Dec and Dec–Mar/Apr; measured annually using dustbins and processed to edible seed weight.
- Experimental manipulation:
  - In 1981–82 and 1984–85, 60 kg of heat-sterilized ash fruit distributed in a subgrid to simulate natural fruit-fall; compared against the main control area.

## Variables and data structure
- Species-specific datasets:
  - Bank voles (Myodes glareolus): winter temperature, annual ash fruitfall (Sept–Dec; Jan–Mar), trapping dates, adult/juvenile counts (Nov/Dec and May/June), density indices, population estimates, and related comments.
  - Wood mice (Apodemus sylvaticus): winter temperature, annual ash fruitfall, trapping dates, adult/juvenile counts (Nov/Dec and May/June), density indices, population estimates.
- Experimental vs control:
  - Separate data files for control and experimental areas enable direct comparison of dynamics under differing fruit-fall regimes.
- File types (examples):
  - Apodemus data and environmental variables (e.g., FlowerdewApodemusData041212csv.csv)
  - Apodemus control and experimental data (e.g., FlowerdewApodemusExData040613Controlcsv.csv, FlowerdewApodemusExData040613Experimentalcsv.csv)
  - Myodes data and environmental variables (e.g., FlowerdewMyodesData291112csv.csv)
  - Myodes control and experimental data (e.g., FlowerdewMyodesExData040613Controlcsv.csv, FlowerdewMyodesExData040613Experimentalcsv.csv)
- Key fields across files include year of June data collection, dates of collections, counts of adults/juveniles, and population estimates (where applicable).

## Modelling and analysis
- Modelling approach: State-space model applied to 33 years of live-trapping data to explain between-year variations in reproductive and population growth rates.
- Indices: Total marked adults used as density indices, validated against model-generated population estimates.
- Environmental drivers:
  - September–March ash fruit-fall as a primary driver of bank vole spring reproductive rate and population growth.
  - September–March fruit-fall shows a weak influence on wood mouse spring reproductive rate; September–December fruit-fall weakly influences summer growth.
  - Winter severity affects bank vole winter growth and wood mouse spring reproductive rate; neither species shows winter breeding.
- Population dynamics: Density-dependence significantly affects winter and summer growth rates for both species.
- Experimental findings: Ash fruit addition experiments confirm the influence of fruit-fall on bank vole demography, with effects often lasting a year or more.
- Cross-species insights: Independent food and weather influences on bank vole demography; observed interspecific differences align with broader perspectives on rodent responses to masting and climate.

## Key findings
- Sept–Mar fruit-fall is the major driver of bank vole spring reproductive rate and population growth; weaker but detectable signals for wood mice.
- Winter severity impacts bank vole winter growth and wood mouse spring reproduction; no winter breeding observed.
- Density-dependence plays a significant role in both species across seasons.
- Ash fruit addition supports the importance of fruit-fall in shaping bank vole demography; effects can persist beyond a single year.
- The study highlights interspecific variation and emphasizes long-term, delayed effects of mast events on small mammal populations.
- Annual ash fruit-fall values reached around 22.52 g m^-2, with oak woodlands typically higher but shorter-lived, which may account for differences in winter breeding behavior.

## Data products and uses for Data Support archetype
- Potential dashboards and self-serve analyses:
  - Time-series visualizations of vole and wood mouse densities alongside fruit-fall and winter severity.
  - Lag analyses to explore delayed effects of mast on demography (up to 1+ year).
  - Comparisons between control and experimental areas to assess fruit-fall manipulation effects.
- Data integrations:
  - Combine Myodes and Apodemus datasets with environmental variables to build multi-species demographic models.
  - Reproduce state-space modelling frameworks to explore causal links between climate, food availability, and population dynamics.
- Outputs for end users:
  - Interactive charts of seasonal population indices, fruit-fall totals, and temperature indices.
  - Summary reports linking environmental drivers to reproductive and growth rates for each species.

## Data quality, limitations, and considerations
- Scope: Single woodland system; findings may not generalize across different habitats.
- Temporal gaps: Long-running dataset with consistent six-monthly sampling; some years have negligible fruit-fall, which is explicitly captured via the experimental grid for interpretation.
- Data structure: Multiple files with control vs experimental designs; careful alignment needed when merging datasets (dates, units, and column definitions vary by dataset).
- Measurements and units: Population indices (density estimates) and counts; ash fruit-fall expressed as g m^-2 dry edible seed; winter severity in degrees Celsius. Ensure consistent unit handling when integrating datasets.
- Documentation: Detailed methodological notes accompany the data (trapping regime, fruit collection, temperature measurement, and modelling approach) to enable reproducibility and proper interpretation.