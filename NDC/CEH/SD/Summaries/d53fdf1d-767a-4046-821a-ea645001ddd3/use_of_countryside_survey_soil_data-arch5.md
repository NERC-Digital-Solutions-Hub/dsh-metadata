# Sampling design

## Overview
- Soil sampling occurred in Countryside Survey (CS) in 1978, 1998, 2007, and 2019.  
- 1978 and 1998 used the same 256 squares; 2007 covered all 591 CS squares but not all measurements were made on all samples.  
- A pilot survey was conducted in 2018; from 2019 a rolling survey aims to measure ~100 squares per year for five years before repeating.  
- Power analyses (Emmett et al. 2008) determined the number of samples required to detect significant change.

## Sample location and plot design
- Sampling sites are CS X-plots, with 5 X-plots randomly spaced within each CS square.  
- X-plots are not replicates because land use, soil type, etc., differ between them.  
- Some X-plots are relocated over time due to plot destruction, access permissions, or uncertainty in original location.  
- Each location has a unique repeat identifier (e.g., 2RPT1) indicating square 2, repeat plot 1; repeat plots are considered the same location, though exact sampling points may be 2–3 m apart around a permanently marked 2 m x 2 m plot.

## Sampling method
- Soils are collected from the top 15 cm (8 cm for the invertebrate sample).  
- 1998, 2007, and the rolling CS survey (2018/2019–2023) use a soil core hammered into the soil and then extracted.  
- 1978 used a soil pit to sample the top 15 cm from the pit side.  
- In some cases, a full 15-cm core could not be collected due to stones or shallow soils.  
- Core photographs and detailed measurements of core dimensions were made in 2007 on some cores (black cores and N mineralization cores). The rolling CS survey adopted this core-based method.

## Measurements and laboratory analyses
- 1978: pH and loss-on-ignition (LOI) only.  
- 1990: some soil mapping conducted.  
- 1998, 2007, and rolling survey (2018/19–2023): multiple cores per X-plot; different cores have different measurements.  
- No chemical analyses are performed by soil horizons; samples are homogenised before pH and LOI measurements.  
- Bulk density measured in 2007 and 2018/19–2023, but not using ISO bulk density method (would require a whole core).  
- A methodological and implications report is available (Emmett et al. 2008).

## Statistical analysis considerations
- Analyses should account for land class structure; ignoring it yields stock/change of the population, while including land classes provides national estimates weighted by land class.  
- Bootstrapping is not always used in analyses of CS data.  
- The CS structure typically uses a mixed model with square as a random factor to account for multiple X-plots within each square.  
- Design-based approach often yields dispersed observations with increased regional precision and coverage, noting that only one core is taken per location.  
- For analysis and interpretation, users should consult UKCEH prior to analysis and check CS publications listed on the CS website.  

## Data governance and provenance notes (implications for Data Stewards)
- Ensure detailed metadata capture for each sampling event: year, square ID, X-plot ID, repeat location ID, exact sampling location relative to the plot, depth, method (core vs. pit), core length and dimensions, and any deviations (stones, shallow soils).  
- Capture measurement specifics: pH, LOI, bulk density, units, analysis year, and whether cores were homogenised before measurement.  
- Track data lineage and methodological changes over time (e.g., transition to rolling survey, adoption of core-based methods, ISO-related notes).  
- Maintain links to key references (e.g., Emmett et al. 2008) and ensure accessible documentation for users planning analyses (including guidance on appropriate statistical models and structure).  
- Ensure unique identifiers (e.g., 2RPT1) consistently map to locations across years, even if exact sampling points shift slightly, to preserve longitudinal traceability.