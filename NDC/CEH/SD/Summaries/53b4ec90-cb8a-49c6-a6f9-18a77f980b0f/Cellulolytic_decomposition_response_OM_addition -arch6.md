# Cellulolytic decomposition of Welsh upland rivers in response to organic matter addition

## Overview
- Field BACI study assessing how adding leaf litter influences cellulose-decomposition, using tensile strength of calico strips as the primary metric.
- Experimental design splits each stream into an upstream reference zone and a downstream experimental zone with ~20–50 m separation to ensure independence.
- Before period (T1) ran ~61–65 days (Nov 2012–Jan 2013) with no manipulation; after period (T2) ran ~57–62 days (Jan–Mar 2013) during which leaf litter was added to the experimental zone.
- Leaf litter addition consisted of one tonne bags of oak, birch, and alder leaves; litter was distributed by zone area and maintained a minimum wet weight of 1.7 kg m^-2; additional 630 kg (wet weight) of leaf litter was added on two storm-event days (Feb 12 and Mar 5, 2013).

## Experimental design and timing
- Units: Six experimental units (cotton/calico strips) per reach; strips were deployed before and after manipulation.
- Sampling periods:
  - T1 (Before): 61–65 days, no manipulation; both reference and experimental zones treated equally.
  - T2 (After): 57–62 days; experimental zone received leaf litter additions.
- Material addition and placement: Leaf litter added above the experimental zone and below the reference zone; litter packs reflected naturally occurring leaf packs.

## Data collection and measurements
- Tensile strength measurement: Calico strips collected at end of T1 and T2, frozen at -20°C, then dried (65°C) and tested with a Hounsfield machine (25 kN load cell, 40 mm test gap) to obtain one breaking strain estimate per strip.
- Controls: Three untreated strips used as transport/wash controls.
- Primary data collected per strip: breaking_strain (Newtons) and %_loss (percent loss of tensile strength relative to the control batch).

## Data structure and content
- Data files: Flatbed comma-separated values (CSV).
- Main data columns (10): 
  - site_code (sampling site)
  - region (stream basin)
  - date (sampling date)
  - time (Before or After manipulation)
  - landuse (basin land-use)
  - reach (Experimental or Control site)
  - replicate (replicate code, A–F)
  - exposure (days exposed)
  - breaking_strain (Newtons)
  - %_loss (percent loss relative to control)
- Supporting metadata: DURESS_CU_site_description.csv with 10 fields including:
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey and Catchment information (WAWS/Welsh Acid Water Survey, Plynlimon catchment, etc.)

## Analytical methods and quality control
- Analytical approach: Laboratory tensile testing of calico strips after field deployment to quantify decomposition proxy.
- Instruments: Hounsfield tensile tester; 25 kN load cell; 40 mm test gap.
- Quality control: No explicit QC steps described beyond the use of three untreated control strips to account for transport/wash effects; no additional calibration steps recorded.

## Data interpretation and potential uses
- Enables comparison of cellulolytic decomposition before vs after leaf-litter addition, across experimental and control reaches, and across sites.
- Facilitates assessment of how organic matter inputs influence breakdown rates in upland Welsh streams.
- Data can be used to explore relationships between exposure (days), site characteristics (region, land use), and observed tensile-strain loss.

## Accessibility and provenance
- Data description references external literature; links provided in the documentation (subject to link stability).
- Data are intended for inclusion in the CEH Data Catalogue; actual link stability may vary.