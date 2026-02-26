# Nectar sugar values of common British plant species [AgriLand]

## Overview
- Dataset from field surveys (2011–2012) in southern England documenting nectar sugar content for common British plant species.
- Two CSV sheets: per-flower nectar measurements and per-species nectar productivity estimates.
- Includes empirical nectar data and modelled productivity values, with derived metrics for potential maximum nectar and standing crop.
- Data custodians: Mathilde Baude, Bill Kunin, Jane Memmott; project linked to UK IPI AgriLand grant BB/H014934/1; dataset created in 2015.

## Data structure and formats
- Spreadsheet 1: nectar per flower (Agr iLand_Nectar_perflower.csv)
  - 3303 observations, 175 species, 19 columns
  - Key fields (examples): species, location, habitat, id, bagging, rinsing, bagging.date, bagging.hour, collection.date, collection.hour, year, temp, hum, plant.no, flower.no, flower.age, flower.sex, sugar in µg/flower/24h, sugarmax in µg/flower/24h
- Spreadsheet 2: nectar per species (AgriLand_Nectar_perspecies.csv)
  - 270 species, 15 columns
  - Key fields (examples): species, mean.nectar.sugar.content.per.flower (µg/flower/day), var.nectar.sugar.content.per.flower, n.nectar.sugar.content.per.flower, mean.potential.max.nectar.sugar.content.per.flower, var.potential.max.nectar.sugar.content.per.flower, n.potential.max.nectar.sugar.content.per.flower, empirical.nectar.productivity.value (kg/ha/year), modelled.nectar.produc tivity.value, final.nectar.productivity.value, origin.of.values (empirical/modelled/default)

## Experimental design and sampling
- Field surveys conducted February–October 2011–2012; majority sites in southern England.
- Species list started with 270 species (from Countryside Survey 2007) and expanded with 50 locally important species; 270 total surveyed.
- For each species: one or two field populations in one or two locations; special cases for three species where pot-grown plants were used due to limited field populations.
- Sampling regime: on average 10 bagged flowers per population; 2 populations per species when possible; median ~20 flowers per species (range 5–30); dataset indicates per-species sample sizes.

## Collection, generation, and transformation methods
- Nectar measurement at the flower scale (µg/flower/day)
  - Flowers bagged 24 hours prior to sampling to prevent insect visitation; standing crop also measured for some unbagged flowers.
  - Nectar collected using glass microcapillaries (1, 5, 10 µL) between 0900–1600 hours.
  - Sugar concentration measured with a handheld refractometer.
  - Sugar per flower calculated as s = 10 × v × C, with density d(C) = 0.0037921C + 0.0000178C² + 0.9988603.
  - For rinsed samples, flowers were rinsed with distilled water; diluted nectar volumes used to estimate sugar content.
- Nectar at the vegetative scale (kg/ha/year)
  - Empirical nectar sugar content per unit vegetative cover scaled to kg/ha/year by multiplying per-flower sugar content, peak flower density, and flowering days (assuming a triangular productivity function across the flowering period).
  - Modelled nectar productivity estimated from linear models (log10(x+1) transformed) using plant traits (from BiolFlor): flower shape, breeding system, life span, dicliny, maximum height, flowering length, family.
  - Back-transformation used to predict annual nectar productivity (kg/ha/year) for surveyed and unsurveyed species; final values combine empirical, modelled, and default values.

## Analytical methods and data processing
- Per-flower nectar: s = 10 × v × C, with d(C) used to obtain density; nectar per flower is the sum of successive samplings from the same flower.
- Per-species statistics: compute mean, variance, and sample size for nectar sugar content per flower (µg/flower/24h).
- Productivity values:
  - Empirical nectar productivity (kg/ha/year) derived from measured data.
  - Modelled nectar productivity derived from trait-based linear modelling; back-transformed to original scale.
  - Final nectar productivity value for each species chosen by priority: empirical > modelled > default.
- Derived fields include origin.of.values to indicate whether a value is empirical, modelled, or default.

## Quality control and data notes
- sugarmax.µg: potential maximum nectar sugar, assuming all added water is recollected.
- Unbagged flowers provide standing crop values; these were not used to calculate species-average nectar per species.
- Notes on dataset scope: includes both bagged (24h) and standing-crop nectar; some species required rinsing due to very low nectar volumes.
- Important context for use: per-flower data can be aggregated to per-species estimates; modelled productivity depends on plant traits and may be used where empirical data are sparse.

## Potential uses and data integration
- Build data products and dashboards showing nectar resources by species, location, and time.
- Combine with pollinator abundance datasets or flowering density data (e.g., AgriLand_flowerdensity) to model pollinator resource availability across landscapes.
- Compare empirical nectar availability with trait-based model predictions to study drivers of nectar production.
- Use final, origin-labeled values to assess reliability and choose appropriate data sources for analyses.

## Provenance and contacts
- Data collection: 2011–2012; mostly in southern England.
- Dataset creation: 2015.
- Data providers: Mathilde Baude, Bill Kunin, Jane Memmott.
- Project: UK IPI AgriLand grant BB/H014934/1.

## References
- Baude et al. 2015 (Britain in bloom: national-scale changes in nectar resources for pollinators; methods and supplementary methods referenced)
- Bolten et al. 1979; Prys-Jones & Corbet 1991; Corbet et al. 2001 (methods for calculating nectar density and sampling considerations)
- Carey et al. 2008 (Countryside Survey: UK results)