# Methods, metadata and summary for fish monitoring at Akrotiri up to 22 nd March 2019 (IJW)

## Overview and aim
- Part of Defra Darwin Initiative Plus Project DPLUS056: assessment and monitoring of current and future IAS in Cyprus to establish baseline data on native and non-native fish populations in the Sovereign Base Area of Akrotiri.

## Organisations involved
- Centre for Ecology & Hydrology (CEH)
- Joint Services Health Unit
- Akrotiri Environmental Education Centre
- Water Development Board of Cyprus

## Data assets and structure
- Metadata and observations collected and stored in CSV spreadsheets:
  - Akrotiri_aquatic_environment_26_2_18_22_3_19: sampling site locations and environmental measurements
  - Akrotiri_fish_26_2_18_22_3_19: all fish observations
  - Akrotiri_traps_26_2_18_22_3_19: traps observations
- Data fields and formats are specified within each file, including:
  - Spatial data: site codes, full site names, latitude/longitude
  - Environmental measurements: water temperature (°C), dissolved oxygen (% and μg/L), conductivity (μS/cm)
  - Biological observations: species (Aphanius fasciatus, Gambusia holbrooki), sex (where evident), fork length (mm)
  - Trap-specific records: trap type (Submerged or Semi-submerged), trap number, counts per species, totals

## Methods and sampling design
- Trapping method:
  - Baited mesh traps: 55 x 24 x 24 cm, 3 mm mesh, baited with halibut pellet
  - Two configurations:
    - Submerged: inshore, bottom, ~1 m depth
    - Semi-submerged: openings span water surface
  - Deployment: ~24 hours per session
  - Locations: 9 water bodies (P1–P6 pools, C1–C3 channels); additional P1 Bay and P1 Main due to dropping water levels
- Additional sampling:
  - Two CEN (European Standard) nets deployed overnight at the largest pool (P1) on 27 Feb 2019
  - Day-time visual fish surveys at P1 and channels C4–C6 (26 Feb–1 Mar 2019)
- Data collection protocol:
  - On retrieval, fish transferred in water to shallow trays, identified, sexed if obvious, and returned
  - All site locations recorded with GPS (Garmin GPSMAP 62s)
- Environmental and physical context:
  - Measured at each visit: water temperature, dissolved oxygen (percent and μg/L), conductivity
  - Temperature also measured with a secondary instrument from 7 Mar 2019 to 22 Mar 2019
  - Comparative conductivity measurements in adjacent sea on 27 Feb 2018

## Species monitored
- Mediterranean killifish (Aphanius fasciatus)
- Eastern mosquitofish (Gambusia holbrooki)

## Data quality, governance and metadata
- Quality assurance and control:
  - Data collection protocols and equipment developed by an experienced CEH staff member (>25 years)
  - Initial field work and staff training provided to local collaborators
  - All data entries reviewed and digitised by CEH personnel
- Data accessibility and documentation:
  - Clear column definitions and naming conventions in the CSV files to support discoverability and reuse
  - Site naming includes natural vs. refuge population notes where applicable

## Coverage, timing and updates
- Sampling window: late February 2018 to late January 2019 (environmental and fish data), with ongoing observations into March 2019
- Revisit interval: approximately every 2 weeks at P1 and C2 during the monitoring period
- Site movement: P1 Bay to P1 Main relocation due to water level changes; other sites tracked within same water body

## Data gaps and limitations
- Missing environmental data due to equipment failure after 25 Jan 2019 (thermometer missing after 7 Mar 2019; DO and conductivity meters largely unaffected)
- A data gap on 28 Feb 2018 for P1 Main
- P1 Bay data considered not unlikely to differ significantly from P1 Main due to proximity

## Practical implications for data management
- The three primary CSV files provide a coherent, linked dataset for spatial, environmental, and biological observations, enabling cross-table querying by site, date, trap configuration, and species
- Metadata supports data discoverability, re-use, and potential integration with broader environmental monitoring datasets
- Data gaps highlight the importance of instrument redundancy and ongoing data validation to maintain a complete time series for policy and management analyses