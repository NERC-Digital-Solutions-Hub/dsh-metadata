# Influence of jasmonic acid on the effect of ozone on pasture

- Purpose and scope
  - Examines interactive effects of ozone exposure and methyl jasmonate (MeJa) treatment on white clover (Trifolium repens cv Crusader) growth, injury, and physiology.
  - Data and methods describe the experimental design, data collection, and analysis workflow used to assess ozone- and jasmonate-mediated responses.

- Experimental design
  - Plant material and preparation: Seedlings propagated in plug-plant trays, transplanted to 7.5 L pots with soil inoculation to introduce soil microbes.
  - Treatments (three main): uncut control, cut+ (single cut to 4 cm height prior to ozone exposure), and MeJa+ (uncut with weekly MeJa spray).
  - Ozone exposure: Plants allocated to six solardomes; random ozone profiles applied. Within-dome replication included 5 pots per treatment (total per dome: 15 pots).
  - Environment and maintenance: Continuous monitoring of temperature, soil moisture, PAR, and humidity in at least one dome; plant rotation every week; watering twice weekly with extra as needed.
  - Duration: 4 weeks of ozone exposure (start 28/05/2014 to 24/06/2014).
  - Replication considerations: Individual ozone treatments were not replicated within domes; prior studies support the statistical validity of this design in the solardome facility.

- Data collected and variables
  - Injury and senescence: Leaves categorized as injured or senesced if >25% surface affected; recorded as a percentage per pot and aggregated across weeks 2–4.
  - Biomass and morphology: Shoot biomass, root biomass, nodules (numbers and mass), total biomass, mass per nodule, and root:shoot ratio; drying and weighing procedures described.
  - Leaf area and vigor indicators: Leaf area index (LAI) derived from dried forage samples.
  - Ozone exposure metrics: Ozone profiles grouped into low (profiles 1–3) and high background (profiles 4–6); mean ozone concentration and ozone range recorded per pot.
  - Data structure: Separate datasets for biomasses and for injury assessments, with detailed columnar metadata.

- Data files and schema
  - Biomass dataset (biomass1worksheet.csv; 23 columns)
    - Key fields: pot, treatment, MeJa+ (yes/no), cutting (yes/no), dome, mean.ozone, ozone (low/medium/high range), shoot.biomass, roots.biomass, nodules, total.biomass, root:shoot, nodule.biomass, mass.per.nodule, etc.
  - Injury datasets (injury_first_assessment.csv, injury_second_assessment.csv, injury_third_assessment.csv; 11 columns each)
    - Key fields: pot, treatment, Jasmonate, cutting, dome, mean.ozone, total.injury, total.senescence, total.leaves, percent.injured, percent.senesced.
  - Overall purpose: Data describe interactive effects of ozone and jasmonic acid treatments on white clover, including selected biomass and ozone injury measures.

- Data processing and analysis
  - Statistical methods: Analysis of variance (ANOVA) with ozone background and treatment as factors; Tukey's honest significant difference (HSD) tests for posthoc comparisons.
  - Correlation analyses: Pearson correlations between total root nodule biomass and total biomass, and between biomass and injury metrics for each treatment.
  - Data transformation: Injury data arcsine transformed prior to ANOVA to meet test assumptions.
  - Software: All analyses performed in R (version 3.1.2).

- Key considerations and implications for data leadership
  - The study demonstrates end-to-end data handling: experimental design, structured data capture with clear metadata, and robust statistical analysis.
  - The data schema supports reproducibility and reuse for exploring interactions between abiotic stress (ozone) and biochemical signaling (jasmonate) in pasture species.
  - Documentation of data provenance (treatment codes, ozone background, dome assignments) facilitates discoverability and interoperability, essential for cross-project data collaboration and governance.

- Relevance to data governance and strategy
  - Highlights the importance of detailed metadata, standardized column naming, and explicit data transformations to ensure discoverability, quality, and reusability across teams and networks.
  - Illustrates potential challenges in complex field-like experiments (e.g., non-replicated individual ozone treatments within domes) and the need to document design rationales for proper interpretation and stewardship.