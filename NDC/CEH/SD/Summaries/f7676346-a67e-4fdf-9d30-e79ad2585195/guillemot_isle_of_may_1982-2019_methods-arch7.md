# Data collection methods (adapted from Wanless et al. (2023) Journal of Animal Ecology ) with subheadings used in the Methods of that paper

## Population trends and environmental data
- Longitudinal counts of breeding common guillemot pairs on the Isle of May from 1982–2019, using standardized early-June counts.
- Mean spring sea surface temperatures (sSST) in February–March computed over a foraging-area box around the Isle of May (56°–57°N, 1°–3°W).
- Data sources include the Isle of May studies and the Bundesamt für Seeschifffahrt und Hydrographie (BSH) marine data.

GIS considerations:
- Spatial scope fixed to Isle of May; potential to map year-by-year breeding density and SST overlays over defined foraging areas.
- Temporal resolution: annual counts plus monthly/seasonal SST context.

## Breeding phenology, fledging success and chick growth index
- Chick rearing data from 536–1014 breeding pairs annually (mean ~832 ± 114 SD) across ~250 m of cliff on the island’s west side.
- Daily checks (3–5 times) to determine hatching dates and fledging dates; fledging defined as reaching 15 days of age unless otherwise noted.
- Fledging success: proportion of hatched chicks that fledged.
- Fledging age measured as days between hatching and the morning first observed absent.
- Wing length threshold for fledging: ≥ 60 mm; mass and mass/wing-length relationships used to index fledging mass and growth rate (g/mm) for chicks with wing lengths 25–59 mm.
- Annual sample sizes for body mass/wing data: n ≈ 59 chicks per year (range 6–140).

GIS considerations:
- Individual chick growth and fledging dates can be linked to nest/cliff location data for spatial analysis of phenology.
- Foraging and habitat context can be overlaid with cliff-type or density data to explore spatial drivers of growth and fledging success.

## Parental effort
- Parental attendance measured in chicks during the chick-rearing period; joint presence vs one parent vs neither present.
- 33-year dataset with mid-day checks (when attendance is least variable and dual parenting is most common; annual mean ~287 chicks in peak period; range 99–449).
- Daily observations across the chick-rearing period used to compute annual index of parental effort as a weighted sum (WS) ranging from 0 (both parents present) to 2.0 (neither parent present).
- States: both parents (i=0), one parent (i=1), unattended (i=2) with state values X0=0, X1=1, X2=2; weights Wi are the observed proportions in each state.
- For a subset (32 days over 22 years) detailed behavioural data captured time spent together post-feeding.

GIS considerations:
- Parental effort index can be mapped at colony-level and linked to chick outcomes (growth, fledging) and to environmental covariates.
- Opportunity to analyze spatial patterns if multiple colonies or plots are included in the future.

## Guillemot chick diet
- Diet quantified by recording prey species and qualitative length class (very small to very large) of fish fed to chicks throughout the day during the chick-rearing period.
- Length classifications calibrated to actual fish lengths measured from fish collected during ringing.
- Major prey families: Ammodytidae (lesser sandeel) and Clupeidae (sprat; occasional herring).
- Calorific values determined from fish samples via calorimetry (1985–1987) and subsequently from body composition; components measured include fat, protein, ash, and mineral content.
- Energy values computed using fat (39.6 kJ/g) and protein (23.7 kJ/g) equivalents.
- Systematic all-day feeding watches in two plots to record frequency of chick feeds (annual mean ~57 feeds; range 19–158; typically 2–8 days of observation per year).
- Annual estimates produced for prey composition (by number) and mean prey length; species-specific energy-value relationships derived; annual calorific-value differences explained relative to species-specific curves.

GIS considerations:
- Diet data include spatially explicit observations in two plots; can be mapped to show spatial variation in prey types and energy supply.
- Integrating diet with chick growth and survival enables spatially-informed foraging ecology analyses.

## Adult survival and body mass
- Adults marked with unique color rings; extensive resighting efforts across breeding and nearby areas; mean annual marked count ~326 (range 101–418) with 1025 individuals observed across years.
- Adult overwinter survival estimated with Bayesian Cormack-Jolly-Seber models (JAGS in R), full time dependence assumed; non-informative priors for survival and recapture probabilities.
- For chicks, adults caught near breeding areas (mean 41 adults per year; range 1–130) weighed to the nearest 5 g to obtain mean mass of chick-rearing adults.

GIS considerations:
- Mark-recapture data can be integrated with location data to assess spatial fidelity and movement patterns across years.
- Link adult mass data to environmental variables (e.g., SST, prey availability) and breeding outcomes.

## References
- Key methodological and analytical references are cited (Wanless et al. 2023; Harris et al.; Thaxter et al.; JAGS/R implementations; calorimetry methods; etc.), providing the data protocols and analytical approaches used in these collections.

Overall relevance for GIS Specialists
- The study provides multi-temporal, multi-layer datasets (counts, phenology, parental effort, diet composition, energy content, survival, and body mass) all tied to spatially defined sites (Isle of May, two diet plots, cliff locations).
- Data integration across years and data types supports GIS-driven analyses of spatial-temporal trends, habitat associations, foraging ecology, and demographic outcomes.
- Potential GIS products include temporal maps of breeding density, phenology timelines by location, spatial overlays of parental effort with chick success, diet- and energy-availability maps, and comprehensive dashboards combining environmental drivers (SST) with demographic metrics.