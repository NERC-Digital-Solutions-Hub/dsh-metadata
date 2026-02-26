# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Supplementary dataset to the paper: Sainsbury et al. (2018) on long-term increases in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain.
- Contains detailed column-level explanations for PolecatRodenticidesFINAL2013-2016March2019EIDC.csv, covering data collected 2013–2016.
- Data are tied to carcass collection and chemical analyses of rodenticide residues, with isotopic measurements from whiskers.

## Dataset structure and key variables
- Batch-level metadata
  - Batch: chemical analysis batch for processing
  - Batch, Notes/Batch, # (sample within batch): identifiers and notes
- Sample and record identifiers
  - record: unique ID for animal (Vincent Wildlife Trust)
  - Collector.no: unique ID for animal (National Museums Scotland)
- Cause and timing
  - CoD: cause of death
  - month, year: collection timing; season; halfYear (December–May = FIRST; June–November = SECOND)
- Location and environment
  - x, y: coordinates in metres (OSGB36)
  - region: North, South, East, West
  - landClass: land-use classification (based on CEH Land Cover map 2007; 1 km buffers applied)
  - resistanc e: area with known resistance to SGARs in rodents
- Animal attributes
  - sex: male/female
  - age: age category
  - alive: status or age at collection
  - fat: kidney fat score (0–4 scale)
- Chemical residues in liver
  - brom, difm, floc, brod, dife: concentrations of specific anticoagulants (µg/g; zero = not detected)
  - bRods, bBrom, bDifm, bFloc, bBrod, bDife: presence/absence of each compound (1 = detected)
  - cRods: number of rodenticides detected in liver (0–4)
  - sumALL: total concentration of detected rodenticides (µg/g)
- Isotope measurements (whisker analysis)
  - meanN, sdN: mean and SD of δ15N for whisker
  - meanC, sdC: mean and SD of δ13C for whisker
  - dN15Max: maximum δ15N value across whisker segments
- Data quality and notes
  - NA: indicates no data available for that field
  - Some fields have specific units (e.g., µg/g for residues; Metres for coordinates)
- References within dataset
  - McDonald et al. (1998) cited for δ15N and δ13C interpretation guidance

## Data provenance and context
- Geographic and temporal scope: Great Britain, 2013–2016
- Data sources: collation from wildlife crime/collection programs (Vincent Wildlife Trust; National Museums Scotland) and chemical/isotopic analyses
- Related publication: 2018 Environmental Pollution article describing long-term exposure trends

## Data quality, standards, and interoperability
- Explicit column explanations provided to ensure consistent interpretation across systems and analyses
- Use of standardized coordinate reference (OSGB36) and land-cover overlay methodology (CEH Land Cover map 2007)
- Clear unit definitions for chemical concentrations and isotopic measurements
- Isotope references: guidance linked to McDonald et al. 1998 for comparability
- Handling of missing data: NA indicates missing observations; users should account for gaps during analyses

## Usage, sharing, and governance considerations for Data Stewards
- Data discoverability: well-documented column definitions support integration with other datasets and pipelines
- Data integration: standardized fields (timing, location, exposure measures, isotopes) enable cross-dataset linkage and meta-analyses
- Update and versioning: maintain consistent schema (units, field names) when incorporating new samples or extending timeframe
- Privacy and access: dataset pertains to wildlife samples; ensure appropriate data sharing permissions align with original collection agreements and institutional policies
- Quality assurance: maintain records of batch-level processing and detection statuses to support reproducibility

## Limitations and caveats
- Missing data indicated by NA in several fields; analyses should accommodate incomplete records
- Some fields rely on contextual lab methods or regional classifications (e.g., landClass, region); ensure consistent application across datasets
- Temporal and spatial coverage limited to 2013–2016 and GB, which may affect generalizability beyond study area

## References
- Sainsbury KA, Shore RF, Schofield H, Croose E, Pereira MG, Sleep D, Kitchener AC, Hantke G, McDonald RA (2018). Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution, 236: 689-698.
- McDonald, R.A., Harris, S., Turnbull, G., Brown, P., Fletcher, M. (1998). Anticoagulant rodenticides in stoats (Mustela erminea) and weasels (Mustela nivalis) in England. Environmental Pollution, 103, 17-23.