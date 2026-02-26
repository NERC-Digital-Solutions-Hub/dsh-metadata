# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Supplement to the 2018 Environmental Pollution paper on long-term increases in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain.
- CSV dataset (PolecatRodenticidesFINAL2013-2016March2019EIDC.csv) contains chemical analysis data and associated metadata for polecat samples collected 2013–2016.
- Linked to the broader study context of SGAR exposure in GB; includes identifiers, collection details, location context, and multi-chemical residue measurements.

## Data structure and fields
- Batch-level metadata: batch, units, notes; sample numbering within batches.
- Sample identifiers: record (unique database ID), collector.no (National Museums Scotland ID).
- Biological and collection details: CoD (cause of death), month, year, season, halfYear (seasonal half), region (North/South/East/West), sex, age, alive, fat score.
- Spatial context: x (easting), y (northing) in OSGB36 coordinates; landClass (land use classification derived from CEH Land Cover map 2007) with 1 km buffer overlays to determine predominant land class (arable vs. pastoral emphasis).
- Resistance context: resistance (area with known resistance to SGARs in rodents).
- Chemical measurements in liver residues: brom, difm, floc, brod, dife (concentration units in µg/g); with corresponding binary detection flags (bRods, bBrom, bDifm, bFloc, bBrod, bDife) indicating presence/absence; cRods indicates number of rodenticides detected (1–4); sumALL (total concentration of rodenticides) and related notes.
- Isotopic and trophic data: meanN, sdN (δ15N values in ‰); meanC, sdC (δ13C values in ‰); dN15Max (maximum δ15N across whisker segments).
- Data completeness: NA used to denote missing data (as specified in the notes).

## Data provenance and collection
- Timeframe: carcass collection 2013–2016 across Great Britain.
- Collected data types include chemical residues (SGARs) and isotopic analyses, as well as extensive contextual metadata (location, land use, sex/age, etc.).
- Data sources cited for methodology: primary references include McDonald et al. (1998) for isotopic methodologies; the data underpin the 2018 polecat SGAR exposure paper.

## Measurements and units
- Chemical residues (rodenticides) reported as concentration in micrograms per gram (µg/g).
- Isotopic data reported in per mil (‰) for δ15N and δ13C.
- Spatial coordinates: OSGB36 grid system (meters) for x and y.
- Land class and region provided as categorical descriptors; season and half-year provide temporal context.

## Spatial and environmental context
- Location data includes region (North/South/East/West) and precise coordinates.
- Land use classification derived from CEH Land Cover map (2007); land class determined within 1 km buffers around carcass collection points.
- Environmental context supports analyses of exposure relative to land cover types and geographic regions.

## Data quality, completeness, and limitations
- Extensive field-level coding with predefined categories (1/2/3) and many NA values.
- Dependence on external datasets (CEH Land Cover, OSGB36 coordinates) and historical collection practices; potential variability in data collection and recording across institutions.
- Some fields indicate possible lack of data (NA), which may limit certain analyses (e.g., isotopic or lipid-related measurements for some individuals).
- Reference framework provided (Sainsbury et al. 2018; McDonald et al. 1998) to support interpretation and comparability.

## Usage notes and governance
- Data are structured with persistent identifiers (record, collector.no) to support traceability and data linkage.
- Explicit metadata explanations accompany each field, aiding discoverability and correct interpretation.
- Suitable for analyses of temporal trends, geographic patterns, and multi-chemical exposure in GB polecats; enables assessment of co-occurrence with land use and resistance-area contexts.
- For proper reuse, consult the 2018 Environmental Pollution paper and the referenced methodological literature.

## References
- Sainsbury KA, Shore RF, Schofield H, Croose E, Pereira MG, Sleep D, Kitchener AC, Hantke G, McDonald RA (2018) Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution, 236:689-698.
- McDonald, R.A., Harris, S., Turnbull, G., Brown, P., Fletcher, M. (1998) Anticoagulant rodenticides in stoats and weasels in England. Environmental Pollution, 103, 17-23.