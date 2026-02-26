# Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011

## Data access and reuse
- Data URL: https://doi.org/10.5285/29ced467-8e03-4132-83b9-dc2aa50537cd
- Licence: Open Government Licence v3
- Citation to use in reports/publications: Perry, A.; Beaton, J.K.; Stockan, J.A.; Cottrell, J.E.; Iason, G.R.; Cavers, S. (2022). Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/29ced4678e03-4132-83b9-dc2aa50537cd
- Attribution statement to include: "Contains data supplied by UK Centre for Ecology & Hydrology."
- Copyright: Include any copyright notice from the metadata record in all copies and presentations.

## Data description
- Seed origins: 210 families (10 families per 21 native Scottish Scots pine populations), each family from the same mother tree (half-siblings assumed).
- Field collection and germination: seeds collected March 2007; germinated June 2007 at James Hutton Institute, Aberdeen; dormancy breaking and storage steps described; 24 candidate seedlings per family prepared.
- Nurseries and layout: seedlings distributed to three nurseries (NW, NE, NG) in 2010; 40 randomised blocks per nursery; two trees per population per block (total 42 trees per block; 1,680 per nursery; 5,040 seedlings total initially).
- Transplant and growth conditions: initial pots (8 cm x 8 cm x 9 cm) with Levington's C2a compost and Osmocote fertiliser; later repotted (2010) into 19 cm pots with Levingtons CNSE Ericaceous compost and Osmocote fertiliser; outdoor and glasshouse conditions with no artificial light.
- Experimental design: three nursery sites (NW, NE, NG) with distinct environments; three blocks of data across time; plants reorganised into new blocks in 2010.
- Phenotype assessments (2007–2011) across three trait types:
  - Phenology: budburst and growth cessation (budburst measured as days from 31 March 2008 to green needles observed; growth cessation as days from 10 September 2008 to end of growth).
  - Form: total number of buds (2008); needle length (three needles per tree; 2007–2009).
  - Cumulative growth: height (2007–2011); stem diameter (2008–2011); canopy width (2007–2009).
- Mortality: recorded annually from 2007–2010.
- Data processing rules: fix negative height increments as missing; small negative stem diameter increments (-2 mm) adjusted to zero; increments < -2 mm set to missing.

## File information
- Single file: NurseryTraits.txt
- Key variables (examples):
  - PopulationCode, Family, Seedling, Nursery (NE, NG, NW)
  - Block07to10, Block10to12 (block identifiers by period)
  - FieldCode (transplant site), HA07–HA11 (height after years), DA08–DA11 (stem diameter after years)
  - CW07_1, CW07_2, CW08_1, CW08_2, CW09_1, CW09_2 (canopy width measurements)
  - NL07_1, NL07_2, NL08_1, NL08_2, NL08_3, NL09_1, NL09_2, NL09_3 (needle length)
  - Bu08 (buds observed after 2nd growing season), BB08 (days to budburst), GC08 (growth cessation)
  - HI08–HI11 (height increments), DI09–DI11 (stem diameter increments)
  - STATUS07–STATUS10 (survival status; ALIVE or DEAD dates)
- Note: Seedling variable was corrected to Alphanumeric type (not numeric).

## Data collection and quality aspects
- Data span: 2007–2011 for growth and phenology; annual mortality checks.
- Measurement approaches: standardized timing and methods for height, diameter, canopy width, budburst, growth cessation, needle length, and bud counts.
- Data quality handling: explicit missing data rules and adjustments for measurement inconsistencies.
- Data hosting and republishing: version history indicates updates to data description and reuse guidance.

## Version history
- 2022-05-04: First version released.
- 2022-08-11: Corrected Seedling variable data type (numeric to Alphanumeric) and added Data access and reuse section.