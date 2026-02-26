# ozone

- Objective
  - Assess interactive effects of ozone and jasmonate treatment on white clover (T. repens cv. Crusader), focusing on injury, senescence, and biomass including root nodules; evaluate whether methyl jasmonate (MeJA) modulates ozone responses.

- Experimental design
  - Seedlings were grown in plug trays, transplanted into 7.5 L pots with soil inoculated to establish a soil microbe population.
  - Treatments: uncut controls, cut+ (single cut to 4 cm prior to ozone exposure), and MeJa+ (uncut with weekly MeJA spray).
  - MeJA treatment: fresh 8 mM stock diluted to 500 µM final solution; sprayed once weekly; controls sprayed with 0.1% alcohol to equalize spraying effects.
  - Growth to greenhouse facility: 4 weeks after initial planting, 15 pots per treatment moved to six solardomes (hemispherical glasshouses) for ozone exposure; five replicate pots per treatment per dome.
  - Ozone exposure: randomly assigned profiles within domes; six ozone profiles categorized into low and high background groups (low: profiles 1–3; high: profiles 4–6). One dome had continuous monitoring of temperature, soil moisture, PAR, and humidity.
  - Replication: six domes with five replicates per treatment per dome; individual ozone treatments were not replicated within a dome but prior studies support the design's statistical validity for the solardome facility.

- Measurements and assessments
  - Injury and senescence: monitored weekly with classification of leaves as injured or senesced if >25% of the adaxial surface was affected; injury and senescence expressed as a percentage of leaves on a representative quarter.
  - Biomass and components: harvest after 4 weeks for shoot biomass, root biomass, root nodules, and leaf area index (LAI) from undamaged leaves; roots and nodules separated, dried, and weighed; nodules counted and weighed; LAI calculated from dried forage samples.
  - Timing: injury assessments recorded in weeks 2, 3, and 4; weekly canopy management and watering as described.
  - Data scaling: injury and senescence data are arcsine-transformed for analysis; total metrics calculated per pot to account for biomass differences.

- Data sets and structure
  - biomass1worksheet.csv (23 columns)
    - Key fields: pot, treatment.code (a: MeJa+ Cut, b: MeJa+, c: Cut+, d: control), jasmonate, cutting, dome, mean.ozone, ozone category (low/medium/high), shoot.biomass, roots.biomass, nodules, total.biomass, root:shoot ratio, nodule metrics, mass per nodule, etc.
  - injury_first_assessment.csv, injury_second_assessment.csv, injury_third_assessment.csv (each with 11 columns)
    - Key fields: pot, treatment (a: MeJa+, Cut+; b: MeJa+; c: Cut+; d: control), jasmonate, cutting, dome, mean.ozone, total.injury, total.senescence, total.leaves, percent.injured, percent.senesced.
  - Scope: phytometer-style experiment examining interactive effects of ozone and jasmonic acid on pasture, including select biomass and ozone injury data.

- Analysis and software
  - Statistical analyses performed in R (version 3.1.2).
  - ANOVA: factors—ozone background (low vs high) and treatment; data arcsine-transformed for injury parameters.
  - Posthoc: Tukey's Honestly Significant Difference (HSD) tests to determine factor significance.
  - Correlations: Pearson correlations between total root nodule biomass and total biomass, and between raw injury parameters and biomass per treatment.
  - Data handling: detailed in data files with explicit variable descriptions and units; dataset metadata included for discoverability.

- Context and relevance
  - This work investigates how jasmonate signaling (MeJA) interacts with ozone stress to influence biomass allocation, root symbiosis (nodules), and surface-level leaf injury in white clover.
  - The design integrates multiple data types (biomass, nodulation, injury, senescence) across treatments, ozone backgrounds, and time points, enabling correlational and predictive analyses.
  - Previous cited studies (e.g., Hayes et al. 2010; Hewitt et al. 2014; Wagg et al. 2013) support the experimental approach and use of the solardome facility for ozone manipulation.