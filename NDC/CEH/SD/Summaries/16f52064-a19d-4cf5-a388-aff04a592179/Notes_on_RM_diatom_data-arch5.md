# Supporting Documentation

- Sediment trapping using sequencing traps was conducted at Rostherne Mere from January 2011 to January 2017 using Technicap PPS 4/3 automatic sequencing traps deployed at 10 m and 25 m depths. Each trap fed into 12 individual 250 ml HDPE bottles, representing ~2 week collection periods (longer 3–4 week periods in January and February). Traps were reset about every 6 months; collected sediment was kept cool, dark, sealed during transport, and stored frozen prior to analysis. Dry sediment weight determined total trap sediment flux.

- Diatom analysis and processing
  - Freeze-dried sediment prepared for diatom analysis using standard methods; peroxide digestion performed at room temperature.
  - A known quantity of microspheres added to cleaned diatoms before slide preparation.
  - Counting: at least 300 diatom valves per slide; if fewer than 100 microspheres reached by the 300th valve, counting continued without species identification until 100 microspheres were counted.
  - Diatom abundance, dissolution, and breakage recorded; valve breakage categorized into four classes; dissolution recorded as pristine/dissolved binary scheme.
  - Total diatom abundance calculated from relative counts to microsphere abundance; biovolume calculated for taxa with >3% abundance, using mean values derived from 25 representative slides.
  - Biovolume units: µm3 per cm2 for taxa-specific biovolume; total diatom biovolume also recorded.

- Auxiliary data and calculations
  - Daily air temperature (2 m above water) and water temperatures at 12 depths (every 2 m from 2–24 m) obtained from the UKLEON buoy.
  - Relative resistance to thermal mixing (RTRM) calculated from temperature-density profiles; stratification strength derived from epilimnion vs. hypolimnion densities.
  - Wind data: onshore wind speed from Manchester Airport corrected for local sheltering using a correction factor derived from UKLEON buoy data (VRM correction; validation R2 = 0.82, n = 1417).

- Nature and units of recorded values
  - Temperature profile: air temperature (°C), water temperatures (°C) at 12 depths, wind speed (m/s), RTRM (dimensionless numeric value).
  - Sediment trap data: trap type, collection dates, collection duration, diatom taxa abundances (percent), dissolution (percent), biovolume (µm3 cm-2), total diatom cells, dissolution/breakage metrics, and total diatom biovolume per sediment weight.

- Data structure and content
  - RMTemperatures (16 columns; A–P)
    - A: Date (DD/MM/YYYY)
    - B–N: Temperature data (mean daily air temperature at 2 m and 12 water depths)
    - O: Wind speed (corrected regional wind speed)
    - P: RTRM (calculated RTRM from temperature profiles)
  - RMTrapDiatoms (232 columns; A–HH)
    - A: Sample code
    - B: Trap depth (S = shallow 10 m, D = deep 25 m)
    - C: Trap type (O = Open tube, S = automatic sequencing)
    - D–G: Dates (sample begin, end, total days, mid-date)
    - H–HH: For each diatom taxon: four columns (percent pristine, percent dissolved, total percent of taxa, biovolume)
    - HI–HJ: Overall dissolution metrics (total pristine cells, total dissolved cells)
    - HK: Total diatom cells per gram of sediment
    - HL: Diatoms sedimenting per cm2 per day
    - HM: Additional spikes of Aulacoseira per 100 diatoms
    - HN–HU: Dissolution and breakage breakdown (undissolved, broken, dissolved, broken percentages)
    - HV: Total biovolume per gram of sediment
    - HW: Total biovolume sedimenting per cm2 per day
    - HX: Total sediment flux per cm2 per day
    - Other empty/missing data indicated by empty cells or 0 values as appropriate

- Data provenance and references
  - Methodological foundations cited: Renberg (1990); Battarbee et al. (2001); Battarbee and Kneen (1982); Hillebrand et al. (1999); Ryves et al. (2003, 2006); Wetzel (2001).
  - Standards and practices for diatom processing, counting, and biovolume estimation are aligned with published protocols for lake sediment diatom analysis.

- Governance, storage, and sharing considerations for Data Stewards
  - Dataset comprises two CSV files (RMTemperatures and RMTrapDiatoms) intended for upload to appropriate portals and catalogues.
  - Metadata should document:
    - Sampling period and depths, trap types, and collection intervals
    - Preservation, storage, and transport conditions (cool, dark, frozen; freeze-drying)
    - Analytical procedures (peroxide digestion, microsphere addition, counting thresholds, biovolume calculations)
    - Derived variables and calculation methods (RTRM, wind correction factor VRM)
    - Data structure details and unit conventions (°C, m/s, µm3 cm-2, etc.)
  - Data quality considerations:
    - Empty cells represent missing data; 0s indicate actual zero values for certain measures (e.g., absence of a taxon)
    - Transparency about any deviations from standard protocols or exceptional collection periods
  - Data management implications:
    - Ensure consistent column naming, units, and taxon coding across releases
    - Maintain provenance to enable reproducibility of diatom counts, biovolume calculations, and RTRM/wind corrections
    - Plan for versioning and updates, given semi-annual trap resets and multi-year data collection

- Practical implications for users
  - The dataset enables reconstructions of historical diatom communities, sediment flux, and environmental stratification dynamics at Rostherne Mere over 2011–2017.
  - Users should be aware of the detailed per-taxon metrics (pristine vs. dissolved vs. total percentages, biovolume) and the transformation steps used to derive total counts and fluxes.
  - Careful interpretation required for rows with missing data or zero-valued fields; consult methods and references for handling such cases.