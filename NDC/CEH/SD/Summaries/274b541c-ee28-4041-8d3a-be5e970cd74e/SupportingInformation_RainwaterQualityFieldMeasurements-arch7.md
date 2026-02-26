# Field measurements of alkalinity, chloride-ion, conductivity,   pH   and   nutrients   in   rainwater   (2004-2006) [LOCAR] LOCAR BASELINE DATASETS LOCAR

## Overview
- Rainwater chemistry data collected as part of the LOCAR programme to understand baseline conditions.
- 7 sampling sites across three catchments: Frome/Piddle (FP), Pang/Lambourn (PL), and Tern (TE) between 2004 and 2006.
- Data suitable for GIS analyses of spatial patterns in water quality and related parameters.

## Variables measured and units
- Alkalinity as CaCO3 (mg/l)
- pH (pH units)
- Ammonia (mg/l N)
- Chloride-ion (mg/l Cl)
- Conductivity at 20°C (µS/cm)
- Nitrate (mg/l N) [nitrate measured as NO3 and converted to N]
- Phosphorus soluble reactive (SRP) (mg/l P)
- Silicate reactive dissolved (SRD) (mg/l SiO2)
- Sulphate (mg/l SO4)

## Locations and sampling scheme
- Sites and catchments:
  - FP04 CEH Winfrith (Frome/Piddle catchment)
  - FP13 Higher Came Farm (Frome/Piddle)
  - FP35 Lower Wraxall Farm (Frome/Piddle)
  - PL06 Warren Farm (Pang/Lambourn)
  - PL11 Frilsham Meadow (Pang/Lambourn)
  - TE11 Helshaw Grange (Tern)
  - TE17 Oakley Folly (Tern)
- Site type: RNWQ (rainwater collector for water quality samples)
- Sampling frequency:
  - Fortnightly in Pang/Lambourn and Tern catchments
  - Roughly monthly in Frome/Piddle catchment
- Time period: January 2004 – May 2006
- Time data note: For FP catchments, sampling times were not recorded (represented as 00:00)

## Sampling and laboratory methods
- Field collection: Rainwater collectors brought to the lab; samples allocated to bottles (pH/alkalinity in glass; SRP filtered; others unfiltered).
- Analysis by Thames Water; samples sent from Catchment Service Teams.
- Analytical methods (examples):
  - Chloride, Sulphate, Nitrate, SRD, SRP: Seal discrete analyser
  - Ammonia: Seal discrete analyser
  - pH: pH electrode
  - Conductivity: Conductivity electrode
  - Alkalinity: Seal discrete analyser
- Data quality indicators:
  - Reported mean concentration (%), method consistency, and limits of detection (LOD) provided per parameter.
  - Nitrate concentration converted from NO3 to N using a standard factor (X*14/64).

## Data quality and quality assurance
- Thames Water performed QA on all data.
- Weekly: duplicate and a QC sample were processed to verify laboratory results.
- Data for FP catchments lack precise time stamps; 00:00 used as a placeholder.
- Box-and-whisker plots generated to show range, median, quartiles, and outliers for all variables.

## GIS usage notes
- Spatial analysis potential:
  - Map concentration patterns across the 7 sites and three catchments.
  - Compare temporal trends (fortnightly vs. monthly) where time is available.
- Data considerations:
  - Be aware of missing time data for FP sites.
  - Consider measurement uncertainties and LODs when creating maps or performing interpolations.
  - Units and parameter conversions (e.g., nitrate to nitrogen) required for consistent visualization.