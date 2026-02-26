# Data collection methods (adapted from Wanless et al. (2023) Journal of Animal Ecology) with subheadings used in the Methods of that paper

- Population trends and environmental data
  - 1982–2019: standardized counts of breeding common guillemot pairs on the Isle of May, conducted in early June.
  - Environmental data: mean spring Sea Surface Temperatures (sSST) in February–March for a defined foraging-area around the Isle of May (56°–57°N, 1°–3°W), sourced from Bundesamt fȕr Seeschifffahrt und Hydrographie (BSH).

- Breeding phenology, fledging success and chick growth index
  - Chick-rearing data for 536–1014 pairs annually (mean ~832 ± 114 SD) across cliff types and densities on ~250 m of cliff.
  - Observations 3–5 times daily to determine hatching and fledging dates; fledging defined as at least 15 days old unless otherwise indicated.
  - Fledging success: proportion of hatched chicks that fledged; fledging age is the interval from hatching to the morning a chick is first observed absent.
  - Chick growth metrics: mass for chicks with wing length ≥60 mm as fledging mass; growth rate indices computed as mass/wing-length-related ratios; annual growth rate (g/mm) for chicks during linear growth using wing lengths 25–59 mm.

- Parental effort
  - Measures of parental attendance during chick rearing: both parents, one parent, or neither present.
  - Data collected across 33 years for ~287 chicks (annual mean) with 27 days of observation per year (range 7–37 days) to derive an annual parental-effort index.
  - Weighted sum (WS) index calculated per year with states: both parents (0), one parent (1), neither (2); weights reflect the proportion of chicks in each state.
  - Subset of 32 days over 22 years with detailed behavioral observations on time spent together after chick feeds.

- Guillemot chick diet
  - All-day watches in two plots to record chick-feeding events; annual mean number of chicks fed (~57; range 19–158).
  - Prey identification and qualitative length classification (very small to very large relative to parent bill) used to estimate species composition and mean prey length.
  - Primary prey families: Ammodytidae (lesser sandeel) and Clupeidae (sprat; some herring); prey-fish samples collected for energy content analysis.
  - Calorific values determined through direct body composition analyses in earlier years and later methods; energy values calculated from fat and protein content.
  - Diet data used to derive annual estimates of prey-species proportions (by number) and mean prey length; species-specific length–calorific value relationships developed; annual differences in prey energy values integrated via relative calorific values.

- Adult survival and body mass
  - Mark-recapture: 1025 adults tagged with color rings; mean annual observed adults ~326 (range 101–418).
  - Adult overwinter survival estimated with a Bayesian Cormack–Jolly–Seber model (via JAGS in R) with time-dependent parameters and non-informative priors.
  - Model setup: three independent MCMC chains, 9000 iterations with 900 burn-in, Thinning ×10.
  - Chick-rearing adults captured near breeding areas and weighed to the nearest 5 g to obtain annual mean mass for this group.

- References
  - Includes methodological and analytical sources used to establish counting, growth, diet, and survival measures (e.g., Harris, Wanless, Thaxter and colleagues; JAGS/Bayesian approaches; caloriﬁc-value methodologies).