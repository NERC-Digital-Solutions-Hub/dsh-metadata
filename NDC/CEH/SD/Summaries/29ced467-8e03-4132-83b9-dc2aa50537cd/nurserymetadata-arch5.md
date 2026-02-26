# Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011

## Overview
- Seed from ten trees from each of 21 native Scottish Scots pine populations collected in March 2007; germinated and grown in three nurseries across Scotland, with a total of 5,040 individuals (210 families x 24 progeny).
- Experimental design: 210 families allocated to three nurseries (NW, NE, NG) in 40 randomized blocks per nursery; two trees per population per block.
- In 2010, NG plants moved outdoors to Glensaugh; all plants repotted into larger pots and re-blocked.
- Phenotype assessments conducted from 2007-2011 across three trait types: phenology, form, and cumulative growth; mortality recorded annually 2007-2010.

## Access, Licensing, and Attribution
- Data accessible at: https://doi.org/10.5285/29ced467-8e03-4132-83b9-dc2aa50537cd
- License: Open Government Licence v3
- Required citation in any publications describing research using the data:
  Perry, A.; Beaton, J.K.; Stockan, J.A.; Cottrell, J.E.; Iason, G.R.; Cavers, S. (2022). Long-term multisite Scots pine trial, Scotland: nursery phenotypes, 2007-2011. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/29ced4678e03-4132-83b9-dc2aa50537cd
- Attribution statement to acknowledge source: "Contains data supplied by UK Centre for Ecology & Hydrology."
- Include any copyright notices from the metadata on all copies of the data, publications, and presentations.

## Data Description and Scope
- Population coverage: 21 native Scottish Scots pine populations representing the species’ native range; three populations from each of seven seed zones.
- Seed handling and nursery setup described, including dormancy breaking, germination, transplanting, substrate, and fertiliser regimes.
- Experimental layout: three nurseries ( NW, NE, NG ) with outdoor and glasshouse conditions; randomised blocks; two trees per population per block.
- 2010 changes: NG seedlings moved outdoor to Glensaugh and all plants repotted into 3 L pots with Ericaceous compost and slow-release fertiliser.
- Traits measured:
  - Phenology: budburst (2008) and growth cessation (2008)
  - Form: total number of buds (2008); needle length (2007-2009)
  - Cumulative growth: height (2007-2011); stem diameter (2008-2011); canopy width (2007-2009)
  - Mortality: recorded annually (2007-2010)
- Measurement schedule: annual measurements after each growing season; phenology assessed weekly during spring and autumn 2008.
- Data quality notes:
  - Height increments less than 0 mm treated as missing (NA) due to measurement error or damage.
  - Stem diameter increments between 0 and -2 mm adjusted to 0; increments < -2 mm set to NA.

## Data Structure and File Information
- File: NurseryTraits.txt (single data file)
- Key columns include:
  - PopulationCode, Family, Seedling
  - Nursery (NE, NG, NW) and Block07to10; Block10to12
  - FieldCode (transplant status, if applicable)
  - Height measurements: HA07–HA11 (mm)
  - Stem diameter: DA08–DA11 (mm)
  - Canopy width: CW07_1, CW07_2, CW08_1, CW08_2, CW09_1, CW09_2 (mm)
  - Needle length: NL07_1, NL07_2, NL08_1, NL08_2, NL08_3, NL09_1, NL09_2, NL09_3 (mm)
  - Bud counts and phenology: Bu08, BB08, GC08
  - Height increments: HI08–HI11 (mm)
  - Diameter increments: DI09–DI11 (mm)
  - Status per year: STATUS07–STATUS10 (ALIVE; or DEAD year)
- Units:
  - Height, diameter, canopy width, needle length, height increments, diameter increments (mm)
  - BB08, GC08: days
  - Bu08: count
  - STATUS: categorical life status per year
- Dataset scope: one file containing all trait measurements and derived fields described above.

## Provenance, Metadata Quality, and Reuse
- Detailed methodology provided for seed origin, nursery conditions, transplanting, and measurement approaches.
- Coordinates for nurseries and transplant sites documented.
- Version history:
  - 2022-05-04: First version
  - 2022-08-11: Corrected data type for Seedling from numeric to alphanumeric; added Data access and reuse section
- Reuse readiness:
  - Clear licensing and attribution requirements
  - Explicit citation and source acknowledgment
  - Metadata includes variable definitions and units, enabling proper interpretation and integration with other datasets

## Data Sharing and Updates
- Centralised data file (NurseryTraits.txt) representing multi-year measurements across three nursery sites.
- Data updates are possible if future revisions are released; current version includes 2007-2011 measurements with 2010 relocation and repotting events noted in the description.

## Governance and Stewardship Considerations
- Ensure continued accessibility via DOI and Open Government Licence v3; preserve attribution statements in all copies and publications.
- Maintain alignment with user needs by preserving comprehensive trait data across phenology, growth, and mortality for long-term pine studies.
- Preserve data provenance: retain site coordinates, nursery configurations, block designs, and year-by-year measurement schedules.
- Promote interoperability by documenting variable naming conventions, units, and coding (e.g., status codes, block identifiers).
- Be mindful of potential data limitations: while licensing is open, ensure proper citation and attribution; monitor for any future embargoes or proprietary concerns if part of dataset is reused with other data sources.