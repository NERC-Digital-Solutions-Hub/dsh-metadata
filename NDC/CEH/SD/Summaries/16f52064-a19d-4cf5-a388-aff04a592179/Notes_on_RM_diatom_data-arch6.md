# Supporting Documentation

- Sediment trapping using sequencing traps conducted at Rostherne Mere from January 2011 to January 2017.
- Used Technicap PPS 4/3 automatic sequencing traps deployed at 10 m and 25 m water depths, feeding into 12 bottles representing ~2-week collection periods (longer 3–4 week periods in January/February).
- Traps reset ~6-monthly; samples stored cold, dark, frozen; all trap sediment freeze-dried and weighed for total dry sediment flux.

- Diatom analysis workflow and QA/QC
  - Freeze-dried sediment digested with concentrated H2O2 at room temperature to avoid heating hazards.
  - A known quantity of microspheres added before slide preparation for absolute counting.
  - Diatoms counted with standard methods; at least 300 diatom valves per slide, with a minimum of 100 microspheres targeted; counting continued beyond 300 diatoms if needed.
  - Valve integrity and dissolution recorded using a four-class pristine/dissolved scheme (F index); dissolution data captured as total pristine vs dissolved.
  - Diatom abundance calculated from relative counts to known microsphere abundance; biovolume calculated for taxa >3% abundance.
  - Biovolume measurements derived from 25 representative slides for mean taxon-specific figures.
  - Diatom data include both qualitative (presence/absence) and quantitative (biovolume) components.

- Ancillary environmental data
  - Temperature and wind data from the UKLEON buoy:
    - Average daily air temperature (2 m above water) and temperatures at 12 depths (2–24 m, every 2 m).
    - Wind speed corrected to local conditions using a site-specific correction factor.
    - Relative resistance to thermal mixing (RTRM) calculated from temperature-density profiles; total stratification strength derived from epilimnion vs hypolimnion density differences.

- Data products and structure
  - Two CSV files: RMTemperatures and RMTrapDiatoms.
  - RMTemperatures (16 columns):
    - Column A: Date (DD/MM/YYYY)
    - Columns B–N: Mean daily temperatures (air 2 m and 12 water depths 2–24 m)
    - Column O: Wind speed (corrected regional value)
    - Column P: RTRM (numeric)
  - RMTrapDiatoms (232 columns):
    - Column A: Sample code
    - Column B: Trap depth (S = 10 m, D = 25 m)
    - Column C: Trap type (O = Open tube, S = Automatic sequencing)
    - Columns D–G: Trap dates (start, end, total days, mid-date)
    - Columns H–HH: Diatom taxa data (for each taxon: pristine %, dissolved %, total % in sample, biovolume in µm³ cm⁻²)
    - Columns HI–HJ: Overall sample dissolution metrics (pristine %, dissolved %)
    - Column HK: Total diatom cells per gram of sediment
    - Column HL: Total diatoms sedimenting per cm² per day
    - Column HM: Additional spikes of Aulacoseira per 100 diatoms identified
    - Columns HN–HU: Breakdown of dissolution and breakage (undissolved, broken, dissolved portions)
    - Column HV: Total biovolume per gram of sediment
    - Column HW: Total biovolume sedimenting per cm² per day
    - Column HX: Total sediment flux per cm² per day
  - Data are accompanied by standard reference methods for diatom analysis, microsphere counting, and biovolume calculations.

- Units and data quality notes
  - Temperature: degrees Celsius (ºC)
  - Wind: meters per second (m/s)
  - RTRM: numeric resistance-to-mixing metric
  - Diatom biovolume: cubic micrometers per square centimeter (µm³ cm⁻²)
  - Diatom counts: per gram of sediment and per cm² per day, with missing data represented as empty cells
  - Data underpinning the two CSV files are generated through standardized laboratory procedures and referenced in the data description.

- Practical relevance and reuse
  - Enables temporal and depth-resolved analyses of thermal stratification, wind-driven mixing, and sedimentation processes.
  - Facilitates examination of diatom community composition, dissolution dynamics, and biovolume trends across years and trap depths.
  - Provides a structured, high-detail data foundation for reconstructing lake environmental change and cross-validating hydrodynamic and paleoenvironmental models.
  - Clear metadata and column definitions support integration with other datasets and reuse in dashboards or data products aimed at end users.