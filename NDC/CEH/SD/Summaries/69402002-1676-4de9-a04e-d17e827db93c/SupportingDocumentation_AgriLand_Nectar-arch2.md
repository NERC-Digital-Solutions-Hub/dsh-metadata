# Nectar sugar values of common British plant species [AgriLand]

## Overview
- A dataset of nectar sugar values from common British plant species, collected during 2011–2012 and compiled in 2015.
- Intended for monitoring environmental resources and pollinator-supporting nectar availability; supports cross-site/time comparisons and policy-relevant analyses.
- Data are structured for standardised reporting and potential integration with other environmental datasets.

## Data structure and contents
- Spreadsheet 1: nectar per flower
  - File: AgriLand_Nectar_perflower.csv
  - 3303 observations, 175 species, 19 columns
  - Key fields: species, location, habitat, bagging, rinsing, collection dates/times, temperature/humidity, flower/plant identifiers, flower age/sex, sugar per flower per 24h (µg), and max potential sugar per flower (sugarmax, µg/flower/24h).
- Spreadsheet 2 (referred to as Spreadsheet 3 in text): nectar per species
  - File: AgriLand_Nectar_perspecies.csv
  - 270 species, 15 columns
  - Key fields: mean/variance/n (sample size) of nectar sugar per flower per species; empirical and modelled nectar productivity per hectare per year; final nectar productivity value; origin (empirical, modelled, or default).
- Data responsibility and provenance
  - Data collected 2011/2012; dataset created in 2015.
  - Project: UK IPI AgriLand grant BB/H014934/1.
  - Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott (contact details provided).

## Experimental design and sampling
- Field surveys conducted February–October 2011–2012, mainly in southern England (e.g., Bristol area).
- Species list: 270 plant species selected based on pollinator relevance and regional surveys; 220 target species plus 50 locally important species.
- Sampling regime per species:
  - On average, 10 bagged flowers from at least 5 distinct individuals per population.
  - Up to 2 populations per species when possible.
  - Total per species: median 20 flowers (range 5–30).
- Field methods:
  - 24-hour bagging of flowers with bridal mesh to allow nectar replenishment and reduce insect visitation.
  - In some cases, nectar collected from unbagged flowers to capture standing crop.
  - Sampling window 0900–1600 hours.

## Collection, transformation, and outputs
- Nectar measurement (per flower per 24h):
  - Nectar volume collected with glass microcapillaries; sugar concentration measured with a refractometer.
  - Calculation for nectar sugar per flower per 24h (s): s = 10 × d × v, where v = volume (µL) and d = density of sucrose solution at concentration C (derived from C with a provided formula).
  - Where rinsing was used, nectar sugar content estimated from diluted nectar volumes and concentrations after rinsing.
  - Bagged vs unbagged data distinguished; standing crop values from unbagged flowers not used in species-average calculations.
- Vegetative-scale productivity (kg/ha/year):
  - Empirical nectar productivity: based on nectar per flower × peak flower density × flowering days (using a triangular productivity function).
  - Modelled nectar productivity: derived from a linear model of log10(nectar productivity) as a function of plant traits (BiolFlor-based), back-transformed to produce annual productivity estimates.
  - Traits used in modelling: flower shape, breeding system, life span, dicliny, maximum height, flowering length, plant family.
- Data processing and outputs:
  - For each flower: compute s; for each population/species: compute mean, variance, and sample size of nectar sugar per flower per day.
  - Outputs include empirical nectar productivity (kg/ha/year), modelled nectar productivity (kg/ha/year), and a final nectar productivity value by priority (empirical > modelled > default/zero).

## Quality control and data interpretation
- sugarmax (µg) indicates potential maximum sugar per flower if all possible nectar is recollected.
- Unbagged flowers represent standing crop nectar values and were not used in calculating species-wide averages.
- Documentation notes ensure transparency on methods and transformations and provide references for methodology.

## Analytical relevance and data use
- Enables monitoring of nectar resource changes over time and space to assess pollinator resources and ecosystem health.
- Data can be combined with other environmental datasets (e.g., plant density, floral traits) to enrich analyses and policy evaluations.
- Provides standardized metrics (flower-level and species-level) and modelled estimates to support scenario analyses and cross-study comparisons.

## References and methodological notes
- Baude et al. 2015 (methods and supplementary details cited).
- Foundational references for nectar calculation and BiolFlor trait data.