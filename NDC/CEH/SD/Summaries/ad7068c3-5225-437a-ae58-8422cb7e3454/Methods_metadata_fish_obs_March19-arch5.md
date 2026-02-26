# Methods, metadata and summary for fish monitoring at Akrotiri up to 22 nd March 2019 (IJW)

## Project and organisations
- Part of Defra Darwin Initiative Plus Project DPLUS056: Assessment and monitoring of current and future IAS in Cyprus to establish baseline data on native and non-native fish in the Sovereign Base Area of Akrotiri.
- Organisations involved: Centre for Ecology & Hydrology (CEH), Joint Services Health Unit, Akrotiri Environmental Education Centre, Water Development Board of Cyprus.

## Methods
- Primary sampling method: baited mesh traps (55 x 24 x 24 cm; 3 mm mesh) baited with halibut pellets.
- Trial and deployment: after exploratory trials with underwater video, two trap configurations deployed for ~24 hours.
  - Submerged: inshore, bottom, depth up to ~1 m.
  - Semi-submerged: trap openings span the water surface in extreme inshore locations.
- Handling: captured fish transferred in water to shallow trays, identified, sexed (as obvious males), then released back to capture water body.
- Sampling locations and timeline:
  - 9 water bodies: 6 pools (P1–P6) and 3 channels (C1–C3).
  - Sampling occurred in late Feb–early Mar 2018; regular monitoring at ~2-week intervals at P1 and C2 until Jan 2019.
  - P1 location moved from P1 Bay to P1 Main due to water level changes.
- Environmental data: location recorded with Garmin GPSMAP 62s.
  - Measurements on all visits (26 Feb 2018 – 25 Jan 2019): water temperature, dissolved oxygen (% and μg/L), conductivity (μS/cm) using YSI Pro30.
  - Comparative conductivity measurement in adjacent sea on 27 Feb 2018.
  - Temperature-only measurements 7 Mar 2019 – 22 Mar 2019.
- Additional surveys: two bottom-set CEN standard nets at largest pool (P1) on 27 Feb 2019; day-time visual fish surveys at P1 and channels C4–C6 (26 Feb – 1 Mar 2019).

## Data and metadata
- Data files (CSV) and descriptions:
  - Akrotiri_aquatic_environment_26_2_18_22_3_19: sampling site locations and environmental measurements.
  - E Akrotiri_fish_26_2_18_22_3_19: all fish observations.
  - Akrotiri_fish_26_2_18_22_3_19: all trap observations (some entries with zero fish).
- Data structure and fields:
  - Environment: Date, Time, Site_code, Site_full_name (including natural or refuge population of Aphanius where applicable), Lat_(N), Lon_(E), Temp (°C), DO_per (%), DO (μg/L), Cond (μS/cm).
  - Fish observations: Date, Site_code, Trap_Type (SUBM = Submerged, SEMI = Semi-submerged), Trap_number, Species (Aphanius fasciatus or Gambusia holbrooki), Sex (M indicated; otherwise not obvious), Length (fork length in mm).
  - Traps observations: Date, Site_code, Trap_Type, Trap_number, Aphanius (count), Gambusia (count), Total (Aphanius + Gambusia).

## Data quality and limitations
- Quality assurance: data and protocols were developed by a CEH staff member with >25 years of relevant experience; all incoming data reviewed and digitised by this person.
- Missing data:
  - Equipment failures caused missing aquatic environmental data after 25 Jan 2019.
  - A thermometer replacement occurred from 7 Mar 2019 onward.
  - Missing data on 28 Feb 2018 for P1 Main; P1 Bay (26 Feb 2018) near P1 Main; differences considered unlikely significant.
- Documentation notes: data are accompanied by site codes, full site names, and population designations to aid interpretation and reuse.

## Practical considerations for data stewardship
- Clear temporal and spatial tagging (date, time, GPS coordinates) supports longitudinal analyses and inter-site comparisons.
- Metadata explains trap configurations and species identifications, supporting reproducibility and data reuse.
- Standardized data formats and explicit field definitions facilitate interoperability across datasets and with other monitoring programs.