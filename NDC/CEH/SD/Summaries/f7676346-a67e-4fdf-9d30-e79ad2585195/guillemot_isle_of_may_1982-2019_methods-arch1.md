# Data collection methods (adapted from Wanless et al. (2023) Journal of Animal Ecology ) with subheadings used in the Methods of that paper

- Population trends and environmental data
  - Counts of breeding common guillemots Uria aalge on the Isle of May conducted from 1982 to 2019 using standardized early June counts.
  - Mean spring Sea Surface Temperatures (sSST) in February–March calculated for a 56°–57°N by 1°–3°W region around the Isle of May, encompassing foraging areas; data sourced from Bundesamt für Seeschifffahrt und Hydrographie (BSH).

- Breeding phenology, fledging success and chick growth index
  - Chick rearing observed annually for 536–1014 pairs (mean 832 ± 114) along ~250 m of cliff; hatching and fledging dates determined from 3–5 daily checks.
  - Fledging defined as the date when a chick aged at least 15 days is first recorded absent (with hatching/fledging dates known to within one day).
  - Fledging mass index derived from weights of chicks with wing length ≥ 60 mm (annual mean N ≈ 59; range 6–140) as an index of fledging mass; annual growth rate (g/mm) calculated from fledging mass and age; linear growth growth-rate index computed from chicks with wing lengths 25–59 mm.

- Parental effort
  - Parental attendance tracked during chick-rearing: proportion of chicks attended by both parents, one parent, or neither.
  - An annual index of parental effort (weighted sum, WS) computed to range from 0 (all chicks attended by both parents) to 2.0 (all chicks unattended); daily observations across chick-rearing period (annual mean days ≈ 27; range 7–37) to capture variation.
  - For a subset of 32 days over 22 years, detailed behavioural observations recorded time a pair spent together after a chick was fed.

- Guillemot chick diet
  - Diet quantified by recording prey species and qualitative length class (relative to parental bill size) during chick-rearing; length classes converted to actual lengths using measured fish from colony encounters.
  - Diet dominated by Ammodytidae (lesser sandeel) and Clupeidae (sprat, with some herring); fish samples collected to determine species-specific calorific values.
  - Calorific values determined via body composition analyses (fat, protein, minerals) and energy equivalents (fat = 39.6 kJ/g, protein = 23.7 kJ/g); energy content assigned to each prey item.
  - All-day watches in two plots recorded the frequency of feeds to chicks; annual estimates produced for prey species proportion by number and mean prey length; species-specific energy values used to derive relative calorific values across years.

- Adult survival and body mass
  - Mark-recapture data from 1025 adults equipped with colour rings to estimate adult overwinter survival via a Bayesian Cormack–Jolly–Seber model implemented in JAGS (R) with non-informative priors.
  - Three independent chains run (9,000 iterations, burn-in 900, thinning factor 10); density-dependent and time-dependent model fitting assumed.
  - A subset of adults with chicks (annual mean 41; range 1–130) captured near breeding sites and weighed to the nearest 5 g to provide annual mean chick-rearing adult mass estimates.

- Data sources, quality assurance and workflow
  - Data collected across multiple facets (population counts, phenology, parental care, diet, and survival) using standardized protocols, with cross-referencing to established methods and prior studies (as cited).
  - Analyses performed to link environmental variables, parental effort, diet quality, and growth/survival metrics, with datasets and methods aligned to reproducible statistical practices (e.g., Bayesian survival modelling and growth indices).