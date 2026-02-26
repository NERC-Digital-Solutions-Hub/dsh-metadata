# Overview

- Aim: A dataset documenting the seasonal abundance of Culex pipiens across life stages at the CEH Wallingford site, to support environmental health monitoring and policy performance assessments over time.

- Field site and sampling design:
  - Immature stages (eggs, larvae, pupae) monitored three times per week from March to October 2015 using four 450 L circular water butts placed close together at the Wallingford site.
  - Butt locations varied in sun exposure and shelter; a hay infusion was created in January–March.
  - A HOBO water temperature logger recorded hourly surface water temperatures in each butt.
  - Egg rafts counted at 10 am on Mondays, Wednesdays, and Fridays; dips (500 ml) taken from north, south, east, and west edges (not the middle) for larval/pupal counts.
  - Larvae/pupae counted in the field when feasible; otherwise photographed and counted later using Microsoft Paint. 4th instar larvae were taken monthly for species-level identification via microscopy.
  - Adults sampled with four John W. Hock UV traps baited with dry ice, run nightly from April 14 to October 2 (with some nights missed). Traps located in trees and field margins at distances from the butts; only females were identified and counted.

- Data collection and instruments:
  - Traps: UV light traps (dry ice bait) linked to field locations around the water butts.
  - Identification: Laboratory microscopy and standard dissection techniques.
  - Temperature: Hourly surface water temperatures per butt.

- Nature and units of recorded values:
  - Eggs: counts of egg rafts, by butt.
  - Larvae/Pupae: counts by sampling occasion, by butt, with separate counts for 1st/2nd instars (L1/2) and 3rd/4th instars (L3/4).
  - Adults: counts of female Cx. pipiens (and other species) per trap per sampling occasion; males not recorded.
  - Temperature: degrees Celsius.

- Quality control:
  - Counting validated by comparing photo-based counts with direct tray counts on the first two days; consistency observed.
  - Some NA entries where traps could not be run due to staffing or dry ice issues.

- Nature of data and structure:
  - Six CSV spreadsheets:
    - Egg_abundance_2015_Wallingford.csv: date and butt number (1–4) per count.
    - Larval_abundance_2015_Wallingford.csv and Pupal_abundance_2015_Wallingford.csv: date plus cornered sampling counts (N,E,S,W) for each butt; larval (L1/2, L3/4) and pupal counts separated.
    - Adult_abundance_2015_Wallingford.csv: date, trap location, and counts for Cx. pipiens and other species (Cs. annulata, Ae. geniculatus) per trap; NA where unavailable.
    - Larval_identification_2015_Wallingford.csv: dates of 4th instar identifications, counts identified as Cx. pipiens, and butt origin.
    - Water_temperatures_2015_Wallingford.csv: hourly water temperatures by butt with date and time.
  - File contents indicate the specific data structure and columns used for each dataset, aligned with the sampling regime described.

- Additional context and notes:
  - Field site coordinates and figure references describe locations of butts and traps relative to the weather station.
  - Some sampling occasions include NA due to operational issues.
  - Data are organized to support cross-comparison across life stages, space (butts), and time, enabling integration with environmental or policy analyses.