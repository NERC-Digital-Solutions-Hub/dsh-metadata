# Dataset: Small rodent dynamics at Lathkill Dale SSSI, Derbys, 1971-2005

## Overview
- 35 years of semi-annual population sampling for adult and juvenile bank voles (Myodes glareolus) and wood mice (Apodemus sylvaticus) in a Derbyshire ash woodland.
- Includes annual and seasonal ash fruit-fall data and a winter severity measure.
- A 4-year experiment in a nearby area added supplementary ash fruit in two winters to compare dynamics with the main area.
- Aim: understand how food supply (masting), climate, and density affect demographic rates; uses long-term state-space modelling to relate environmental variables to population growth and reproduction.

## Study area and data collection
- Location: Lathkill Dale, Derbyshire, England; ash Fraxinus excelsior woodland, 0.45 ha experimental/control grid.
- Trapping: 90 Longworth traps on a 6x5 grid, sampled over two 24-hour periods at roughly 6-month intervals from 1971 to 2005.
- Environmental data: ash fruit-fall measured (Sept–Mar or Apr) as g per m^2 of dry weight; winter severity indexed by mean minimum daily temperature Dec–Mar from Buxton Met Station.
- Experimental design: in 1981-82 and 1984-85, 60 kg of heat-treated ash fruit distributed on the experimental grid to simulate fruit abundance, enabling comparative analysis with the main area.

## Modelling approach
- State-space model applied to 33 years of live-trapping data to explain between-year variations in reproductive and population growth rates for both species.
- Population indices derived from total marked adults and validated against model-generated population estimates; juveniles assessed similarly.
- Key drivers identified: September–March fruit-fall strongly influences bank vole spring reproductive rate and growth; winter severity affects bank vole winter growth and wood mouse spring growth; density dependence significantly affects both species in winter and summer.
- Fruit-fall experiments confirmed a delayed, lasting impact on bank vole demography (often >1 year).
- Findings highlight species-specific responses and emphasize independent food and weather effects on bank vole demography.

## Data files and structure (CSV datasets)
- Data span: 1971–2005 for bank voles; 1981–1985 for control/experimental comparisons; two study areas (control and experimental) for both species.

- FlowerdewApodemusData041212csv.csv
  - Wood mouse and environmental data (1971–2005)
  - Columns include year, winter severity, annual ash fruitfall (Sept–Dec, Jan–Mar, Sept–Mar), dates of collections, adult/juvenile counts, and density estimates.

- FlowerdewApodemusExData040613Controlcsv.csv
  - Wood mouse data (1981–1985, Control area)
  - Columns include year, collection dates, and daily/summary adult and juvenile counts.

- FlowerdewApodemusExData040613Experimentalcsv.csv
  - Wood mouse data (1981–1985, Experimental area)
  - Columns include year, collection dates, and daily/summary adult and juvenile counts.

- FlowerdewMyodesData291112csv.csv
  - Bank vole and environmental data (1971–2005)
  - Columns include year, winter severity, ash fruitfall (Sept–Dec, Jan–Mar, Sept–Mar), collection date, daily/summary adult and juvenile counts, and density estimates.

- FlowerdewMyodesExData040613Controlcsv.csv
  - Bank vole data (1981–1985, Control area)
  - Columns include year, collection dates, and daily/summary adult and juvenile counts.

- FlowerdewMyodesExData040613Experimentalcsv.csv
  - Bank vole data (1981–1985, Experimental area)
  - Columns include year, collection dates, and daily/summary adult and juvenile counts.

## Key findings and interpretations
- September–March ash fruit-fall is the major driver of bank vole spring reproductive rate and population growth; it also influences subsequent summer dynamics.
- September–December fruit-fall has a weaker influence on wood mouse spring reproduction and on summer growth.
- Winter severity affects bank vole winter growth and wood mouse spring reproduction; neither species breeds in winter.
- Density dependence is a significant factor for both species across winter and summer seasons.
- Ash fruit addition experiments confirmed the fruit-fall influence on bank vole winter demography; effects can last for a year or more.
- Long-term modelling reveals interspecific differences and underscored the importance of independent food and weather effects, with substantial delayed impacts of fruit-fall on bank vole demography.
- Annual ash fruit-fall values peaked at 22.52 g m^-2 of edible seed in the study area (higher in oak woodlands, typically shorter-lived); these dynamics help explain the apparent absence of winter breeding in this system.

## Spatial and temporal context for GIS use
- Spatial unit: 0.45 ha trapping grid within the woodland, enabling map-based visualization of population indices and density estimates over time.
- Temporal coverage: 1971–2005 (longitudinal, with a focused 1981–1985 experimental window).
- Variables suitable for GIS integration: population counts/density indices (adults/juveniles, winter and summer), environmental drivers (winter severity, ash fruit-fall), and experimental treatment status.

## Data quality and usage notes
- Data come from multiple CSV files with consistent but area- and period-specific schemas; careful merging is required by year, area (Control/Experimental), and species.
- Measurement units: ash fruit-fall as g m^-2 (dry weight); temperature in degrees Celsius; population indices via trapping counts and Zippin estimates.
- Some years have no or negligible natural fruit-fall; experimental grids provide controlled contrasts.
- Potential limitations include spatial resolution limited to a single 0.45 ha grid per area and the need to align semi-annual sampling with precise calendar dates.