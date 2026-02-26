# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Purpose and context
- Data supplement to the paper: Sainsbury KA, et al. (2018) on long-term increase in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain.
- Covers chemical analyses of polecat liver residues and related metadata from 2013–2016.
- Intended to support reproducibility and further analysis by providing detailed column explanations for PolecatRodenticidesFINAL2013-2016March2019EIDC.csv.

## Data structure and key variables
- Batch: chemical analysis batch for processing; batch-level grouping.
- record: unique database identifier issued to the animal.
- Collector.no: database identifier issued by National Museums Scotland.
- CoD: cause of death.
- Temporal variables: month, year, season; halfYear (FIRST = December–May, SECOND = June–November).
- Location and environment: x (easting), y (northing) in metres (OSGB36); region (North, South, East, West); landClas s (predominant land use).
- Land cover context: land use derived by overlaying carcass locations onto the CEH Land Cover map (2007) with 1 km buffers to determine predominant class (arable vs pastoral).
- Resistance: whether the carcass was collected from an area with known resistance to SGARs in rodents.
- Demographics: sex; age; alive; fat (kidney fat score).
- Chemical residues in liver: brom, difm, floc, brod, dife (concentrations in µg/g; zero = not detectable).
- Detection indicators: bRods, bBrom, bDifm, bFloc, bBrod, bDife (whether each compound detected).
- Summary counts: cRods (number of rodenticides detected); sumALL (total µg/g of detected rodenticides).
- Isotopic measurements (whisker): meanN, sdN (δ15N in ‰); meanC, sdC (δ13C in ‰); all values negative for mean/differences where applicable.
- Isotopic extremes: dN15Max (maximum δ15N value across whisker segments).
- Notes: NA indicates no data available for that individual.

## Geographic and environmental processing
- Location data prioritized for standardization and comparability.
- 1 km buffers around carcass locations used to determine predominant land class (arable vs pastoral).
- OSGB36 coordinate reference system used for all spatial data.

## Data quality and usage notes
- NA indicates missing data for that individual.
- Column explanations accompany the data to support consistent interpretation across analyses.
- References the baseline work: McDonald et al. (1998) on anticoagulant rodenticides in stoats and weasels.

## Relation to environmental monitoring and policy
- Enables assessment of secondary exposure to second-generation anticoagulant rodenticides over time, by region and land-use context.
- Supports data standardization, quality assurance, and potential integration with other environmental datasets.
- Aims to increase data value by enabling broader analyses and access to underlying data for reuse and verification.