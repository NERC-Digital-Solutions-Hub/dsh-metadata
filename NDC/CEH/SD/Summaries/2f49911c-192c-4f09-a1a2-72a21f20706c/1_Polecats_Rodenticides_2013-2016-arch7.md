# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Purpose and context
- Data supplement to the paper on long-term increases in secondary exposure to anticoagulant rodenticides in European polecats in Great Britain (Sainsbury et al., 2018; Environmental Pollution).
- Column heading explanations for the CSV PolecatRodenticidesFINAL2013-2016March2019EIDC.csv, detailing data processed for analysis.

## Data structure and identifiers
- Batch information: batch, batch notes, and batch units; used to group chemical analyses.
- Sample and animal identifiers: record (unique animal identifier), collector.no (collecting institution identifier).
- Chemical analysis identifiers: # (sample number within batch).
- Multiple reference fields: NA indicates missing data; notes provide minimal context.
- Core references: McDonald et al. 1998 cited for related methodologies.

## Spatial data and geography
- Location coordinates: x (easting) and y (northing) coordinates in OSGB36 CRS (metres).
- Region classification: region (divided into North, South, East, West).
- Land cover context: carcass collection locations overlaid onto CEH Land Cover Map (2007); 1 km buffers applied to derive majority land class (primarily arable vs pastoral).
- Spatial attributes linked to collection points to support GIS analyses of habitat influence and exposure patterns.

## Temporal details
- Month and year of carcass collection.
- Season of collection: Spring (Mar–May), Summer (Jun–Aug), Fall (Sep–Nov), Winter (Dec–Feb).
- halfYear: FIRST (December–May) or SECOND (June–November) to capture seasonal variation.

## Biological and sampling information
- CoD: Cause of death (with NA when unknown).
- Demographics: sex (coded), age (coded or determined via cementum aging), alive (status/age), region-specific metadata.
- Condition metrics: fat (kidney fat score; 0–4 scale as per McDonald et al. 1998).

## Chemical exposure data (liver residues)
- Individual rodenticides measured: bromadiolone (brom), difenacoum (difs?), flocoumafen (floc), brodifacoum (brod), difethialone (dife).
- Reported as concentration in liver residue (µg/g); zero indicates non-detect.
- Detection flags: bRods (whether one or more rodenticides detected), bBrom, bDifm, bFloc, bBrod, bDife (whether specific compound detected; 1 = detected).
- Summary counts: cRods (number of rodenticides detected in the liver; 0–4), sumALL (total concentration of all detected rodenticides; units µg/g).
- Data quality/consistency flags: NA used where data are not available.

## Isotopic and biomarker information
- Isotopic measurements on whisker: meanN (mean δ15N), sdN (standard deviation of δ15N), meanC (mean δ13C), sdC (standard deviation of δ13C).
- dN15Max: maximum δ15N value across whisker segments tested for the animal.
- All isotope-related values are reported with appropriate units (‰ for isotopes); notes indicate values are negative where applicable.

## Data interpretation notes
- “NA” denotes missing data for a given individual.
- Land cover classification and 1 km buffer approach underpin habitat context around carcass collection sites.
- The dataset integrates chemical, spatial, temporal, and biological data to support analysis of secondary exposure to second-generation anticoagulant rodenticides in GB polecats.

## References
- McDonald, R.A., Harris, S., Turnbull, G., Brown, P., Fletcher, M. (1998). Anticoagulant rodenticides in stoats and weasels in England. Environmental Pollution, 103, 17-23.