# Sampling design

- The document outlines the Countryside Survey (CS) soils sampling framework across multiple years (1978, 1998, 2007, 2019) with a pilot in 2018 and a rolling survey starting in 2019.
- Power analyses determined the number of samples needed to detect significant change; details are in Emmett et al. 2008.
- Rolling survey aims to measure approximately 100 squares each year for five years before repeating, enabling trend detection and national-scale estimates.

## Sample location

- Soils are sampled from CS X-plots within CS squares; each square contains 5 randomly spaced X-plots.
- X-plots within a square are not replicates due to differences in land use, soil types, etc.
- Some X-plots are relocated over time due to destruction, access denial, or relocation uncertainty; each location has a unique repeat identifier (e.g., 2RPT1) corresponding to square 2, repeat plot 1.
- Samples with the same ID come from the same location, though exact sampling coordinates may shift about 2–3 m around a permanently marked 2 m × 2 m plot.
- See Emmett et al. (2008) for further details.

## Sampling

- Soils are collected from the top 15 cm (8 cm for invertebrate samples).
- 1998, 2007, and the rolling 2018/2019–2023 surveys used a soil core hammered into the soil and pulled out; 1978 used a soil pit to sample the top 15 cm.
- In some soils, a full 15-cm core isn’t possible due to stones or shallow soils.
- Core photographs and measurements of core dimensions were recorded in 2007 for some cores (black cores and N mineralization cores).
- The rolling CS survey adopted this method.

## Measurements

- In 1978, only pH and loss-on-ignition (LOI) were measured.
- In CS1990, some soil mapping occurred.
- In 1998, 2007, and the rolling survey (2018/19–2023), multiple cores per X-plot were measured; different cores may have different measurements.
- No chemical analyses are conducted by soil horizons; samples are homogenised before pH and LOI measurements.
- Bulk density was measured in 2007 and 2018/19–2023, but not using ISO bulk density methods (which require a whole core).
- A report on implications and a full method description are available (Emmett et al. 2008).

## Statistical analysis

- Analyses should account for the CS structure; ignoring land class structure can yield stock-and-change estimates rather than national estimates weighted by land classes.
- Bootstrapping is not always used; analyses should consider the CS design, at minimum using a mixed model with square as a random factor to account for multiple X-plots per square.
- For CS, a dispersed set of observations can increase regional precision and coverage when spatial structure is not the primary focus.
- Users should consult UKCEH prior to analysis and interpretation and check CS publications listed on the CS website.
- The CS design emphasizes broad coverage and regional estimates over strict replication at each location.