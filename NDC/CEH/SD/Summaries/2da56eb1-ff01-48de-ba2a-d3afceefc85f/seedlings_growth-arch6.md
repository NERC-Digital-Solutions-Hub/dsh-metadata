# Amazon Fertilization Experiment (AFEX)

- The study is conducted in the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, in a humid tropical forest with a dry season (Jul–Sep) and a rain peak in Mar–Apr.
- Climate and soils: mean temp about 26.7°C; annual rainfall ~2200 mm; soils are red-yellow podzols and yellow latosols with high weathering, acidity, and low fertility (ferralsols).
- Purpose: a full factorial fertilization experiment to assess how seedlings respond to nitrogen, phosphorus, and cations (K, Ca, Mg) under controlled nutrient additions.

## Study and Experimental Design

- Experiment start: March 2017.
- Treatments: seven fertilizer treatments plus a control, namely:
  - CONTROL
  - N
  - P
  - CATIONS
  - N+P
  - N+CATIONS
  - P+CATIONS
  - N+P+CATIONS
- Replication and layout: 32 plots total (4 replicates per treatment) arranged in four independent blocks, each at least 250 m apart.
- Plot configuration: each plot is 50 x 50 meters; fertilization is applied annually in three applications to reduce leaching and runoff, done by hand during systematic walks.
- Subplots and sampling framework: within each 50 x 50 m plot, four 1 x 1 m subplots inside a 30 x 30 m plot, yielding 16 subplots per treatment and 128 subplots overall.

## Seedling Sampling

- Target plants: seedlings taller than 20 cm with diameter at ground height (DGH) < 1 cm; palms and lianas are not identified or sampled.
- Measurements within each sub-plot:
  - Seedling height (ground level to apex)
  - DGH (mm)
  - Total leaves
  - Leaves with herbivory damage
  - Mortality (binary: 1 = dead, 0 = alive)
- tagging: each seedling assigned a unique INDIVIDUAL tag.
- Data collection schedule: bi-monthly over 12 months, totaling six replications per sub-plot (four in the rainy season, two in the dry season).

## Data Spreadsheet: seedlings_growth.csv

- Contents: 3,409 data rows and 13 columns.
- Columns and meanings:
  - CENSUS: sampling number
  - MONTH: sampling month
  - DATA: sampling day
  - TRT: plot treatment (refer to AFEX 2.1)
  - BLOCK: block number (1–4)
  - PLOT: plot number (1–8)
  - SUBPLOT: sub-plot number (1–4)
  - INDIVIDUAL: seedling tag
  - DGH: diameter at ground height (mm)
  - HEIGHT: height (cm)
  - TOTAL_LEAVES: total leaves
  - LEAVES_WITH_HERBIVORY: leaves with herbivory
  - MORTALITY: 1 = dead, 0 = alive

## Data Use and Potential Outputs

- End-user data products:
  - Growth trajectories and treatment effects by fertilizer regime
  - Mortality and herbivory patterns across treatments and seasons
  - Dashboards and pivotable summaries enabling self-service exploration
- Data integration opportunities:
  - Combine AFEX seedling data with soil properties, microclimate, and plot-level metadata to investigate drivers of growth responses
- Prototyping and dissemination:
  - Share early outputs/prototypes with stakeholders and gather feedback
  - Promote data reuse and advocate for ongoing data creation and more comprehensive metadata

## Data Quality, Documentation, and Access Considerations

- Ensure consistent ID schemes across CENSUS, TRT, BLOCK, PLOT, SUBPLOT, and INDIVIDUAL for reliable longitudinal analyses.
- Units and measurement protocols are specified (DGH in mm; HEIGHT in cm; herbivory and mortality data recorded).
- Temporal coverage spans both wet and dry seasons, enabling seasonality analyses; maintain clear dating (DATA) for each observation.
- Consider potential data gaps due to field conditions and maintain documentation to support data cleaning and integration with other BDFFP datasets.

## References

- Chauvel, A. 1982. Os latossolos amarelos, álicos, argilosos dentro dos ecossistemas das bacias experimentais do INPA e da região vizinha. Acta Amazonica 12(3): 38-47.
- Comita, L. S., Condit, R., & Hubbell, S. P. (2007). Developmental changes in habitat associations of tropical trees. Journal of Ecology, 95(3), 482-492.
- Laurance, W. F., et al. 1999. Relationship between soils and Amazon forest biomass: a landscape-scale study. Forest Ecology and Management 118:127-138.
- Lovejoy, T.E. & R.O. Bierregaard. 1990. Central Amazonian Forest and the minimal critical size of ecosystems project. In: Four Neotropical Rainforest, pp 60-71, Yale University Press.
- Quesada, C.A., Lloyd, J., Anderson, L.O., Fyllas, N.M., Schwarz, M., Czimczik, C., Paiva, R., et al. 2010-2011. Soils of Amazonia with particular reference to the RAINFOR sites; Variations in chemical and physical properties of Amazon forest soils in relation to their genesis. Biogeosciences.
- RADAMBRASIL. 1978. Levantamento de recursos naturais. Folha SA20 Manaus. Ministério de Minas e Energia.
- Ranzani, G. 1980. Identificação e caracterização de alguns solos da Estação Experimental de Silvicultura Tropical do INPA. Acta Amazonica, 10(1):7-41.