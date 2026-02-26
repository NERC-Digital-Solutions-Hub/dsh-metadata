Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain

## Overview
- Dataset accompanying the paper on long-term increases in secondary exposure to anticoagulant rodenticides in GB polecats (Sainsbury et al. 2018; Environmental Pollution).
- Supplemental data file: PolecatRodenticidesFINAL2013-2016March2019EIDC.csv.
- Contents: chemical analysis results, carcass metadata, demographic info, location data, land-use context, and isotopic measurements for polecats collected 2013–2016.

## Data structure and key variables
- Chemical residue data (liver concentrations in µg/g): brom (bromadiolone), difm (difenacoum), floc (flocoumafen), brod (brodifacoum), dife (difethialone); with corresponding detection flags:
  - bBrom, bDifm, bFloc, bBrod, bDife (presence/absence of each compound)
  - cRods: number of rodenticides detected (0–4)
  - sumALL: total concentration of detected rodenticides (µg/g)
- Other carcass/biological data:
  - record, Batch (chemical analysis batch), CoD (cause of death), month, year, season, halfYear
  - region (North, South, East, West)
  - landClass: predominant land use around collection site (derived from CEH Land Cover map 2007)
  - resistance: indication if collected from an area with known resistance to SGARs (categories 0/1/2/3 as per dataset)
  - sex, age, alive, fat (condition scoring)
- Isotopic and biomarker data:
  - meanN, sdN (δ15N in whisker, per animal)
  - meanC, sdC (δ13C in whisker, per animal)
  - dN15Max (maximum δ15N value across whisker segments)
- Location and spatial context:
  - x, y: easting and northing coordinates in OSGB36
  - region and landClass contextual metadata
- Data quality indicators:
  - NA entries indicate missing data; notes explain interpretation of missing fields
  - Some values (e.g., δ15N) are noted as negative

## Collection, processing, and context
- Sample scope: European polecats in Great Britain, carcasses collected 2013–2016.
- Location processing:
  - carcass locations overlaid onto CEH Land Cover map (2007)
  - 1 km buffers created around each carcass
  - majority land class within buffer (between arable and pastoral) used as landClass
- Coordinate system: OSGB36; x and y provide precise collection-site positioning
- Data provenance:
  - Supplement to the 2018 Environmental Pollution paper
  - References include McDonald et al. (1998) for context on anticoagulant rodenticides in mustelids
  - Data collection and sharing linked to Vincent Wildlife Trust records (record and collector identifiers)

## Intended use and analytical considerations
- Primary aim: support analyses of secondary exposure to second-generation anticoagulant rodenticides, including temporal trends, geographic patterns, and associations with land use, pesticide resistance areas, and demographic factors.
- Potential analyses:
  - Correlations between liver concentrations (brom, difm, floc, brod, dife) and region, landClass, resistance status, season, or age/sex
  - Patterns in the number of compounds detected (cRods) and total burden (sumALL)
  - Relationship between isotope biomarkers (δ15N, δ13C) and rodenticide exposure
  - Spatial and temporal trends across 2013–2016
- Cautions:
  - Missing data (NA) in several fields; require careful handling and transparent reporting
  - δ15N values are negative; interpret within the context of biomarker limitations
  - Derived variables (landClass, resistance) depend on external datasets and processing steps (e.g., 1 km buffers, land cover mapping)

## References and provenance
- Supplementary dataset for: Sainsbury KA, Shore RF, Schofield H, et al. (2018). Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution, 236: 689-698.
- Related methodological and background references:
  - McDonald, R.A., Harris, S., Turnbull, G., et al. (1998). Anticoagulant rodenticides in stoats and weasels in England. Environmental Pollution.
  - CEH Land Cover Map 2007 (for landClass derivation)
  - Vincent Wildlife Trust data provenance (record/collector identifiers)