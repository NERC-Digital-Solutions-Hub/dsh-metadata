# Impacts of experimental drought and plant trait diversity on floral resources and pollinator visitation

- Study goal: Assess how plant functional diversity and experimentally imposed drought influence floral resources and pollinator visitation, linking plant community traits to ecosystem functions.

- Context: Field-based dataset from the Winklebury Hill experiment in Wiltshire, UK (2013–2016), focusing on how functional trait groupings affect carbon and nitrogen cycling, floral resources, and pollinator activity under drought.

- Key components:
  - Plant communities created using seeds and plugs to represent three functional groups (FG1–FG3) with distinct root and leaf traits.
  - Drought manipulation via rain shelters and control treatments to simulate extreme drought events.
  - Measurements of floral resources and nectar, plus pollinator visitation to assess potential impacts on pollination services.

## Study site, design, and treatments

- Location and habitat: Ex-arable calcareous grassland on chalk soil in Wiltshire, UK (coordinates provided); plots established on bare soil in 8 m x 8 m blocks with 2 m gaps.
- Experimental design: 24 plots arranged in a grid across six blocks; seven plant community combinations across FG1–FG3, plus replicates of each combination within blocks.
- Plant functional groups:
  - FG1: Deep, thick tap or stoloniferous roots; large, thin leaves; hypothesized low nutrient cycling and poor drought resistance.
  - FG2: Long-lived, shallow tap roots, small rosettes; hypothesized low nutrient cycling but relatively good drought resistance.
  - FG3: Long-lived, shallow, fibrous roots; thick, fleshy leaves; hypothesized high nutrient cycling and decent drought resistance.
- Drought manipulation: Introduced in 2015 and 2016 using rain shelters to create six-week dry periods (simulated drought) with ambient rain in control plots and a roofed-control treatment to account for potential shelter effects.
- Drought realism: Shelter period modeled as a one-in-100-year drought using a Gumbel distribution based on a decade of local rainfall data; soil moisture measured after drought to confirm effects.

## Plant functional diversity and species composition

- Sowing strategy: Seven experimental plant communities formed by combining FG1, FG2, and FG3 in varied proportions; each plot replicated across blocks.
- Species mix: Includes a range of calcareous grassland species within each functional group; detailed species lists provided in supplementary materials.
- Community context: From 2015 onward, drought shelters remained in place during the defined drought window to simulate extreme conditions.

## Data collected and measurements

- Floral resources and nectar:
  - Floral resources recorded per subplot: number of flowers, flower diversity, and proportion of flowers with nectar; nectar volume and sugar concentration measured for up to three flowers per raceme of selected focal species (Lathyrus pratensis, Onobrychis viciifolia, Prunella vulgaris).
  - Nectar measurements: Nectar volume (μl) with microcapillaries; sugar concentration (mg/mg) with a refractometer; calculations to convert concentration to mg/μl and to estimate nectar produced per flower over 24 hours (w = v × c).
  - Handling notes: When nectar volumes were too small for readings, pooled measurements from flowers of the same species and treatment were used.
- Plant and resource surveys (community-scale and pollinator visitation):
  - Floral surveys in 1 m² quadrats: all flowering plants identified to species; floral units counted (one or multiple flowers that can be visited without flying between units).
  - Pollinator observations: 10-minute focal observations per quadrat to record insect visits to floral units; visitors identified to morphotype in the field; specimens collected for later identification.
  - Survey timing: Two rounds of surveys conducted between 18–22 July (weather criteria aligned with Pollard & Yates 1993).
- Data quality and ethics:
  - Standardized field protocols, data entry in MS Access, and anomaly checks.
  - Missing data noted in metadata; ethics approval obtained (CLES Penryn Research Ethics Committee, 2016/1429).

## Datasets and data integration

- Four main data files (NERC PropNectar and nectar, floral surveys, and pollinator surveys) with linked fields:
  - NERCPropNectar.csv: nectar accessions; fields include Raceme_ID, Plant_Species, Subplot_Type, CountWithNectar, TotalFlowersTested, Plot_ID, Row.
  - NERCNectar.csv: per-flower nectar metrics; fields include Plot_ID, ID, Raceme_ID, No_Floral_Units, Volume_Absolute (μl), Concentration_Absolute (mg/μl), Concentration_AverageBlanks, Sugar_Absolute (mg), Row.
  - NERCFloralSurveys.csv: floral survey details; fields include Plot_ID, FG, FG_Diversity, Date_Surveyed, Subplot_Type, SurveyID, IP_PlantSppRich, TotalNumberOfPollVisits, plus species-level floral unit counts (Columns 9–55).
  - NERCPollinatorSurveys.csv: pollinator visitation data; fields include Plot_ID, FG, FG_Diversity, Date_Surveyed, Subplot_Type, SubplotID, Survey_Number, SurveyID, TaxonomicID (lowest-level ID), Pollinator_Species_Code, Plant_Species, No_Visits.
- Linking across datasets: PlotID, SubplotID, RacemeID, and SurveyID are consistent between datasets to enable integrated analyses; Plot IDs can link to Fry et al. 2017/2018 datasets.

## Data quality, limitations, and notes

- Missing data:
  - Nectar concentration readings missing for 20% of observations due to small nectar volumes.
  - Some observer-related data gaps: first-round pollinator survey for subplot 14.C not conducted due to observer error.
- Coding and metadata considerations:
  - Raceme_ID and Plot_ID are categorical identifiers; some fields require categorical treatment in analyses.
  - Subplot_Type codes: D (full drought), C (control), R (roofed control).
- Ethics and governance:
  - Data collection approved by institutional ethics committee; data are described with clear QA notes and linking metadata to ensure reproducibility and reusability.

## Winklebury Hill experiment (contextual summary)

- Objective: Establish plant communities on bare chalk to test functional effects on carbon and nitrogen cycling and ecosystem health, with three functional effect trait groups.
- Experimental layout: Grid of plots (7 across by 6 down) incorporating all combinations of FG1–FG3, replicated across six blocks; from 2015, rain shelters added to impose drought conditions.
- Functional groups and expected effects:
  - Group 1: Deep, thick roots; high leaf area; variable life history; hypothesized to influence carbon storage and soil nutrient dynamics.
  - Group 2: Small rosettes; shallow roots; potential for limited carbon storage but some drought resistance.
  - Group 3: Large, shallow-rooted, fast nutrient cycling; potentially rapid carbon and nitrogen turnover.
- Timeframe: Field experiment conducted from 2013 to 2016, with ecosystem-function measurements aligned with plant community composition and drought treatment.