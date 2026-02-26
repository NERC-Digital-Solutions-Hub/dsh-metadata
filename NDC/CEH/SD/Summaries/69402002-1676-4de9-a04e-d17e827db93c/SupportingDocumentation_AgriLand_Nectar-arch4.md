# Nectar sugar values of common British plant species [AgriLand]

- Dataset name and scope: Nectar sugar values for common British plant species collected under the AgriLand project; two CSV spreadsheets describing nectar at the flower level and nectar at the species level.
- Data owners and project: Responsible investigators Mathilde Baude, Bill Kunin, and Jane Memmott; UK IPI AgriLand grant BB/H014934/1; dataset created 2015 from 2011–2012 field data.
- Data format: CSV files (AgriLand_Nectar_perflower.csv and AgriLand_Nectar_perspecies.csv).

## Data structure

- Spreadsheet 1 (per flower): AgriLand_Nectar_perflower.csv
  - Contents: 3303 observations, 175 species, 19 columns
  - Key fields (examples):
    - species, location, habitat
    - id (year, species, location, bagging, flower number)
    - bagging (bagged or unbagged), rinsing (yes/no)
    - bagging.date/hour, collection.date/hour
    - year, temp, hum
    - plant.no, flower.no, flower.age, flower.sex
    - sugar (µg/flower/24h), sugarmax (µg/flower/24h)
- Spreadsheet 3 (per species): AgriLand_Nectar_perspecies.csv
  - Contents: 270 species, 15 columns
  - Key fields (examples):
    - species
    - mean.nectar.sugar.content.per.flower (µg/flower/day)
    - var.nectar.sugar.content.per.flower
    - n.nectar.sugar.content.per.flower
    - mean.potential.max.nectar.sugar.content.per.flower
    - var.potential.max.nectar.sugar.content.per.flower
    - n.potential.max.nectar.sugar.content.per.flower
    - empirical.nectar.productivity.value (kg/ha/year)
    - modelled.nectar.produc tivity.value (kg/ha/year)
    - final.nectar.productivity.value
    - origin.of.values (empirical/modelled/default)

## Nature and units of recorded values

- Nectar per flower (perflower.csv)
  - s (µg/flower/24h): sugar produced per flower in 24h
  - v (µL): volume of nectar collected
  - d: density of sucrose solution at concentration C
  - C: sugar concentration (%)
  - Calculations: s = 10 × d × v × C; density formula and references provided
  - Additional notes: includes both bagged (replenished nectar) and unbagged (standing crop) samples; some flowers rinsed prior to sampling
- Nectar per species (perspecies.csv)
  - Aggregated metrics: means, variances, and sample sizes for nectar per flower
  - Potentially scaled-up metrics: mean/potential max nectar content, empirical and modelled nectar productivity values (kg/ha/year)
  - Final values: final.nectar.productivity.value chosen by priority (empirical, modelled, or default)

## Experimental design and sampling regime

- Field surveys conducted February–October 2011–2012, mainly in southern England (Bristol area, etc.)
- Species coverage: 270 species selected from a pool of 270 (based on pollinator relevance and distribution)
- Sampling per species: 1–2 populations when possible; typically 10 bagged flowers from at least 5 individuals per population; median of ~20 flowers per species; range 5–30
- Population strategy: 1–2 populations per species; exceptions for three species where half nectar from pot-grown plants due to flowering limits
- Species list basis: UK Countryside Survey 2007 data plus locally important pollinator species added

## Collection and processing methods

- Nectar collection (flower scale)
  - Bagging: flowers bagged 24 hours prior to sampling to allow nectaries to replenish; some samples from unbagged flowers for standing crop
  - Collection: glass microcapillaries (1, 5, 10 µL) pressed into nectaries; hours of collection 09:00–16:00
  - Measurement: sugar concentration measured with a handheld refractometer; nectar sugar content per flower calculated via s = 10 × d × v × C
  - Rinsing: some flowers rinsed with ~1–5 µL distilled water when nectar volumes were too low; rinsed nectar used to estimate diluted sugar content
- Nectar at vegetative scale
  - Conversion: empirical nectar sugar content per unit vegetative cover (kg/ha/year) scaled by peak flowering density and number of flowering days, assuming a triangular productivity function
  - Modelled productivity: linear model using plant traits (from BiolFlor: flower shape, breeding system, life span, dicliny, height, flowering length, family) to predict annual nectar productivity; back-transformed to kg/ha/year
  - Backing data: AgriLand_flowerdensity dataset and methods in Baude et al. 2015

## Analytical methods and calculations

- Per flower: s = 10 × d × v × C; density d derived from C using the provided formula
- Aggregation: compute mean, variance, and sample size for nectar per species from flowers of the same species
- Productivity values: empirical (from data), modelled (traits-based), or default; final productivity value chosen by priority

## Quality control and data interpretation

- sugarmax.µg: potential maximum nectar sugar assuming complete recollection of all added water
- unbagged: standing crop values (not used for computing species averages)
- Clear documentation of data provenance, measurement methods, and limitations
- Data quality notes emphasize potential biases due to bagging status, rinsing, and sampling times

## Data provenance, access, and references

- Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott
  - Contact emails provided for data inquiries
- References for methods and context
  - Baude et al. 2015 (Britain in bloom; nectar resources)
  - Bolten et al. 1979; Prys-Jones & Corbet 1991; Corbet et al. 2001 (methods for nectar concentration and sampling)
  - Carey et al. 2008 (UK Countryside Survey)
  - BiolFlor database (plant traits)
- Note on usage: dataset provides both empirical measurements and modelled estimates of nectar productivity; data suitable for pollinator resource assessments and cross-species comparisons within the AgriLand framework

## Practical implications for data leadership and reuse

- Clear, well-structured data with per-flower and per-species views supports end-to-end data products and policy-friendly outputs
- Metadata includes units, sampling methodology, and quality flags (e.g., bagging, rinsing, standing crop)
- Useful for assessing nectar resources across species and landscapes, and for integrating with plant-trait and flowering-density datasets
- Considerations for future use: data access processes, potential updates, standardization across datasets, and alignment with sector-wide data-sharing practices to reduce fragmentation and barriers to data discovery
- Governance and stewardship: explicit data responsibilities and references enable tracking provenance and ensuring ongoing stewardship and updates