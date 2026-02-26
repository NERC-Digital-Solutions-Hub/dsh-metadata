# Dataset information

## Overview
- Data name: Nectar sugar values of common British plant species [AgriLand]
- Description: Nectar sugar values of common British species
- Format: CSV (two spreadsheets)
- Responsibility: Mathilde Baude, Bill Kunin, Jane Memmott
- Project: UK IPI AgriLand grant BB/H014934/1
- Data collection: 2011–2012
- Dataset creation: 2015

## Data structure

- Spreadsheet 1: nectar per flower
  - File: AgriLand_Nectar_perflower.csv
  - 3303 observations, 175 species, 19 columns
  - Key fields (examples): species, location, habitat, id, bagging, rinsing, bagging.date, bagging.hour, collection.date, collection.hour, year, temp, hum, plant.no, flower.no, flower.age, flower.sex, sugar in µg/flower/24h, sugarmax in µg/flower/24h

- Spreadsheet 2: nectar per species
  - File: AgriLand_Nectar_perspecies.csv
  - 270 species, 15 columns
  - Key fields (examples): species, mean.nectar.sugar.content.per.flower, var.nectar.sugar.content.per.flower, n.nectar.sugar.content.per.flower, mean.potential.max.nectar.content.per.flower, var.potential.max.nectar.content.per.flower, n.potential.max.nectar.content.per.flower, empirical.nectar.productivity.value, log10(value+1)modelled.nectar.productivity, log10(95%lwr+1)modelled.nectar.productivity, log10(95%upr+1)modelled.nectar.productivity, modelled.nectar.productivity.value, nectar.productivity.default.value, final.nectar.productivity.value, origin.of.values

## Units and measurement details

- Nectar per flower (Spreadsheet 1)
  - s (µg of sugars per flower per 24h)
  - v (volume of nectar in µL)
  - d (density of sucrose solution at concentration C)
  - C (sucrose concentration, %)
  - Equations: s = 10 * v * d * C; d = 0.0037921*C + 0.0000178*C^2 + 0.9988603
  - Measurements: bagged (24h to exclude insect visitors) or unbagged; rinsing performed when necessary
  - Columns include: bagging.date, bagging.hour, collection.date, collection.hour, temp, hum, etc.

- Nectar per species (Spreadsheet 2)
  - Aggregated metrics: mean, variance, and sample size of nectar sugar content per flower (µg/flower/24h)
  - Productivity metrics: empirical and modelled nectar productivity in kg of sugars/ha/year
  - Final values: final.nectar.productivity.value; origin of values (empirical, modelled, or default)

## Experimental design and sampling

- Field surveys conducted Feb–Oct 2011–2012, mainly in southern England
- For each species: 1–2 field populations across 1–2 locations
- Special cases: for Caltha palustris, Lamium purpureum, Sinapis arvensis, half nectar collected from field; Viola arvensis from pot-grown plants
- Species list: 270 plant species selected for pollinator relevance (from Countryside Survey 2007 plus locally important extras)
- Sampling regime per population: on average 10 bagged flowers from at least 5 distinct individuals
- Total per species: median 20 flowers, range 5–30 flowers

## Collection and processing methods

- Nectar at flower scale (µg/flower/24h)
  - Flowers bagged 24 hours prior to sampling to replenish nectar
  - Nectar collected with glass microcapillaries (1, 5, 10 µL)
  - For each population: about 10 flowers from at least 5 individuals
  - Nectar volume v used in calculations; sugar concentration C measured with refractometer
  - Rinsing: some species rinsed with distilled water; nectar sugar content estimated from diluted nectar
- Nectar at vegetative scale (kg/ha/year)
  - Empirical nectar content scaled by peak flowering density and flowering days
  - Assumes a triangular flowering productivity function
  - Data linked with AgriLand_flowerdensity and related methods

## Analytical methods

- Per-flower sugar production (s) calculation: s = 10 * v * d * C
- d (density) calculated from C using the specified polynomial equation
- For multiple samplings from the same flower, sugar is summed across samplings to obtain per-flower 24h value
- Species-level summaries: mean, variance, and sample size for µg/flower/24h
- Per-species productivity values include empirical, modelled (traits-based), and default options

## Quality control and data caveats

- sugarmax.µg: potential maximum nectar sugar assuming full recollection
- unbagged flowers: standing crop values not used for species averages
- Data provenance noted: empirical measurements, model-based estimates, and default values; origin indicated in final field
- References provided for methods and trait sources

## Data provenance and references

- Baude et al. 2015 (related methods and datasets)
- Bolten et al. 1979; Prys-Jones & Corbet 1991; Corbet et al. 2001 (density and nectar calculations)
- Carey et al. 2008 (Countryside Survey reference)
- BiolFlor database (plant traits)
- Additional methodological details in supplementary materials of Baude et al. 2015

## GIS-specific considerations

- Useful for spatial mapping of nectar resources by species and by site
- Relevant fields for GIS: species, location, habitat, year, collection date/time, temperature/humidity, and per-flower/per-species productivity values
- Data integration potential: join with AgriLand or related vegetation datasets to model pollinator resource landscapes
- Key challenges: multiple data sources, variable resolutions, missing data, and the need for standardization and cleaning before GIS analysis
- Suitable outputs: per-flower nectar maps, species-level productivity maps, and regional nectar resource assessments over time