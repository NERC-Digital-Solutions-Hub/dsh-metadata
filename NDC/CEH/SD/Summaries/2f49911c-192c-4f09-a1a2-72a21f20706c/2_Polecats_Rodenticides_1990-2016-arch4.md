# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain. Column heading explanations for PolecatRodenticidesFINAL1990-2016March2019EIDC.csv

## Purpose and context
- Data supplement to the paper on long-term increase in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain.
- Documents column headings and data provenance for the PolecatRodenticidesFINAL1990-2016March2019EIDC.csv dataset.
- Supports assessment of temporal and spatial patterns of secondary rodenticide exposure in GB polecats and enables data reuse for policy and management discussions.

## Data structure and key variables
- record: unique animal identifier issued by the Vincent Wildlife Trust.
- data: origin of chemical analyses data; NEW = Sainsbury et al. 2016; OLD = Shore et al. 2003.
- year: year of carcass collection (1990–2016).
- time: time since first animal was collected (in years).
- survey: which survey round (ONE = 1990–1995; TWO = 1995–1998; THREE = 2013–2016).
- season: season of carcass collection (Spring, Summer, Fall, Winter).
- halfYear: half-year period of collection (FIRST = December–May; SECOND = June–November).
- x, y: spatial coordinates (metres) in OSGB36 coordinate reference system.
- region: broad collection region (North, South, East, West).
- expansio n: inside or outside the 1990s range (IN/OUT).
- landClas s: predominant land use at the collection location, determined by overlaying carcass points on the CEH Land Cover map (2007) with 1 km buffers; classifies land as arable or pastoral (updated via majority class).
- hBrom: concentration of bromadiolone in liver (µg/g); detection status derived from LODs from Shore et al. 2003 (applied to 2018 dataset).
- hDifm: concentration of difenacoum in liver (µg/g); detection status as above.
- hBrod: concentration of brodifacoum in liver (µg/g); detection status as above.
- hBBrom, hBDifm, hBBrod: detection indicator for each compound (0 = none detected; 1 = detected; LOD-based).
- hBRods: number of rodenticides detected in the liver (0, 1, 2, or more).
- hCRods: coded value for the number of rodenticide compounds detected (1 = one; 2 = two; 3 = three; with LOD adjustments).
- hConcT: total concentration of rodenticide compounds detected (µg/g) in the liver (2018 dataset; LODs from Shore et al. 2003).
- NA: indicates missing data for the individual field.
- Notes: data provenance and standardization remarks; LOD imputation details referenced to Shore et al. 2003 and applied to the 2018 dataset.

## Data provenance, processing, and standards
- Data origins: Shore RF et al. (2003) and Sainsbury KA et al. (2018) underpin the dataset.
- LOD handling: limits of detection from Shore et al. 2003 applied to the 2018 dataset for consistency.
- Spatial processing: carcass locations overlaid onto CEH Land Cover map (2007); 1 km buffers created; majority land class (arable vs pastoral) used as landClas s.
- Coordinate reference: OSGB36 CRS (x, y in metres).
- Data integration: consolidates two historical data sources (OLD and NEW) into a harmonized schema with consistent variable definitions and units.
- Analytical context: dataset forms part of long-term assessments of secondary exposure to anticoagulant rodenticides in GB polecats.

## Temporal and spatial coverage
- Temporal range: carcass collection from 1990 to 2016.
- Spatial scope: Great Britain; regional classification into North, South, East, West based on collection location.

## Data quality, limitations, and usage notes
- Missing data: many fields may be NA where information was not recorded.
- Detection data depend on historical LODs; combined with newer dataset using Shore et al. 2003 standards.
- Land use classification relies on 2007 land cover data and 1 km buffers, which may not reflect microhabitat variation.
- One dataset integrates analyses from two source studies; users should be aware of potential source-related differences prior to harmonization.
- Designed to support longitudinal trend analysis and cross-study comparisons, with metadata to aid traceability and reuse.

## References
- Shore RF, Birks JDS, Afsar A, et al. (2003). Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats (Mustela putorius) from throughout their range in Britain, 1992–1999. Environmental Pollution, 122, 183-193.
- Sainsbury KA, Shore RF, Schofield H, et al. (2018). Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution, 236, 689-698.