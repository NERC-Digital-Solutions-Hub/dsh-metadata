# Influence of jasmonic acid on the effect of ozone on pasture

## Overview
- Investigates interactive effects of ozone and methyl jasmonate (MeJa) on white clover (Trifolium repens cv. Crusader) biomass and ozone injury.
- Plant material: seedlings propagated from seeds obtained from Wynnstay Seeds (UK); inoculated soil microbial population introduced via soil slurry.
- Experimental setup: plants grown in plug trays, then in 7.5 L pots; three treatments across pots (uncut control, cut+ with a single cut before ozone exposure, MeJa+ with weekly MeJa spray).
- Ozone exposure: conducted under six solardomes (hemispherical glasshouses) at the CEH solardome facility; randomised ozone profiles applied for 4 weeks.
- Environment tracking: temperature, soil moisture, PAR, and relative humidity monitored; plants rotated weekly and watered regularly.
- Replication and design notes: 5 replicate pots per treatment per dome; ozone profiles categorized as low or high background; some caution on within-dome replication but established methodological validity for solardome studies.

## Experimental design and data collection
- Timeline: seedling propagation in early 2014, growth to potting stage, treatment application, then 4-week ozone exposure starting late May 2014; harvest in June 2014.
- Treatments:
  - Uncut (control)
  - Cut+ (single cut to 4 cm height immediately prior to ozone exposure)
  - MeJa+ (uncut with weekly MeJa spray; fresh 8 mM stock diluted to 500 µM final solution; 0.1% ethanol as solvent)
- Spraying controls: uncut and cut+ pots sprayed with 0.1% alcohol solution to equalize handling effects.
- Sample collection: representative quarters of each pot analyzed for injury, senescence, biomass, and nodule metrics; LAI measured from dried forage.
- Measurements: injury and senescence assessed visually (injury >25% leaf area considered injured; senescence similarly defined); biomass separated into shoot, root, and nodules; nodules counted and weighed; biomass data adjusted for biomass differences between treatments.
- Data handling: ozone profiles grouped into low (profiles 1–3) and high background (4–6); data analyzed by ANOVA with ozone background and treatment as factors; posthoc Tukey tests performed; relationships between root nodules and biomass evaluated by Pearson correlations; analyses conducted in R (v3.1.2).

## Data structure and contents
- Data files:
  - biomass1worksheet.csv (23 columns)
    - Key fields: pot, treatment.code (b = MeJa+, c = cut+, d = control), Jasmonate (yes/no), cutting (yes/no), dome (solardome number), mean.ozone (ppb), ozone category (low/medium/high), shoot.biomass, roots.biomass, nodule.biomass, total.biomass, root:shoot, nodules, nodules.pot, dry weights, mass per nodule, and other related biomass metrics.
  - injury_first_assessment.csv
  - injury_second_assessment.csv
  - injury_third_assessment.csv
    - Each injury file contains 11 columns: pot, treatment, Jasmonate, cutting, dome, mean.ozone, total.injury, total.senescence, total.leaves, percent.injured, percent.senesced.
- Dataset scope:
  - Subjects: interactive effects of ozone and jasmonic acid on white clover.
  - Variables cover: treatment identity, MeJa presence, cutting status, environmental dome, ozone exposure, biomass components (shoots, roots, nodules), root-to-shoot ratio, nodule metrics, injury and senescence measures, leaf counts, and derived proportions.

## Data processing and analysis notes
- Injury and senescence calculations: reported as raw totals per representative quarter and converted to percentages; arsin(e) transformations applied prior to ANOVA.
- Statistical analyses: ANOVA with factors of ozone background and treatment; Tukey HSD for posthoc comparisons; Pearson correlations between total root nodule biomass and biomass metrics or injury parameters.
- Software: all analyses conducted in R (v3.1.2).

## Data governance, accessibility, and metadata
- Data provenance: experiments conducted in 2014 at CEH solardome facility; detailed methodological notes provided for growth, treatments, ozone profiles, and measurement procedures.
- Metadata coverage:
  - Comprehensive column-level explanations included in dataset descriptions (e.g., column meaning, units, and coding for treatments).
  - Clear documentation of treatment codes (MeJa+, Cut+, Control) and corresponding variables (Jasmonate, cutting).
  - Ozone exposure context (low vs. high background) and dome-level environmental monitoring details.
- Sharing considerations:
  - Datasets are organized for reuse in plant-ozone interaction studies; raw and derived metrics are available (biomass, injury, senescence, nodules).
  - To facilitate discovery and interoperability, ensure consistent coding schemes, explicit method descriptions, and provenance notes accompany data when archived or deposited in a data portal.
- Limitations and notes for stewardship:
  - Within-dome replication of specific ozone treatments is limited; cross-study comparability requires attention to experimental context and dome-specific conditions.
  - Some treatment combinations (e.g., MeJa+ Cut) have incomplete biomass data noted in the file descriptions.

## Practical implications for data stewards
- Ensure metadata clarity for treatment codes and chemical treatments (MeJa concentration, solvent).
- Maintain provenance links between the biomass and injury datasets to support integrated analyses.
- Preserve environmental context (dome, mean ozone, background ozone) to enable reproducibility and secondary analyses.
- Include details on sampling strategy (representative quarter, definitions of injury/senescence) and data transformations (arcsine) used in analyses.
- Consider indexing datasets by dome, treatment, and replicate to support robust data discovery and future meta-analyses.