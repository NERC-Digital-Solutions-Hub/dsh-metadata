# Seedlings herbivory

## Overview
- Study area within the Biological Dynamics of Forest Fragments Project (BDFFP) in the KM41 reserve, ~100 km from Manaus, Brazil.
- Humid, wet climate; mean temperature ~26.7°C; ~2200 mm annual precipitation; dry season July–Sept; rain peak March–April.
- Dense Terra Firme rainforest; canopy 30–37 m (emergents up to 55 m); red-yellow podzols and yellow latosols soils with high weathering, acidity, and low fertility (ferrasols).

## Amazon Fertilization Experiment (AFEX)
- Initiated March 2017; full factorial design with eight treatments: Control, N, P, CATIONS (K, Ca, Mg), N+P, N+CATIONS, P+CATIONS, N+P+CATIONS.
- 32 plots total, arranged in four independent blocks (≥250 m apart).
- Each plot is 50 x 50 m; blocks at least 100 m apart; fertilizers applied annually in three applications to mitigate leaching/runoff.
- Fertilizers: N (125 kg N ha⁻¹ yr⁻¹ as urea); P (50 kg P ha⁻¹ yr⁻¹ as triple superphosphate); K (50 kg K ha⁻¹ yr⁻¹ as KCl); Ca (160 kg Ca ha⁻¹ yr⁻¹ as dolomitic limestone); Mg (160 kg Mg ha⁻¹ yr⁻¹ as dolomitic limestone).

## Seedling sampling design
- Within each 50 x 50 m plot, four 1 x 1 m subplots are nested inside a 30 x 30 m area, yielding 16 subplots per treatment (128 total across all treatments).
- All plant individuals >20 cm height and with diameter at ground height <1 cm identified and tagged; palms and lianas excluded from sampling.
- For each individual, the closest 10 mature leaves to the apical yolk are marked and tracked bi-monthly to assess leaf-level herbivory.
- Herbivory measured as leaf area loss (percentage) following Johnson et al. 2016; leaves sectioned with a millimetre grid to improve accuracy.
- Additional data collected per leaf: gall presence, fungal presence, leaf miners, and leaf mortality (binary). Data collected bi-monthly for 12 months (six campaigns: four rainy season, two dry season).

## Data spreadsheet and structure
- Data file: seedlings_herbivory.csv
- Size: 27,510 rows and 14 columns
- Columns and meanings:
  - A CENSUS: Sampling number
  - B MONTH: Month of sampling
  - C DATE: Sampling date
  - D TRT: Plot treatment (see AFEX section)
  - E BLOCK: Block (1–4)
  - F PLOT: Plot (1–8) within the block
  - G SUBPLOT: Subplot number (1–4)
  - H INDIVIDUAL: Seedling individual tag
  - I LEAF: Leaf tag
  - J HERBIVORY: Leaf area loss due to herbivory, in %
  - K GAIL: Gall presence (1) or absence (0)
  - L FUNGUS: Fungus presence (1) or absence (0)
  - M LEAF_MINERS: Leaf miners presence (1) or absence (0)
  - N MORTALITY: Leaf death (1) or survival (0)

## Data use and potential applications
- Enables cross-treatment comparisons of herbivory and associated biotic factors (galls, fungi, leaf miners) across temporal seasons.
- Facilitates integration with environmental data (soil properties, climate variables) for broader analyses of fertilization effects on seedling herbivory dynamics.
- Supports the development of data products (dashboards, reports) to assist stakeholders in exploring herbivory patterns across treatments and time.