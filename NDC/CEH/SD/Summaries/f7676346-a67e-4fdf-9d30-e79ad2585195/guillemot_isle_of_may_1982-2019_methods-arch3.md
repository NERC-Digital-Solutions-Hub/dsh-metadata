# Data collection methods (adapted from Wanless et al. (2023) Journal of Animal Ecology ) with subheadings used in the Methods of that paper

## Overview
- Describes long-term, multi-facet data collection on common guillemots (Uria aalge) on the Isle of May to derive environmental health measures.
- Combines population, phenology, chick development, parental behavior, diet, and adult survival data.
- Data span several decades and integrate field observations, measurements, and laboratory analyses.

## Population trends and environmental data
- Population: standardized counts of breeding pairs (1982–2019) conducted in early June.
- Environmental driver: mean spring sea surface temperatures (sSST) in February–March, in the foraging area around the Isle of May (56–57°N, 1–3°W) using data from the German Federal Maritime and Hydrographic Agency (BSH).

## Breeding phenology, fledging success and chick growth index
- Chick rearing: data collected annually for 536–1014 breeding pairs (mean ~832) across cliff types and densities.
- Hatching and fledging: daily checks (3–5 times) to determine hatch and fledging dates; fledging defined as chicks reaching at least 15 days or being absent at the nest.
- Fledging mass and growth: wing length threshold (≥60 mm) used to define linear growth phase; annual chick growth index based on mean fledging mass and age at fledging; growth rate (g/mm) derived from younger chicks (25–59 mm wings).

## Parental effort
- Parental attendance: daily observations during chick-rearing with variable presence (both parents, one parent, or neither).
- Index of parental effort: weighted sum (WS) from 0 (both parents present) to 2.0 (neither present), across 27–37 days per year, with a subset of 32 days of detailed behavior over 22 years.
- Additional behavior: detailed time-together observations for a subset of pairs during the post-feeding period.

## Guillemot chick diet
- Diet assessment: all-day watches in two plots to record frequency of feeds; annual mean chicks observed ~57 (range 19–158).
- Prey identification: classification of fish by species and length class (very small to very large) fed to chicks; conversion to actual lengths using fish collected during ringing.
- Energy content: calorific value determined for key prey (Ammodytidae and Clupeidae) via laboratory analyses; later years used body composition to estimate energy content.
- Diet composition and energy: annual estimates of prey species proportions, mean prey length, and relative calorific value differences to reflect annual dietary energy available to chicks.

## Adult survival and body mass
- Marking: 1,025 adults marked with color rings; intensive annual resighting to estimate survival and site fidelity (high fidelity to previous breeding area).
- Survival analysis: adult overwinter survival estimated with a Bayesian Cormack-Jolly-Seber (CJS) model implemented in JAGS within R; non-informative priors (Uniform 0–1); three chains run with burn-in and thinning.
- Body mass: annual mean mass of chick-rearing adults measured (n ~41 on average; range 1–130).

## Methods and data analysis
- Statistical framework: Bayesian CJS model for survival; R and JAGS used for analysis; robust handling of limited priors and Markov-chain Monte Carlo sampling (burn-in, thinning, multiple chains).
- Data integration: comprehensive combination of observational counts, phenology, diet, and physiological metrics to derive multi-year demographic and energetic indices.

## Implications for monitoring frameworks
- Demonstrates the value of integrated, long-term monitoring across multiple linked data streams (population biology, behavior, diet, physiology, and environmental drivers).
- Highlights the need for standardized, repeatable data collection protocols and transparent metadata (e.g., measurement methods, sampling effort, and data transformations) to support policy evaluation and decision-making.
- Shows how coupling environmental variables (sSST) with demographic and energetic metrics can illuminate responses to climate and resource changes.
- Underlines challenges common to monitoring programs: maintaining data quality, ensuring data accessibility and interoperability, and choosing appropriate analytical approaches to synthesize diverse data types.