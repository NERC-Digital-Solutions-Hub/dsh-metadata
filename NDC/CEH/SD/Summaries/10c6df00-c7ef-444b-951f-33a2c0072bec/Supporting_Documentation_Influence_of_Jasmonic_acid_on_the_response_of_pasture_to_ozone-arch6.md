# ozone

## Purpose and scope
- Investigates interactive effects of ozone and methyl jasmonate (MeJa) on white clover (Trifolium repens) grown with soil microbial inoculation.
- Examines how cutting and jasmonate treatment modulate ozone injury and plant biomass, with measurements of shoot/root biomass, nodules, and injury indicators.

## Experimental design
- Plant preparation: seedlings propagated in plug-plant trays, transferred to 7.5 L pots with John Innes No. 2 compost; 3 seedlings per pot.
- Treatments (3 total):
  - Uncut (control)
  - Cut+ (single cut to 4 cm height immediately before ozone exposure)
  - MeJa+ (uncut with weekly methyl jasmonate spray)
- MeJa administration: 8 mM stock in alcohol, diluted to 500 µM final solution with 0.1% ethanol; sprayed once weekly; controls sprayed with 0.1% alcohol solution.
- Growing environment: six solardomes (3 m diameter, 2.1 m high) at CEH solardome facility, near Bangor, North Wales; ozone profiles applied randomly across domes.
- Replication and duration: 15 pots per treatment across six domes; 4-week exposure period (28 May–24 June 2014); plants rotated weekly; regular watering.
- Environmental monitoring: in one dome, continuous measurements of ambient temperature, soil moisture, PAR, and relative humidity.
- Injury assessment: weeks 2–4, leaves categorized as healthy, injured, or senesced; injury/senescence expressed as a percentage of adaxial leaf area.

## Data collected and measurements
- Biomass and morphology:
  - Shoot biomass, root biomass, and nodules (per pot and per representative quarter)
  - Root:shoot ratio
  - Nodule metrics: count, mass, and mass per nodule
  - Total biomass (shoot + root + nodules)
  - Leaf area index (LAI) from dried forage
- Ozone exposure:
  - mean ozone concentration per pot
  - ozone treatment category: low, medium, high
  - ozone background used as a factor in analyses
- Injury indicators:
  - Total injury and total senescence (per representative quarter)
  - Total leaves per quarter
  - Percent injured and percent senesced

## Data files and structure
- Biomass data: biomass1worksheet.csv (23 columns)
  - Key fields: pot, treatment code (MeJa+, Cut+, control), jasmonate, cutting, dome, mean.ozone, ozone category, shoot.biomass, root.biomass, nodules, total.biomass, root:shoot, nodule.biomass.pot, mass.per.nodule, etc.
- Injury data: injury_first_assessment.csv, injury_second_assessment.csv, injury_third_assessment.csv (each with 11 columns)
  - Key fields: pot, treatment, jasmonate, cutting, dome, mean.ozone, total.injury, total.senescence, total.leaves, percent.injured, percent.senesced.
- Context: Data concern a phytometer experiment assessing interactive effects of ozone and jasmonic acid on white clover; includes both biomass and ozone injury data.

## Analysis and processing
- Statistical approach:
  - Analysis of variance (ANOVA) with factors: ozone background and treatment
  - Posthoc Tukey's honest significant difference tests where appropriate
  - Relationships between total root biomass and total biomass, and raw injury parameters assessed via Pearson correlations
- Data handling:
  - Injury data arcsine-transformed prior to ANOVA
- Software:
  - Analyses conducted in R (version 3.1.2)
- Design notes:
  - Individual ozone treatments within a dome were not replicated; the solardome facility has established statistical validity for this setup in prior studies (cited references include Hayes et al. 2010; Hewitt et al. 2014; Wagg et al. 2013).

## Context, provenance, and limitations
- Location: CEH solardome facility, Bangor, North Wales, UK
- Related literature: Hayes et al. 2010; Hewitt et al. 2014; Wagg et al. 2013; Hewitt et al. 2014 (in prep)
- Limitations:
  - Ozone treatments within a dome not replicated; randomization and multiple domes mitigate this, but readers should consider dome-level effects when interpreting results.
  - Findings are based on controlled, collector-phase conditions (solardomes) and may differ from field conditions.

## Potential uses and data applications
- Facilitate self-serve exploration of treatment-by-ozone interactions in white clover
- Combine with other datasets for broader meta-analyses or policy-relevant insights on ozone stress and jasmonate signaling
- Build dashboards or data products to visualize biomass and injury responses across treatments and ozone backgrounds
- Reproduce analyses in R and derive additional metrics or cross-variable relationships from the provided data files