# Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011

## Overview
- A long-term, multisite seedling trial of Scots pine across Scotland, encompassing 210 families (10 families × 21 populations) and 5,040 individuals.
- Seedlings were grown in three nurseries (NW: western Scotland outdoor; NE: Aberdeen outdoor fruit cage; NG: Aberdeen unheated glasshouse) and later transplanted to additional sites.
- Phenotype data collected 2007–2011 across three trait types: phenology, form, and cumulative growth; mortality tracked annually 2007–2010.
- Data intended to support understanding of environmental health and long-term climate–genotype interactions, with standardised outputs for monitoring and policy evaluation.

## Data access and licensing
- Data available at: https://doi.org/10.5285/29ced467-8e03-4132-83b9-dc2aa50537cd
- Licence: Open Government Licence v3.
- Required citation for any research using the data: Perry, A.; Beaton, J.K.; Stockan, J.A.; Cottrell, J.E.; Iason, G.R.; Cavers, S. (2022). Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/29ced4678e03-4132-83b9-dc2aa50537cd
- Attribution: "Contains data supplied by UK Centre for Ecology & Hydrology."
- Include any copyright notice from the metadata in all copies, publications, and presentations.

## Data collection and experimental design
- Sampling: seeds from ten trees per population, across 21 native Scottish Scots pine populations (210 families total; 24 progeny per family; total 5,040 individuals).
- Germination and propagation: seeds germinated in Aberdeen; dormancy broken by 24-hour soak; maintained in controlled conditions before outplanting.
- Nurseries (sites and setup):
  - NW: outdoor nursery at Inverewe Gardens (western Scotland)
  - NE: outdoor fruit cage at James Hutton Institute (Aberdeen)
  - NG: unheated glasshouse at James Hutton Institute (Aberdeen)
- Experimental layout: 40 randomised blocks per nursery; two trees per population per block (total 42 trees per block).
- Transplanting and repotting: 8 seedlings per family moved to each nursery; 2010 repotted to 19 cm pots; later relocation of NG seedlings outdoors to Glensaugh.
- Data collection window: 2007–2011; no artificial lighting in nurseries.

## Traits and measurements
- Phenology (2008): budburst and growth cessation timing.
  - Budburst: days from 31 March 2008 to emergence of green needles.
  - Growth cessation: days from 10 September 2008 to end of growth.
- Form (2007–2009): total number of buds; needle length (average from three needles per tree).
- Cumulative growth (2007–2011): height (mm), stem diameter (mm), canopy width (mm; measured at two points and averaged).
- Mortality: recorded annually (2007–2010).
- Data handling specifics: 
  - Negative height increments (<0 mm) treated as missing.
  - Stem diameter increments between 0 and -2 mm adjusted to 0 due to measurement orientation differences.
  - Increments < -2 mm treated as missing along with the most recent diameter measurement.

## Data file and metadata
- File: NurseryTraits.txt
- Key variables (high level):
  - PopulationCode, Family, Seedling, Nursery
  - Block07to10, Block10to12
  - FieldCode (transplant status)
  - Height (HA07–HA11)
  - Stem diameter (DA08–DA11)
  - Canopy width (CW07–CW12)
  - Needle length (NL07–NL09)
  - Bud counts (Bu08)
  - Budburst timing (BB08)
  - Growth cessation timing (GC08)
  - Height increments (HI08–HI11)
  - Diameter increments (DI09–DI11)
  - Status per year (STATUS07–STATUS10)
- Units are provided for each variable (mm, days, counts, ALIVE/DEAD, etc.).

## Version history and notes
- 2022-05-04: First version released.
- 2022-08-11: Corrected description of the Seedling variable (from numeric to alphanumeric); added Data access and reuse section.

## Relevance for environmental monitoring
- Provides a long-term, standardised dataset of phenotypic responses across diverse pine populations and environments, enabling analysis of genotype-by-environment interactions over multiple years.
- Supports data integration with other environmental datasets for enhanced monitoring, trend analysis, and policy assessment.
- Data are citable and designed for reuse in environmental health and biodiversity monitoring contexts.