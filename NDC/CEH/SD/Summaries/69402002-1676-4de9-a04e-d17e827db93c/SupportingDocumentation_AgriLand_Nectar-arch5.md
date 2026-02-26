# Nectar sugar values of common British plant species [AgriLand]

## Overview
- Dataset name and description: Nectar sugar values of common British species (AgriLand)
- Data format: CSV with two spreadsheets
- Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott
  - Emails: mathilde.baude@univ-orleans.fr, W.E.Kunin@leeds.ac.uk, jane.memmott@univ-bristol.ac.uk
- Project name: UK IPI AgriLand grant BB/H014934/1
- Data collection period: 2011–2012
- Dataset creation: 2015
- Purpose and scope: Provides empirical nectar sugar measurements at the flower scale and modeled/empirical nectar productivity at the vegetative scale for common British plant species to support pollinator resources research
- Relevance for discovery and reuse: Comprehensive metadata and experimental design details to support data governance, quality checks, and reuse in related studies

## Data structure and metadata

- Spreadsheet 1: nectar per flower
  - File: AgriLand_Nectar_perflower.csv
  - Contents: 3303 observations across 175 species and 19 columns
  - Key columns (examples): species, location, habitat, id (year/species/location/bagging/flower number), bagging, rinsing, bagging.date/hour, collection.date/hour, year, temp, hum, plant.no, flower.no, flower.age, flower.sex, sugar in µg/flower/24h, sugarmax in µg/flower/24h
- Spreadsheet 2: nectar per species
  - File: AgriLand_Nectar_perspecies.csv
  - Contents: 270 species across 15 columns
  - Key columns (examples): species, mean.nectar.sugar.content.per.flower, var.nectar.sugar.content.per.flower, n.nectar.sugar.content.per.flower, mean.potential.max.nectar.sugar.content.per.flower, var.potential.max.nectar.content.per.flower, n.potential.max.nectar.sugar.content.per.flower, empirical.nectar.productivity.value, modelled.nectar.productivity.value, final.nectar.productivity.value, origin.of.values

Note: The document lists two spreadsheets for per-flower data and per-species data; the second spreadsheet includes both empirical and modelled productivity metrics and an origin indicator for values.

## Experimental design and sampling

- Field surveys conducted 2011–2012 (February to October), mainly in southern England (e.g., Bristol region)
- Populations and species
  - For each species, 1–2 field populations in 1–2 locations
  - Exceptions: three species (Caltha palustris, Lamium purpureum, Sinapis arvensis) had half nectar sampled from pot-grown plants due to field scarcity; Viola arvensis also sourced from pot-grown plants
- Sampling regime
  - Approximately 10 bagged flowers per population
  - 2 populations per species when possible
  - Total per species: median ~20 flowers; range 5–30
- Species list
  - Initial list of 270 species derived from Countryside Survey 2007 (Carey et al. 2008): 220 pollinator-rewarding species plus 50 locally important species

## Collection, generation, and transformation methods

- Flower-scale nectar (µg/flower/24h)
  - Bagging: flowers bagged 24 hours before sampling to prevent insect depletion
  - Additional unbagged samples collected for standing crop in some species
  - Collection: 0900–1600 hours using glass microcapillaries
  - Sampling: about ten flowers from at least five individuals per population
  - Measurement: nectar sugar concentration via refractometer; sugar content calculated with s = 10 × d × v × C, where v is volume, d is density of sucrose solution (density formula provided), and C is concentration
  - Rinsing: for low-volume nectar, flowers rinsed twice with distilled water (1–5 µL per rinse) and diluted nectar re-collected
  - Notes: sugarmax values reflect potential maximum nectar sugar if all rinsed water could be recollected
- Vegetative scale nectar (kg/ha/year)
  - Empirical nectar sugar content per unit vegetative cover scaled to kg/ha/year
  - Scaling factors: nectar per flower (24h) × peak flower density × number of flowering days (divided by 2)
  - Triangular function assumption across the flowering period (referenced AgriLand_flowerdensity dataset and Baude et al. 2015 supplementary methods)
  - Modelled productivity: linear model of log10(x+1)-transformed annual nectar sugar productivity as a function of plant traits (e.g., flower shape, breeding system, life span, dicliny, maximum height, flowering length, family) using BiolFlor-derived traits; back-transformed to obtain predicted values
  - Final per-species nectar productivity: prioritized as empirical, modelled, or default values with explicit origin recorded

## Analytical methods

- Core calculation: s = 10 × d × v × C for nectar sugar per flower per 24h
  - v: measured nectar volume (µL)
  - d: density of sucrose solution based on concentration C
  - C: sugar concentration (percent)
- Data aggregation
  - Mean, variance, and sample size computed for nectar sugar content per species (µg/flower/24h)
  - Per-species potential maximum nectar sugar content and associated statistics calculated under rinsing assumptions
- Data provenance and transformation
  - Raw flower-scale data underpin per-species summaries and modelled productivity estimates
  - Modelled values rely on trait-based linear modelling with back-transformation

## Quality control and caveats

- Quality control notes
  - sugarmax.µg provides a potential maximum nectar sugar estimate under recollection assumptions
  - Unbagged flowers reflect standing crop with pollinator visitation and were not used for average nectar-per-species calculation
- Data provenance and limitations
  - Data include both empirical measurements and modelled estimates; origin is recorded per value
  - Some species required pot-grown plant data due to field limitations; users should consider source differences when aggregating

## Data availability, governance, and provenance

- Data responsibility and contact points provided for governance and archiving
- Metadata-rich design supports discoverability, provenance tracking, and replication
- Publication and methods references included to facilitate validation and reuse

## References

- Baude et al. 2015. Britain in bloom: national-scale changes in nectar resources for pollinators in revision
- Bolten A. B., Feinsinger P., Baker H. G. & Baker I. (1979). On the calculation of sugar concentration in flower nectar. Oecologia 41:301-304
- Carey, P.D.; Wallis, S.; Emmett, B.A.; Maskell, L.C.; Murphy, J.; Norton, L.R.; Simpson, I.C.; Smart, S.M. 2008. Countryside Survey: UK Headline Messages from 2007. CEH
- Corbet S. A., et al. (2001). Native or exotic? Double or single? Evaluating plants for pollinator-friendly gardens. Annals of Botany 87(2):219
- Klotz S., Kühn I. & Durka W. (2002). BIOLFLOR - Eine Datenbank zu biologisch-ökologischen Merkmalen der Gefäßpflanzen in Deutschland
- Prys-Jones O. E. & Corbet S. A. (1991). Bumblebees (pp. 1-92). The Richmond Publishing Co. Ltd.