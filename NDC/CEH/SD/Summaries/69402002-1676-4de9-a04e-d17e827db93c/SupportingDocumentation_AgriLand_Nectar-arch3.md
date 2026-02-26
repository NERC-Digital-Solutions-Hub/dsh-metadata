# Nectar sugar values of common British plant species [AgriLand]

- Purpose: Provides measured and modelled nectar sugar values to inform monitoring of nectar resources for pollinators and support policy decisions on environmental health and biodiversity.

- Datasets and structure:
  - Spreadsheet 1: AgriLand_Nectar_perflower.csv (per flower; 3303 observations; 175 species; 19 columns)
  - Spreadsheet 2: AgriLand_Nectar_perspecies.csv (per species; 270 species; 15 columns)
  - Key per-flower variables include: species, location, habitat, flower/plant identifiers, bagging and rinsing status, sampling dates/times, weather (temp, humidity), flower age/sex, and sugar content per flower (µg/flower/24h) plus the potential maximum (sugarmax).
  - Key per-species variables include: mean/variance/ n of nectar sugar per flower, potential max nectar content, empirical and modelled nectar productivity (kg/ha/yr), and origin (empirical, modelled, or default).

- Experimental design and sampling regime:
  - Field surveys conducted Feb–Oct 2011–2012, mainly in southern England (e.g., Bristol area).
  - For each species: 1–2 populations in 1–2 locations; most species observed in 20 flowers (median) with 5–30 flowers sampled; 2 populations per species when possible.
  - Species list derived from countryside vegetation data; 270 survey species plus 50 locally important species.

- Collection and measurement methods:
  - Nectar sampling to prevent insect depletion: bagged flowers (20–24 hours) or unbagged for standing crops; flowers bagged with bridal mesh prior to sampling.
  - Nectar collected with glass microcapillaries (1, 5, 10 µL); timing 09:00–16:00.
  - Nectar sugar concentration measured with a handheld refractometer; sugar content per flower calculated as s = 10 × d × v, where v is volume and d is solution density calculated from C with a provided formula.
  - For low nectar volumes, rinsing with distilled water (1–5 µL per rinse) was performed; diluted nectar re-collected to estimate sugar content.
  - Measurements also include water density equations and methods to convert to µg sugar per flower per 24 h.

- Scaling to landscape scale and modelling:
  - Nectar per flower scaled to kg/ha/year based on flower density and flowering duration, using a triangular function of nectar productivity across the flowering period.
  - Modelled nectar productivity derived from a linear model (log10(x+1) transformed) using plant traits (from BiolFlor): flower shape, breeding system, life span, dicliny, height, flowering length, and family; back-transformed to provide annual nectar productivity (kg/ha/yr).
  - For unsurveyed species, traits-based predictions are used to estimate productivity; final values combine empirical, modelled, and default values by priority.

- Quality control and data governance:
  - sugarmax refers to the potential maximum nectar sugar if all added water is recollected.
  - Unbagged nectar values represent standing crop (not used for average nectar per species); bagged values used for per-flower averages.
  - Clear documentation of data provenance (empirical, modelled, or default) and metadata to support verification.

- Data provenance and references:
  - Data responsibility: Mathilde Baude, Bill Kunin, Jane Memmott; UK IPI AgriLand grant BB/H014934/1.
  - Data collection: 2011–2012; Dataset creation: 2015.
  - References include Baude et al. (2015), methodological sources on nectar calculation and BiolFlor traits database, and related Countryside Survey materials.

- Practical implications for monitoring frameworks:
  - Enables monitoring of nectar resource availability for pollinators at both flower and species levels.
  - Provides transparency on measurement methods, scaling assumptions, and data origins (empirical vs modelled), aiding governance and data-sharing decisions.
  - Supports integration with broader nectar resource datasets (e.g., AgriLand) to inform habitat restoration, pollinator support strategies, and policy evaluation.