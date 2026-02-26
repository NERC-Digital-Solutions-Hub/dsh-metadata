# Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011

## Overview
- A long-term, multi-site experiment on Scots pine from native Scottish populations to study nursery phenotypes across three environments and multiple years.
- Seed from 21 populations (10 families per population, total 210 families) yielding 5,040 individuals (24 progeny per family).
- Seeds collected in 2007; germinated at James Hutton Institute (Aberdeen) and grown in three nurseries: NW (outdoors, western Scotland), NE (outdoors in a fruit cage, eastern Scotland), NG (unheated glasshouse, Aberdeen).
- In 2010, NG seedlings moved outdoors to Glensaugh (Aberdeenshire).
- Phenotype assessments conducted 2007-2011 for three trait types: phenology, form, and cumulative growth; mortality tracked 2007-2010.
- Data describe growth and development across years, enabling analysis of genetic and environmental influences on trait variation.

## Experimental design
- 210 families distributed across three nurseries in randomized blocks: 40 blocks per nursery; two trees per population per block (total 42 trees per block).
- 8 seedlings per family per nursery (total 1,680 per nursery).
- Plants reorganized into new blocks in 2010; all plants repotted into larger pots with standardized Ericaceous compost and slow-release fertilizer.
- No artificial light; different watering regimes by nursery (automatic in NG; manual in NE and NW).
- Seedlings have been monitored and measured annually after each growing season; data quality checks applied (e.g., handling of negative height increments and measurement orientation issues).

## Data collected and definitions
- Phenology: budburst (days from 31 March 2008 to green needles visible) and growth cessation (days from 10 September 2008 to end of growth).
- Form: 
  - Total number of buds (Bu08; counts) measured after 2nd growing season.
  - Needle length (NLxx; mm) averaged across three needles per tree.
- Cumulative growth: 
  - Height (HA07–HA11; mm) across 2007–2011.
  - Stem diameter (DA08–DA11; mm) across 2008–2011.
  - Canopy width (CW07_1, CW07_2, CW08_1, CW08_2, CW09_1, CW09_2; mm) across 2007–2009.
- Mortality: status tracked annually (STATUS07–STATUS11; ALIVE or DEAD with year suffix).
- Data cleaning notes: 
  - Height increments < 0 mm treated as missing.
  - Diameters with small negative increments (−2 mm) adjusted to 0 due to measurement orientation.
  - Diameters with increments < −2 mm treated as missing.

## File information
- File: NurseryTraits.txt
- Key variables:
  - PopulationCode, Family, Seedling, Nursery (NE, NG, NW), Block07to10, Block10to12, FieldCode (transplant sites), Ha07–Ha11 (height), Da08–Da11 (stem diameter), CW07_1, CW07_2, CW08_1, CW08_2, CW09_1, CW09_2 (canopy width), NL07_1, NL07_2, NL08_1, NL08_2, NL08_3, NL09_1, NL09_2, NL09_3 (needle length), Bu08 (bud count), BB08 (budburst days), GC08 (growth cessation days), HI08–HI11 (height increment), DI09–DI11 (diameter increment), STATUS07–STATUS11 (survival).
- Units included for all measurements (e.g., mm, days, counts).

## Data access, usage, and attribution
- Data access: https://doi.org/10.5285/29ced467-8e03-4132-83b9-dc2aa50537cd
- License: Open Government Licence v3
- Citation to include in any publication: 
  Perry, A.; Beaton, J.K.; Stockan, J.A.; Cottrell, J.E.; Iason, G.R.; Cavers, S. (2022). Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/29ced4678e03-4132-83b9-dc2aa50537cd
- Attribution statement to use: "Contains data supplied by UK Centre for Ecology & Hydrology."
- Copyright: Include any metadata-provided copyright notice in all copies and publications.

## Reuse considerations and potential analyses
- Large, multi-site, long-term dataset suitable for:
  - Investigating genetic vs. environmental influences on growth, phenology, and form across Scots pine populations.
  - Developing predictive models of height, diameter, canopy development, and phenology traits under varying nursery environments.
  - Examining survival and growth trajectories from 2007 to 2011 and relationships with early-life phenotypes.
- Consider limitations:
  - Data are from controlled nurseries, with a later outdoor transplant; environment-specific effects may influence extrapolation to natural habitats.
  - Missing data handling and measurement errors noted in the data description.
  - The scale of the environment (three distinct nursery settings) provides broad context but may require careful modeling of site effects.
- Geographic references and setup:
  - Nurseries located at NW (57.775714, −5.597181), NE (Aberdeen), NG (Aberdeen; unheated glasshouse); external transplant site Glensaugh (56.893567, −2.535736) in 2010.
- Data is suitable for regression, mixed-effects models, and multi-level analyses that account for family, population, block, and nursery-level variance.