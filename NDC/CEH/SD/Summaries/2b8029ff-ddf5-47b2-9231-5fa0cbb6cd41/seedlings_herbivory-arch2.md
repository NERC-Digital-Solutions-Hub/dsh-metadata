# Amazon Fertilization Experiment (AFEX)

## Study area and context
- Location: Biological Dynamics of Forest Fragments Project (BDFFP) KM41 reserve, ~100 km from Manaus (02 24'S, 59 52'W).
- Environment: humid/wet climate; mean temperature ~26.7°C; annual rainfall ~2200 mm; dry season July–Sept; rain peak March–April.
- Vegetation/Soils: dense Terra Firme rainforest; canopy 30–37 m (emergents up to 55 m); soils are clayey red-yellow pods and yellow latosols, highly weathered, acidic, low fertility; WRB ferrasols.
- Purpose: AFEX is a full factorial fertilization experiment conducted within the BDFFP area.

## AFEX experimental design
- Start: March 2017.
- Design: full factorial with seven treatments plus control, four replicates per treatment (32 plots total), arranged in four independent blocks at least 250 m apart.
- Treatments (N, P, CATIONS) and combinations: Control; N; P; CATIONS; N+P; N+CATIONS; P+CATIONS; N+P+CATIONS.
- Plot layout: each plot 50 x 50 m; minimum 100 m separation between plots; all plots in areas with similar soil, vegetation, and topography.
- Fertilization: annual applications divided into three events to reduce leaching and runoff; fertilizers spread by hand during a systematic walk within plots.

## Seedling sampling and herbivory data collection
- Subplot design: within each 50 x 50 m plot, four 1 x 1 m subplots inside a 30 x 30 m plot; 16 subplots per treatment, totaling 128 subplots.
- Seedling criteria: individuals >20 cm height and diameter at ground height (DGH) < 1 cm; palms and lianas excluded.
- Leaf marking and monitoring: for each seedling, mark the closest 10 mature leaves to the apical yolk and monitor bimonthly for 12 months (six campaigns; four in the rainy season, two in the dry season).
- Herbivory and damage metrics: leaf area loss by herbivory (percent) via direct visual estimation with a millimetre grid to improve accuracy; record presence/absence data for galls (GAIL), fungi (FUNGUS), and leaf miners; track leaf mortality.
- Data collection cadence: six campaigns over 12 months (bimonthly).

## Data and measurements
- Data file: seedlings_herbivory.csv with 27,510 rows and 14 columns.
- Columns:
  - CENSUS: Sampling number
  - MONTH: Month of sampling
  - DATE: Sampling day
  - TRT: Plot treatment
  - BLOCK: Block (1–4)
  - PLOT: Plot (1–8)
  - SUBPLOT: Subplot number (1–4)
  - INDIVIDUAL: Seedling tag
  - LEAF: Leaf tag
  - HERBIVORY: Leaf area loss (%)
  - GAIL: Gall presence (1/0)
  - FUNGUS: Fungus presence (1/0)
  - LEAF_MINERS: Leaf miners presence (1/0)
  - MORTALITY: Leaf death (1/0)

## References
- Chauvel, A. 1982; Os latossolos amarelos, álicos, argilosos...
- Comita, L. S., Condit, R., & Hubbell, S. P. 2007; Developmental changes in habitat associations...
- Johnson, M. T., Bertrand, J. A., & Turcotte, M. M. 2016; Precision and accuracy in quantifying herbivory
- Laurance, W. F. et al. 1999; Relationship between soils and Amazon forest biomass
- Lovejoy, T. E., & Bierregaard, R. O. 1990; Central Amazonian Forest...
- Quesada, C. A. et al. 2010, 2011; Soils of Amazonia; Variations in chemical and physical properties
- RADAMBRASIL. 1978; Levantamento de recursos naturais
- Ranzani, G. 1980; Identificação e caracterização de solos da INPA
- Additional related sources cited in the document

## Implications for environmental monitoring (Analysts’ perspective)
- Data support: Enables monitoring of fertilization effects on seedling herbivory and related biotic factors within a tropical rainforest setting.
- Standardization and QA: Uses standardized sampling and measurement procedures (e.g., grid-based herbivory assessment) across replicated plots and temporal campaigns.
- Data management: Data are stored in a structured CSV format with explicit metadata fields; outputs are intended to be stored and uploaded to appropriate data portals to facilitate reuse.
- Value and accessibility: Highlights the need to increase dataset value by integrating with additional data sources and ensuring access to underlying data for transparency and reuse.