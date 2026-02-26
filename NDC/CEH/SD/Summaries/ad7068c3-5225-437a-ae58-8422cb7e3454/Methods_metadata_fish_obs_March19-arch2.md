# Methods, metadata and summary for fish monitoring at Akrotiri up to 22 nd March 2019 (IJW)

## Overview and purpose
- Part of Defra Darwin Initiative Plus Project DPLUS056: Assessment and monitoring of current and future IAS in Cyprus to establish baseline data on native and non-native fish populations in the Sovereign Base Area of Akrotiri.
- Aimed at producing standardized, QA’d data to support baseline assessments of environmental health and policy-relevant monitoring over time.

## Project and organisations
- Sampling conducted by:
  - Centre for Ecology & Hydrology (CEH)
  - Joint Services Health Unit
  - Akrotiri Environmental Education Centre
  - Water Development Board of Cyprus

## Monitoring design and study area
- Nine water bodies sampled: six pools (P1–P6) and three channels (C1–C3).
- Sampling window: late February–early March 2018, with follow-up monitoring at ~2-week intervals for:
  - P1 (pool) and C2 (channel)
  - Extended period up to January 2019; P1 moved from P1 Bay to P1 Main due to falling water levels.
- Additional surveys: bottom-set CEN nets deployed overnight at the largest pool (P1) on 27 February 2019; daytime visual surveys at P1 and channels C4–C6 between 26 Feb and 1 Mar 2019.

## Methods: fish capture and handling
- Primary gear: baited mesh traps (A25; 55 × 24 × 24 cm; 3 mm mesh) baited with a halibut pellet.
- Trap configurations:
  - Submerged: traps placed on the water body bottom inshore, depth up to ~1 m.
  - Semi-submerged: traps positioned so openings span the water surface at extreme inshore location.
- Procedure: traps deployed for ~24 hours; captured fish were measured, sexed (as obvious males), and released alive back to capture water body.
- Additional surveys: daytime visual assessments of fish in P1 and other channels.

## Environmental measurements and timing
- Location recorded with Garmin GPS on first visit; precise site codes and full names noted.
- In situ water properties (Feb 26, 2018–Jan 25, 2019): temperature, dissolved oxygen (% and μg/L), and conductivity (μS/cm).
- Comparative measurement: conductivity also recorded in adjacent sea on Feb 27, 2018.
- Temperature-only measurements: conducted from Mar 7, 2019 to Mar 22, 2019.

## Species observed
- Aphanius fasciatus (Mediterranean killifish) and Gambusia holbrooki (Eastern mosquitofish).
- For captured fish: sex (male indicated when obvious) and fork length (mm) recorded.

## Data products and structure
- Metadata and data stored in three CSV files:
  - Akrotiri_aquatic_environment_26_2_18_22_3_19: site location and environmental measurements
    - Columns include: Date, Time, Site_code, Site_full_name, Lat_(N), Lon_(E), Temp, DO_per, DO, Cond
  - Akrotiri_fish_26_2_18_22_3_19: fish observations
    - Columns include: Date, Site_code, Trap_Type (SUBM = Submerged, SEMI = Semi-submerged), Trap_number, Species (Aphanius or Gambusia), Sex, Length
  - Akrotiri_traps_26_2_18_22_3_19: traps observations
    - Columns include: Date, Site_code, Trap_Type, Trap_number, Aphanius, Gambusia, Total
- Trap and fish data capture notes:
  - Species abbreviations: Aphanius fasciatus (Aphanius); Gambusia holbrooki (Gambusia)
  - Length: Fork length (mm)

## Data quality assurance and provenance
- QA/QA: All equipment and protocols designed and led by an experienced CEH staff member with >25 years of relevant experience; all data reviewed and digitised by that person.
- Training: Local organisation staff received specific training as part of the field work.
- Data management: Datasets intended to be stored and uploaded to appropriate data portals.

## Data gaps and limitations
- Missing data largely due to equipment failure after 25 Jan 2019 (thermometer replacement post-7 Mar 2019 helped recover some data).
- Gaps include missing data for 28 Feb 2018 at P1 Main; P1 Bay data from 26 Feb 2018 exist but are from a nearby site and assumed comparable due to proximity.
- Conductivity measurements exclude some late-event dates; temperature-only data available post-March 2019.

## Relevance for ongoing monitoring and analysis
- Provides a standardized, QA’d dataset linking environmental conditions with fish presence and community composition across multiple habitats.
- Structured for integration into reports, maps, and time-series analyses to assess environmental health and policy performance over time.
- Datasets are designed to be reusable and comparable with other monitoring efforts, supporting broader environmental monitoring goals and data sharing.