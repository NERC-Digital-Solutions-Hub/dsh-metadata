# Site description

- Long-term alpine research site located in Gunnison National Forest, Colorado (38.978725°N, 107.042104°W) at ~3540 m elevation on a southeast-facing ridgeline with ~20% slope.
- Substrates: Mancos shale downslope and quartz monzonite porphyry upslope, with a surface layer of loose weathered gravel; bedrock within 5–10 cm.
- Vegetation: primarily barren or sparse (0–10% cover) during the short summer season.
- Climate/conditions: snow typically accumulates October–June/July; strong west-to-east winds are common; avalanches are rare.
- Experimental design: fifty 2 × 2 m permanent plots arranged in a 5 × 10 grid along the ridge (approx. 40° heading) with 2 × 2 m buffers; overall site footprint about 18 × 38 m.

- Data types collected (overview of datasets)
  - Census data (plants per plot, 2014–2017)
  - Microenvironment data (high-resolution environmental mapping within plots)
  - Macroenvironment data (annual climate context from a nearby weather station)
  - Functional trait data (belowground and aboveground plant traits)
  - Data summarization/analysis outputs (niche, growth, recruitment, mortality, fecundity, trait neighborhoods)

- Data management context
  - Species identifications rely on herbarium vouchers (RMBL).
  - One plant seedling could not be identified and was labeled Indet indet.
  - Permanent plant tagging and precise spatial localization (to the cm) are used for tracking individuals across years.
  - A substantial portion of measurements were obtained from field instruments, with results processed and summarized through statistical techniques (e.g., kriging, PCA).

- Scope of measurements and sampling details
  - Census: annual in late July/August; enumerate every individual, record size metrics, recruit/dormancy/death status, and fecundity (floral structures).
  - Microenvironment: measurements at each plot corner (2 m resolution) with subsequent 10 cm interpolated maps; includes substrate temperature, slope, aspect, trail-disturbance proxy, soil moisture (shallow and deep), soil texture, soil chemical properties (subset of samples), and soil hardness (penetration energy density).
  - Macroenvironment: annual precipitation from January–July, using data from a proximate weather station (4.5 km away).
  - Functional traits: collected from adjacent non-plots individuals to avoid plot disturbance; includes root traits (length, depth, volume, specific root length, root tissue density), AMF and DSE colonization, leaf traits (thickness, area, specific leaf area, leaf dry matter content), tissue biomass fractions, photosynthetic capacity (per-mass, via LiCor), leaf carbon and nitrogen concentrations, stable isotopes (δ13C, δ15N), and fruit/seed metrics (seed set, mean seed mass).
  - Seeds: 10 mature fruits per species sampled in 2015 to assess fertility and seed size distributions.

- Data processing and summarization methods (high-level)
  - Microenvironment: kriging to create 10 cm resolution grids; PCA on standardized variables; realized niche centroids derived from presence/absence mapped to a 20,000-cell grid.
  - Vital rates: recruitment (new establishment), growth rate (change in vegetative length), mortality (death in a year), fecundity (number of floral structures).
  - Trait data: species means with gap-filling for a small portion of missing data; trait PCA with eigenvalue-based component selection.
  - Neighborhood analyses: quantified trait differentiation and hierarchical trait relationships between species; calculated crowding and mean trait differences/hierarchy within a 50 cm radius around focal plants, incorporating plant size as weights.
  - Data integration: multi-step summarization across micro/macroenvironment, demographics, and functional traits to enable analyses of realized niches, vital rates, and trait-based neighborhood effects.