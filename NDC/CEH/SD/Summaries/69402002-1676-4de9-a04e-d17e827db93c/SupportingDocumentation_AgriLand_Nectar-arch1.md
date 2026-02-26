# Nectar sugar values of common British plant species [AgriLand]

- Overview
  - A dataset describing nectar sugar values for common British plant species, compiled under the UK IPI AgriLand project.
  - Contains two CSV spreadsheets with field-collected nectar data and modelled estimates to support analysis of nectar resources for pollinators.
  - Data collectors and curators: Mathilde Baude, Bill Kunin, and Jane Memmott.

- Datasets and structure
  - Spreadsheet 1: nectar per flower (AgriLand_Nectar_perflower.csv)
    - Contents: 3303 observations across 175 species and 19 columns.
    - Key columns include: species, location, habitat, id (year, species, location, bagging, flower number), bagging (bagged or unbagged), rinsing, bagging.date/hour, collection.date/hour, year, temp, hum, plant.no, flower.no, flower.age, flower.sex, sugar in µg/flower/24h, sugarmax in µg/flower/24h.
  - Spreadsheet 3: nectar per species (AgriLand_Nectar_perspecies.csv)
    - Contents: 270 species across 15 columns.
    - Key columns include: species, mean.nectar.sugar.content.per.flower (µg/flower/day), var.nectar.sugar.content.per.flower, n.nectar.sugar.content.per.flower, mean.potential.max.nectar.sugar.content.per.flower, var.potential.max.nectar.sugar.content.per.flower, n.potential.max.nectar.sugar.content.per.flower, empirical.nectar.produc tivity.value (kg/ha/yr), modelled.nectar.productivity.value, final.nectar.productivity.value, origin.of.values (empirical/modelled/default).
  - Note: The dataset also references additional related datasets (e.g., AgriLand_flowerdensity) used for scaling nectar productivity to vegetation-scale metrics.

- Experimental design and sampling regime
  - Field surveys conducted February–October in 2011 and 2012, mainly in southern England (e.g., Bristol area).
  - Species coverage: 270 species selected from a broader UK flora list (270 species across 220 potential pollinator-rewarding species, plus 50 locally important species).
  - Population sampling: one to two field populations per species, in one to two locations; some species collected from pot-grown plants due to limited field populations.
  - Sampling per species: on average 10 bagged flowers from at least 5 distinct individuals per population; two populations per species when possible; median total flowers per species ~20 (range 5–30).

- Collection and data generation methods
  - Nectar at the flower scale (µg/flower/24h)
    - Bagging: flowers bagged with bridal mesh 24 hours prior to sampling to prevent insect visitation and allow nectar replenishment.
    - Nectar collection: both bagged (to measure replenished nectar) and unbagged flowers (standing crop) sampled between 0900–1600 h using glass microcapillaries (1, 5, 10 µL).
    - Measurement: nectar volume per flower derived from the length of liquid in the capillary; sugar concentration measured with a refractometer.
    - Calculation: sugar per flower per 24 h (s) calculated as s = 10 × d × v × C, where v is volume (µL), C is sugar concentration (%), and d is density of a sucrose solution given by d = 0.0037921C + 0.0000178C² + 0.9988603.
    - Rinsing: for many species, nectar required rinsing with 1–5 µL distilled water prior to sampling; diluted nectar re-collected to estimate total sugars.
    - Notes: unbagged flowers (standing crop) were not used for calculating species-average nectar values.
  - Nectar at the vegetative scale (kg/ha/year)
    - Empirical nectar sugar content per unit vegetative cover (kg/ha/year) scaled from per-flower data using peak flowering density and flowering days, assuming a triangular productivity function across the flowering period (reference to AgriLand_flowerdensity and Baude et al. 2015 supplementary methods).
  - Modelled nectar productivity (kg/ha/year)
    - Based on a linear model of annual nectar sugar productivity (log10(x+1) transformed) as a function of plant traits.
    - Plant traits drawn from BiolFlor (e.g., flower shape, breeding system, life span, dicliny, maximum height, flowering length, family).
    - Most parsimonious model (selected by AIC) used to back-transform predictions for the initial species list and unsurveyed species.

- Analytical methods and data derivation
  - Flower-level sugar calculation: s = 10 × d × v × C; density d derived from C with the empirical equation above.
  - Nectar per flower: calculated from individual samplings of flowers from the same species; mean, variance, and sample size computed per species for µg/flower/24h.
  - Species-level nectar productivity: two pathways
    - Empirical: mean nectar sugar content per flower (µg/flower/day) scaled to annual productivity using flowering density and number of flowering days.
    - Modelled: linear-modelled annual nectar productivity (kg/ha/year) based on plant traits, back-transformed to original scale.
  - Final nectar productivity value: priority order of empirical, then modelled, then default values; final values are reported as kg of sugars/ha/year.
  - Quality control and data notes
    - sugarmax.µg: potential maximum nectar sugar if all water added during rinsing could be recollected.
    - Unbagged flower nectar values reflect standing crops with pollinator visitation; these values not used for computing species-average nectar per species.
  - Data provenance and references
    - Primary reference: Baude et al. 2015 (Britain in bloom: national-scale changes in nectar resources for pollinators).
    - Supporting methodological references for nectar calculation and plant trait data (e.g., Bolten et al. 1979; Prys-Jones & Corbet 1991; Corbet et al. 2001; BiolFlor database).

- Key notes for analysts
  - The dataset enables correlational and predictive analyses of nectar resources across British plant species, suitable for linking plant traits, phenology, and nectar availability to pollinator resources.
  - It provides both flower-level and species-level metrics, including empirical and modelled nectar productivity at the landscape scale (kg/ha/year).
  - Consider scale and method caveats when integrating with other datasets:
    - Bagging and rinsing affect nectar measurements; standing-crop values differ from replenished nectar.
    - The vegetative-scale productivity relies on triangular flowering curves and density data from auxiliary datasets.
    - Modelled productivity depends on trait data quality and the chosen linear model; note the provenance of trait data (BiolFlor) and potential trait gaps.
  - Data accessibility and provenance
    - Data curators and contact points listed for verification and reuse.
    - Created 2015 from field data collected 2011–2012; intended for broad ecological analyses and pollinator resource assessments.