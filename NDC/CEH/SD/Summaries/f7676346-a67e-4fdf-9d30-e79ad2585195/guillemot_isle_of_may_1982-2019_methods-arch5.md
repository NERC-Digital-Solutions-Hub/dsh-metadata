# Data collection methods (adapted from Wanless et al. (2023) Journal of Animal Ecology ) with subheadings used in the Methods of that paper

## Overview
- Long-term, multi-faceted study of common guillemots Uria aalge on the Isle of May (1982–2019), integrating population, breeding, diet, survival, and parental effort data.
- Incorporates environmental data (sea surface temperature) from external sources to contextualize demographic and behavioral metrics.

## Data types and key variables
- Population trends and environmental context
  - Breeding pair counts conducted in early June (standardized counts).
  - Mean spring sea surface temperatures (sSST) in February–March for a defined foraging-area around the Isle of May.
  - External data source: Bundesamt fȕr Seeschifffahrt und Hydrographie (BSH).
- Breeding phenology, fledging success and chick growth
  - Chick-rearing data across 536–1014 (mean ~832) pairs on ~250 m of cliff; daily checks to determine hatching and fledging.
  - Fledging criteria: fledging age of at least 15 days unless contrary evidence.
  - Fledging mass index: weight of chicks with wing length ≥ 60 mm; annual growth rate (g/mm) calculated during the linear growth window.
- Parental effort
  - Daily chick attendance categorized for each chick: both parents, one parent, or neither.
  - Annual parental effort index (weighted sum, WS) ranging from 0 (both parents present) to 2.0 (neither present); weights correspond to attendance states.
  - Subset of 32 days over 22 years with detailed behavioral observations of pair time spent together after chick feeding.
- Guillemot chick diet
  - Diet quantified via all-day watches in two plots; records of prey species and qualitative length class (relative to parent’s bill: very small to very large).
  - Conversion to actual lengths using year-specific fish measurements; main prey families: Ammodytidae (sandeels) and Clupeidae (sprat, with some herring).
  - Prey energy content determined via calorific analysis (initially via freeze-drying and bomb-calorimetry, later via body composition) to derive energy values; annual estimates of prey proportion and mean species-specific lengths.
  - Data used to generate annual energy-value estimates by integrating calorific value and prey length; relative calorific deviations computed against species-specific length–calorific value curves.
- Adult survival and body mass
  - Marked adults (color rings) tracked across years; mean annual marked birds observed per year recorded.
  - Adult overwinter survival estimated with Bayesian Cormack–Jolly–Seber model (JAGS/R) using non-informative priors; three chains, 9,000 iterations with burn-in and thinning.
  - Chick-rearing adults captured near breeding areas and weighed to the nearest 5 g to obtain annual mass estimates.

## Data collection protocols and design
- Population and environment
  - Standardized June counts; sSST defined in a specific geographic box around the Isle of May to reflect foraging habits.
- Breeding and chick data
  - Visual checks 3–5 times daily during chick-rearing; hatching/fledging dates recorded to within one day when possible.
  - Systematic sampling of chick growth metrics and wing length to compute growth indices and fledging mass metrics.
- Parental effort and behavior
  - Regular mid-day checks during the chick-rearing period for attendance data; comprehensive records across years to derive WS index.
  - Detailed 32-day subset for post-feeding time together analyses.
- Diet and energy analyses
  - Annual all-day feeding watches; dietary samples collected to determine prey species composition and size distribution.
  - Laboratory analyses conducted to derive calorific values and energy content of prey, enabling energy-based diet metrics.
- Adult survival and body mass
  - Intensive marking and recapture surveys; targeted weighing of chick-rearing adults to link mass with reproductive effort.

## Data processing, derived metrics, and interoperability
- Derived metrics
  - Fledging success as a proportion of hatched chicks that fledged.
  - Fledging mass index and growth rate (g/mm) computed from wing length and mass data.
  - Parental effort index (WS) computed from three attendance states with year-specific state proportions.
  - Diet energy values constructed by pairing prey species lengths with calorific values; annual energy-value deviations relative to species-specific curves.
- Processing and statistical methods
  - Bayesian survival analysis (Cormack–Jolly–Seber) implemented in JAGS within R; non-informative priors and multi-chain convergence approach.
  - Data integration across multiple streams (population counts, phenology, diet, survival) relies on consistent sampling windows and clear state definitions.
- Documentation and references
  - Methods and measurement techniques traceable to Harris, Wanless, and colleagues; external data sources and methodological references explicitly cited (e.g., BSH, calorimetry, Bayesian modeling).

## Data provenance, sources, and governance implications
- Provenance
  - Primary field data collected by a long-running team (e.g., Harris & Wanless) across multiple decades; external climate/environmental data sourced from BSH.
  - Laboratory analyses (calorific values, body composition) conducted per established protocols referenced in the literature.
- Governance considerations
  - Opportunity to document lineage of raw vs. derived data, transformation steps, and versioning for reproducibility.
  - Need to capture metadata such as sampling effort, observer effort, date ranges, locations, and exact methods used (e.g., definitions of attendance states, hatching/fledging criteria).
  - Data stewardship should preserve raw measurements alongside derived metrics (growth indices, WS, diet summaries, energy values) to enable reprocessing with updated methods.

## Data quality, limitations, and stewardship recommendations
- Quality considerations
  - Long time span with repeated measures; potential methodological changes or observer variation over years; explicit notes on effort and calibration are important.
  - Complex derived metrics depend on careful standardization of units and definitions (e.g., wing length thresholds, mass measurement precision).
- Limitations and risks
  - Data from external sources (e.g., sSST from BSH) require clear licensing and terms of use.
  - Gaps or uneven sampling across years could affect trend analyses; documentation of missing data and imputation strategies is advisable.
- Stewardship actions
  - Store raw data and all derived metrics with clear, machine-readable metadata, including units, sampling design, and variable definitions.
  - Archive analysis code (R scripts, JAGS models, and any data transformation pipelines) to support reproducibility.
  - Maintain data dictionaries linking variables to published definitions (e.g., states for parental attendance, hatching/fledging criteria).
  - Provide data access controls and citation guidance to ensure proper credit for datasets and lab analyses.

## Endnotes and references
- Data sources and methodological references are cited throughout (e.g., Harris & Wanless, Wanless et al., Thaxter et al., Allen, Crisp, Seber, Jolly, Plummer, R Core Team, etc.), underpinning the data collection, processing, and analysis approaches described.