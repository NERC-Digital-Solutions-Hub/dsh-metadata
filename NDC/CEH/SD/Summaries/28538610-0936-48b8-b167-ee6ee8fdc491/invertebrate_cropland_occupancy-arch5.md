# Annual estimates of occupancy for six invertebrate taxa in areas of high, low and no cropland cover in Great Britain, 1990-2019

## Overview
- Mission: Provide occupancy estimates for six invertebrate taxa in Great Britain across regions of high, low, and no cropland cover from 1990 to 2019.
- Data product: 999 posterior samples of occupancy per species, year, and cropland region; derived from a Bayesian occupancy-detection model.
- Taxa: Apoidea (bees), Syrphidae (hoverflies), Coccinellidae (ladybirds), Arachnida (spiders), Carabidae (carabids), Heteroptera (plant bugs).
- Data source: Observations from national volunteer recording schemes, verified by taxon experts, forming presence-only data used as input for occupancy modelling.
- Output format: Occupancy estimates (proportion of occupied 1 km cells) with associated posterior distributions.

## Data sources and processing
- Primary sources: Bees, Wasps, and Ants Recording Society; Hoverfly Recording Scheme; UK Ladybird Survey; Ground Beetle Recording Scheme; Terrestrial Heteroptera Recording Scheme; Spider Recording Scheme.
- Data quality and cleaning:
  - Presence-only records with taxon expert verification.
  - Standardised spatial (1 km) and temporal (day) precision; limited to 1990–2019.
  - Taxonomy standardised to species level where possible; certain taxa modelled as aggregates due to taxonomic changes.
  - Harlequin ladybird (Harmonia axyridis) removed due to invasion-driven trends.
  - Excluded species with insufficient data for reliable trends.
- Data preparation:
  - Detection histories created per visit using formatOccData from the sparta R package.
  - Target-group approach used to infer non-detections in presence-only data.
  - List length used as a proxy for sampling effort.
- Taxa and dataset sizes after cleaning:
  - Bees: 224 species
  - Carabids: 221 species
  - Hoverflies: 250 species
  - Ladybirds: 41 species
  - Plant bugs: 264 species
  - Spiders: 535 species

## Cropland regions classification
- Land cover sources: Land Cover maps for 1990 and 2015 (25 m resolution; 15 classes).
- Cropland definition includes arable and horticultural crops and freshly ploughed land.
- Site filtering:
  - Excluded sites with cropland cover change > 10% between 1990 and 2015.
  - Excluded sites with >25% cover of wetlands, built-up areas, or other non-cropland classes.
- Regional classification:
  - High cropland cover (>50%), Low cropland cover (0–50%), No cropland cover (0%).

## Occupancy models
- Modelling framework: Hierarchical Bayesian occupancy-detection models (state process for true occupancy, observation process for detection given occupancy).
- State model:
  - Occupancy probability ψ_it for site i in year t, with year effects varying by cropland region (high, low, none) and a site random effect u_i.
  - Year effects modeled with a random-walk prior to enable smooth temporal changes.
- Observation model:
  - Detection probability p_itv depends on year effects and data type (list length categories reflecting sampling intensity): 1, 2–3, or 4+ species recorded.
  - Detection conditional on true occupancy (z_it = 1).
- Priors and computation:
  - Uninformative priors for most parameters.
  - Implemented with occDetFunc (sparta) via MCMC (JAGS): 3 chains, 32,000 iterations, burn-in 30,000, thinning 6.
- Outputs:
  - Posterior occupancy estimates (proportion of occupied sites) per region (high, low, no cropland) for each species and year.

## Model outputs and data format
- Data product: occ_out_pass.csv containing 999 posterior samples of occupancy for each species:region:year combination.
- Size and structure:
  - Approximately 4,304,691 occupancy estimates across 34 columns.
  - Columns include year_1990:year_2019, tax_grp, species, agri (region), iteration (1–999), and additional metadata.
- Taxa and year coverage:
  - Bees, hoverflies, and spiders span 1990–2019.
  - Carabids cover up to 2014; plant bugs up to 2016.
  - Not all species appear in all cropland regions due to data availability.
- Data description examples:
  - Rows per iteration; per year a column holds the occupancy estimate (0–1).
  - Example columns: year_1991, year_1992, …, year_2019; tax_grp; species; agri; iteration.
- Format notes:
  - Some species-region combinations are absent from the dataset.
  - The dataset includes 1,535 species across six taxonomic groups.

## Data governance, quality, and limitations
- Provenance and reproducibility:
  - Based on citizen-science data with established QA processes; model code and methodology described and cited.
  - Use of standardised data processing workflow (formatOccData; target-group approach) and transparent modelling framework.
- Limitations and considerations for use:
  - Presence-only data requires assumptions to infer non-detections; list-length as a sampling-effort proxy.
  - Detection probability varies with data type (list length) and year, which influences occupancy estimates.
  - Not all species or regions have complete year coverage; some years are missing for certain taxa.
  - Exclusion of species with insufficient data and the invasive Harlequin ladybird to avoid bias.
- Data sharing and lineage:
  - Data are presented as posterior samples of occupancy, enabling uncertainty to be carried through analyses.
  - Data suitable for meta-analyses of trends across cropland regimes and taxa, subject to the above limitations.
- Acknowledgements and references:
  - Volunteer contributors and funding acknowledgments; extensive references for methods and data sources.

## Acknowledgements
- Thanks to volunteer recorders and supporting schemes; funded by NERC grants NE/S000100/1 and NE/V007548/1.