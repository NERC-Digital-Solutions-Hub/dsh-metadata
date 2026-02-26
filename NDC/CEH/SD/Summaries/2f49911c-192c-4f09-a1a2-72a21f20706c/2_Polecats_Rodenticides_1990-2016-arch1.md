# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Supplementary dataset to the 2018 Environmental Pollution paper on long-term increases in secondary exposure to anticoagulant rodenticides in British polecats.
- Collected data (1990–2016) from three rodenticide surveys, with chemical analyses of liver residues for three compounds and related metrics.
- Enables analysis of spatial, temporal, and environmental patterns of exposure in European polecats in Great Britain.

## Data structure and key variables
- Record-level identifiers and provenance:
  - record: unique animal identifier.
  - data: origin of chemical analyses (NEW = Sainsbury et al. 2016; OLD = Shore et al. 2003).
  - year/time/survey/season/halfYear: temporal metadata, with surveys defined as ONE (1990–1995), TWO (1995–1998), THREE (2013–2016); seasons and halves indicate timing within year.
  - region: broad geographic region (North, South, East, West).
  - expansio n: inside or outside the 1990s range (IN/OUT).
  - x/y: OSGB36 coordinates (metres) for collection locations.
  - landClas s: predominant land cover at the location, derived from CEH Land Cover Map 2007 using 1 km buffers and majority classification between arable and pastoral.
  - sex: biological sex when known.
- Chemical analysis metrics (all liver residue or detection indicators):
  - hBrom, hDifm, hBrod: concentrations of bromadiolone, difenacoum, brodifacoum (µg/g); LODs applied from Shore et al. 2003 for the 2018 dataset.
  - hBBrom, hBDifm, hBBrod: detection flags (0 = none detected; 1 = detected).
  - hBRods: number of rodenticide compounds detected (0, 1, 2, or 3; 0 = none detected; LOD-derived).
  - hCRods: total number of rodenticide compounds detected (1, 2, or 3).
  - hConcT: total concentration of rodenticide compounds (µg/g; LODs applied for the 2018 dataset).
- Data origin and notes:
  - Notes indicate data gaps (NA) where data were not available for an individual.
  - Land cover classifications generated using Quantum GIS; carcass coordinates overlaid on the CEH Land Cover Map (2007).
  - hConcT and detections reflect layer from Shore 2003 and applied to the Sainsbury 2018 dataset.

## Data sources, timeline, and scope
- Primary references:
  - Shore RF et al. 2003: Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats across Britain (1992–1999).
  - Sainsbury KA et al. 2018: Long-term increase in secondary exposure to anticoagulant rodenticides in British polecats.
- Timeframe:
  - Carcass collection and analyses span 1990–2016.
  - Three surveys correspond to periods: 1990–1995, 1995–1998, and 2013–2016.
- Analysis scope:
  - Combines data from two analyses (2003 and 2016/2018 datasets) to enable longitudinal assessment of exposure trends.

## Geographic and environmental processing
- Location data:
  - Coordinates provided in OSGB36 with x (easting) and y (northing) values.
  - Region categorisation into North, South, East, West.
- Land cover assignment:
  - 1 km buffers around carcass coordinates; majority land class determined by comparing arable versus pastoral land cover using CEH Land Cover Map 2007.
  - Land class used to assess environmental context of exposure.

## Analytical considerations and potential uses
- For analysts aiming to identify correlations and predict exposure:
  - Examine temporal trends in hConcT and detection rates across surveys and time periods.
  - Explore regional differences (North/South/East/West) and associations with land cover type (arable vs pastoral).
  - Assess seasonality and within-year timing (season, halfYear) of detected exposures.
  - Analyze the number of rodenticides detected (hBRods, hCRods) as a measure of exposure burden.
  - Compare data sources (OLD vs NEW) and harmonize LOD imputation with Shore 2003 methods for cross-year comparability.
- Data quality and harmonisation:
  - LODs applied from Shore 2003 to 2018 dataset; interpret nondetects and detections accordingly.
  - Potential gaps where data were not available (NA); some variables may be incomplete (e.g., sex, precise land class for all records).
  - Ensures traceability by listing data provenance and keeping a record-level identifier for reproducibility.

## Practical notes and limitations
- Data integration challenges addressed by standardising units (µg/g) and converting detection to binary where appropriate.
- Spatial resolution constrained by 1 km land-cover overlay and the accuracy of carcass collection locations.
- Temporal gaps exist due to survey intervals; long-term inferences rely on the three defined survey periods.
- LOD imputation methods are consistent with the cited Shore 2003 approach for comparability.

## References
- Shore RF, Birks JDS, Afsar A, Wienburg CL, Kitchener AC (2003) Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats (Mustela putorius) from throughout their range in Britain, 1992-1999. Environmental Pollution 122, 183-193.
- Sainsbury KA, Shore RF, Schofield H, Croose E, Pereira MG, Sleep D, Kitchener AC, Hantke G, McDonald RA (2018) Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution 236, 689-698.