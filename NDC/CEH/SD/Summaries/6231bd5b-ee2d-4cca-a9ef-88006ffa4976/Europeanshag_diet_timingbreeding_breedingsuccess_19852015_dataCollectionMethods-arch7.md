# Data Collection methods

- Scope and time frame
  - Data collected on shag breeding phenology and success, inshore SST, and diet for Isle of May.
  - Breeding phenology data span 1987–2016 (nests per year: range 35–266); some years missing (1993, 2003).
  - Nests monitored in 18 plots across the colony; nests checked every seven days from before laying to after fledging.

- Breeding phenology and success
  - Lay date estimation: typically three days before the first recorded incubation; in some nests, egg counts on first confirmation allow more accurate lay-date estimates using standard three-day laying intervals.
  - Measurement error: maximum potential lay-date error up to four days (worst case when laying just after last visit); within-year measurement error assumed consistent and smaller than within-year lay-date variance.
  - Data handling: second clutches from failed first clutches not included in core analyses due to non-independence with first-clutch dates; however, an extra analysis tested the effect of the first-clutch lay date on overall breeding success with no qualitative difference. Subsequence models used first laying attempts only.
  - Population counts: annual counts of breeding pairs collected using standardised methods.
  - GIS implications: nest- and plot-level phenology data enable spatial visualization of lay dates, breeding success by location, and year-to-year spatial patterns.

- Inshore temperature data
  - Source: Sea surface temperature (SST) data for February and March from bsh.de.
  - Spatial scope: area around Isle of May overlapping shag foraging distribution (approx. 56°0'–56°4' N, 2°7'–2°3' W).
  - Rationale: late-winter SST is a key driver of sandeel somatic investment and recruitment; population-level lay date also correlates with SST in the same period.
  - Processing: compute mean late-winter SST per year from monthly records.
  - GIS implications: yearly SST rasters or summary layers for the breeding season window can be spatially joined to colonies to explore relationships with breeding metrics.

- Diet
  - Sample collection: regurgitated food from both chicks and adults during chick-rearing (April–July) on the Isle of May, 1985–2014 (n = 863; median 29 samples per year; range 4–69).
  - Temporal alignment: collection dates strongly correlated with shag breeding season timing (median collection date vs. median lay date, r = 0.86).
  - Key diet components: predominantly 1+ group sandeels (≈70% biomass) and 0 group sandeels (≈12% biomass).
  - Seasonal dynamics: 1+ group sandeels are abundant early (April–May) and then decline as they bury; 0 group sandeels become available from June onward after metamorphosis.
  - Energetic differences: 1+ group sandeels larger and higher energy density than 0 group.
  - Hypotheses and variation: yearly variation in the proportion of 1+ group sandeels is influenced by timing and gradient of the proportion change within the breeding season; higher 1+ group proportion is predicted to be associated with higher average breeding success.
  - GIS implications: diet-time series by year, and if available at finer resolution, spatially integrated diet metrics per plot or nest to explore spatial-diet–phenology relationships. Potential to link diet shifts with breeding outcomes and SST context.