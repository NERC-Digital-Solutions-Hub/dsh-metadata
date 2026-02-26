# ozone

- The document describes a phytometer experiment examining the interactive effects of ozone exposure and methyl jasmonate (MeJa) on white clover (T. repens cv. Crusader). The study uses a controlled, multi-factor design to assess biomass production and ozone-related injury.

## Experimental design and sampling

- Plant material: Seedlings of T. repens cv. Crusader propagated in plug trays, then grown in 7.5 L pots with compost.
- Treatments: 
  - Uncut control
  - Cut+ (single cut to 4 cm height immediately before ozone exposure)
  - MeJa+ (uncut with weekly MeJa spraying)
- MeJa treatment: 8 mM stock solution in alcohol, diluted to 500 µM final solution with 0.1% ethanol; sprayed weekly on the canopy.
- Experimental setup:
  - 6 solardomes (hemispherical glasshouses, ~3 m diameter) at a CEH facility in Bangor, North Wales.
  - 15 pots per treatment per dome (5 replicates per treatment per dome); total 90 pots across 6 domes.
  - Ozone profiles applied randomly across domes for a 4-week exposure (start 28 May 2014 to 24 June 2014).
  - One dome included continuous monitoring of ambient temperature, soil moisture, PAR, and humidity.
  - Plants rotated weekly within domes; watered twice weekly with extra watering as needed.
- Data collection timeline:
  - Weeks 2–4: assessment of healthy, injured, or senesced leaves from a representative quarter of each pot.
  - Injury defined as >25% of adaxial leaf surface affected; senescence similarly assessed.
  - Biomass harvest after 4 weeks for shoots, roots, and root nodules; leaves dried for LAI estimation.

## Data collected and variables

- Biomass measurements:
  - Shoot biomass and dry weight
  - Root biomass (including dry weight and per-pot calculations)
  - Nodule biomass, count, and mass (per pot and per representative quarter)
  - Total biomass (shoots + roots + nodules)
  - Root-to-shoot ratio
  - LAI estimated from dried forage
- Injury metrics:
  - Total injury and total senescence per representative quarter
  - Total number of leaves per quarter
  - Percent injured and percent senesced leaves
- Experimental metadata:
  - Dome number, treatment code (MeJa+, Cut+, or control), jasmonate treatment (yes/no), cutting treatment (yes/no)
  - Mean ozone exposure (mean.ozone) and ozone category (low, medium, high)
- Data structure notes:
  - Injury and biomass data are recorded on a per-pot basis with aggregation to per-quarter observations.
  - Ozone background is categorized into low vs. high for certain analyses.

## Data processing and analysis

- Data transformations:
  - Injury and senescence data arc-sine transformed prior to analysis.
- Statistical analyses:
  - Analysis of variance (ANOVA) with factors for ozone background and treatment.
  - Post hoc comparisons using Tukey’s honest significant difference tests.
  - Correlation analyses (Pearson) between total root nodule biomass and other biomass/injury parameters.
- Software:
  - All analyses conducted in R (version 3.1.2).

## Data files and schema

- biomass1worksheet.csv
  - 23 columns; key fields include:
    - pot (pot number), treatment.code (MeJa+, Cut+, or control)
    - Jasmonate (yes/no), cutting (yes/no), dome (solardome number)
    - mean.ozone, ozone (low/medium/high)
    - shoot.dry, shoots.bag, shoot.biomass
    - roots.dry, roots.bag, root biomass, roots.pot
    - root:shoot, nodules, nodules.pot, nodule.bag
    - dry, nodule.biomass, nodule.biomass.pot
    - total.biomass, mass.per.nodule
- injury_first_assessment.csv
- injury_second_assessment.csv
- injury_third_assessment.csv
  - Each injury file contains 11 columns with:
    - pot, treatment (a: MeJa+ Cut+, b: MeJa+, c: Cut+, d: control)
    - Jasmonate (yes/no), cutting (yes/no)
    - dome, mean.ozone
    - total.injury, total.senescence, total.leaves
    - percent.injured, percent.senesced

- Summary of data scope:
  - The datasets cover the interactive effects of ozone and jasmonic/methyl-jasmonate treatments on white clover, including both biomass production and ozone-related injury metrics.

## GIS-relevant implications and potential data products

- Spatial framing:
  - Although not a geographic field study, the data include a dome-level and pot-level structure (dome number, pot identity, treatment, ozone exposure) suitable for spatial-type visualization within a GIS environment.
  - Potential to map ozone exposure (mean.ozone) and injury/biomass responses by dome and pot to explore spatial patterns of stress responses in a controlled environment.
- Data integration opportunities:
  - Combine with additional environmental layers (temperature, humidity, PAR) captured in the monitoring dome to build environmental suitability or stress maps.
  - Link biomass and injury outcomes to ozone profiles for predictive mapping of ozone sensitivity across treatments.
- Data quality and provenance:
  - Clearly documented experimental design, replication within domes, and detailed variable definitions support reproducibility and traceability in GIS analyses.

## Additional notes

- The study emphasizes randomized ozone exposure and robust statistical treatment, with careful consideration of canopy-level management (cutting vs. non-cutting) and jasmonate treatment.
- The datasets are structured to support both traditional statistics and potential spatial visualization of treatment effects within the solardome facility.