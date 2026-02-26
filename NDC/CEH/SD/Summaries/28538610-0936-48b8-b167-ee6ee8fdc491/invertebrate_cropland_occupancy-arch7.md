# Annual estimates of occupancy for six invertebrate taxa in areas of high, low and no cropland cover in Great Britain, 1990-2019

## Brief description
- Dataset provides occupancy estimates for six invertebrate taxa (Apoidea bees, Syrphidae hoverflies, Coccinellidae ladybirds, Arachnida spiders, Carabidae ground beetles, Heteroptera plant bugs) in Great Britain across cropland cover categories: high, low, and no cropland, from 1990 to 2019.
- Occupancy defined as the proportion of 1 km grid cells occupied by a species, estimated via a Bayesian occupancy-detection model.
- Each species:year:region combination includes 999 posterior samples.
- Derived from observations compiled by UK recording schemes; data are presence-only and were used as input for the occupancy model.

## Data sources and processing
- Data originate from citizen-science recording schemes and societies (e.g., Bees/Wases/Ants Recording Society; Hoverfly Recording Scheme; UK Ladybird Survey; Ground Beetle Recording Scheme; Terrestrial Heteroptera Recording Scheme; Spider Recording Scheme).
- Records are presence-only and vetting is performed by taxon experts.
- Cleaning and standardisation steps:
  - spatial precision: 1 km; temporal precision: day
  - records outside 1990–2019 excluded; taxonomy standardised to species level (or treated as aggregates when needed)
  - resulting datasets: 6 taxonomic groups with 1,538 species total (e.g., bees: 232; carabids: 221; hoverflies: 250; ladybirds: 41; plant bugs: 264; spiders: 535)
- Detection histories created per visit (1 km site × date) using the sparta R package; presence-only data augmented with a target-group approach to infer non-detections; list length used as a proxy for sampling effort.
- Species filtering:
  - exclude species with insufficient data for reliable estimates
  - exclude Harmonia axyridis (Harlequin ladybird) due to invasion-driven trends
- Final outputs: occupancy models produced for 224 bees, 221 carabids, 250 hoverflies, 41 ladybirds, 264 plant bugs, and 535 spiders.

## Cropland regions
- Cropland classification uses Land Cover Map 1990 and Land Cover Map 2015 (25 m resolution; 15 land-cover classes).
- Cropland defined to include arable and horticultural classes; percentage cover calculated per 1 km cell for 1990 and 2015.
- Sites with cropland change >10% between 1990 and 2015 discarded; cells with >25% in wetlands, built-up, or other classes excluded.
- Regions categorized by cropland cover using an empirical distribution:
  - high cropland: >50%
  - low cropland: 0–50%
  - no cropland: 0%
- Purpose: compare occupancy trends across distinct cropland-intensity regions.

## Occupancy models
- Hierarchical Bayesian occupancy-detection models with two submodels:
  - State (occupancy) submodel: z_it ~ Bernoulli(ψ_it); year effects differ by cropland region (high, low, none) with site effects included.
  - Observation (detection) submodel: y_itv ~ Bernoulli(p_itv × z_it); detection probability p_itv depends on year effect and data type (list length categories: 1, 2–3, or 4+ species observed).
- Model specifics:
  - year effects: bt, with random-walk prior enabling smooth temporal changes and sharing information across years
  - priors: uninformative for all other parameters
  - data-type categories capture varying sampling intensity across visits
- Fitting: occDetFunc (R package sparta) using MCMC via JAGS
  - three chains, 32,000 iterations each, burn-in 30,000, thinning 6

## Model outputs
- Occupancy estimates: proportion of occupied sites (ψ_it) for each region (high, low, no) and year, with a posterior distribution.
- Posterior samples: 999 occupancy samples per region:species:year combination.
- Data availability notes:
  - not all species appear in all cropland regions
  - differing year ranges by taxon: bees, hoverflies, ladybirds, spiders (1990–2019); carabids and plant bugs (up to 2014 and 2016, respectively)

## Data format and content
- Data file: occ_out_pass.csv
- Content: 4,304,691 occupancy estimates across 34 columns
- Columns include:
  - tax_grp: taxonomic group (one of six)
  - species: Latin species name
  - agri: cropland region (high, low, no_agri)
  - iteration: MCMC sample index (1–999)
  - year_1990:2019: Occupancy estimate for each year (0–1)
- Structure: one row per iteration; multiple rows share same species/year/region but differ in iteration
- Note: Table layout indicates presence of intervening years not presented in example rows

## Acknowledgements and references
- Acknowledges volunteer contributors and supporting schemes; funding from NERC grants
- References include methodological foundations for occupancy modelling, citizen science data handling, and related datasets

## Potential GIS use and considerations
- Enables map-based visualization of occupancy trends by species across GB at 1 km resolution and across cropland richness categories
- Useful for spatial policy analysis, conservation planning, and agricultural-land management assessments
- Consider data gaps by taxon and year when designing maps or analyses; account for regional and temporal availability limitations
- The 999 posterior samples per year-region allow uncertainty visualization (e.g., credible intervals) on maps and in GIS analyses