# Supporting Documentation

- Sediment trapping using sequencing traps was conducted at Rostherne Mere from January 2011 to January 2017.
- Two 12-bottle sequencing traps (Technicap PPS 4/3) were deployed at 10 m and 25 m depths to collect sediment over ~2-week periods (longer periods in Jan–Feb). Traps were reset ~every 6 months.
- Samples were kept cool, dark, and sealed during transport and stored frozen before analysis.
- Freeze-dried trap sediment was prepared for diatom analysis using standard peroxide digestion methods, with microspheres added for absolute quantification of diatoms.
- Diatom counting followed established protocols, including assessment of valve breakage and dissolution (F index). Counts continued beyond 300 diatoms to reach 100 microspheres when necessary.
- Diatom biovolume was calculated for taxa exceeding 3% abundance, using standard biovolume methods and a mean figure derived from 25 representative slides.
- Environmental context for interpretation included:
  - Daily air temperature (2 m above water) and water temperatures at 12 depths (2–24 m) from the UKLEON buoy.
  - Relative resistance to thermal mixing (RTRM) calculated from temperature/density profiles.
  - Wind speed data corrected for local sheltering (VRM) using nearby meteorological data (UKLEON buoy data used where available; Manchester Airport data used otherwise).
- Recorded data types include temperature, wind, RTRM, trap type, dates, diatom counts and dissolve percentages, diatom biovolume, total diatom abundance, breakage/dissolution metrics, and sediment flux metrics.

## Data and Variable Details

- Nature and Units of Recorded Values
  - Temperature: degrees Celsius (°C)
  - Wind: meters per second (m/s)
  - RTRM: numeric resistance value

- Data Structure
  - RMTemperatures.csv
    - 16 columns (A–P)
    - Date (DD/MM/YYYY)
    - Temperature data: mean daily air temperature (2 m above lake) and 12 water depths (2–24 m, every 2 m)
    - Wind speed (corrected regional wind speed)
    - RTRM (calculated from temperature profiles for density)
  - RMTrapDiatoms.csv
    - 232 columns (A–HV or similar)
    - Sample code; Trap depth (S = 10 m, D = 25 m)
    - Trap type (O = Open tube, S = automatic sequencing)
    - Dates: start, end, total days, mid-date
    - Diatom taxa data: for each taxon, four sub-columns
      - Pristine percentage
      - Dissolved percentage
      - Total percentage in sample
      - Biovolume (µm³ cm⁻²)
    - Overall dissolution: pristine vs dissolved percentages
    - Total diatom cells per gram of sediment
    - Total diatoms per cm² per day
    - Additional diatom spike data (Aulacoseira) per 100 diatoms
    - Dissolution and breakage breakdown by category (undissolved broken, dissolved broken)
    - Total biovolume per gram of sediment
    - Total biovolume per cm² per day
    - Total sediment flux per cm² per day
    - Empty cells indicate missing data or 0 values indicate non-detects

## Data Management and Usage

- The dataset comprises two CSV files: RMTemperatures and RMTrapDiatoms.
- Data were generated using standardized methods, enabling cross-comparison and temporal trend analyses for environmental health monitoring.
- The documentation reflects QA steps (e.g., preparation, counting, dissolution categorization, and biovolume calculations) and provenance (references for methods).
- The aim aligns with standard environmental monitoring practice: create verifiable datasets, store them properly, and upload to appropriate data portals to facilitate broader access and reuse.