# Summary This dataset includes key photosynthesis and respiration data from three common garden sites along an elevation/temperature gradient in the Colombian Andes, collected between June and August 2019.

- Data files
  - Three CSV files:
    - ACiData_ColombianAndes_2019
    - VcmaxJmaxData_ColombianAndes_2019
    - RdarkData_ColombianAndes_2019
  - Column set (example): ID (genus, species, ID), Date, Time, A (photosynthesis, µmol m⁻² s⁻¹), Ci (internal CO₂, µmol mol⁻¹), gsw (stomatal conductance, mmolm⁻² s⁻¹), Tleaf (°C), RH (%), Qin (PPFD, µmol m⁻² s⁻¹), Patm (kPa), Vcmax25, VcmaxTg, Jmax25, JmaxTg, Rdark25, RdarkTg.
  - Descriptions and units provided in accompanying Table 1.

- Experimental design
  - Three experimental sites at different altitudes in the Colombian Andes with distinct mean annual temperatures (MAT): high (2516 m, ~14°C MAT), mid (1357 m, ~22°C MAT), low (736 m, ~26°C MAT).
  - Each site: six blocks per plot, with 6x15 plants per plot and 4x90 plants per site.
  - Block 6 in each plot received fertilised soil.
  - Plants originated from nursery (two years) and were planted in November–December 2018.
  - Data collected from eight species, totaling 123 individuals.

- Data collection and A-Ci curves
  - A-Ci curves measured with LI-6800 portable photosynthesis system.
  - Cuvette conditions: 29°C, 65% RH, 410 ppm CO₂; g_s ≥ 0.05 mol m⁻² s⁻¹, eight ambient CO₂ levels (Ca: 410, 300, 175, 60, 410, 800, 1500, 2000 µmol mol⁻¹).
  - Light intensity set to species-specific saturating PPFD based on prior A-Q curves.
  - A-Ci data stored in MontaneAcclim-ACiData2019.csv.

- Parameter estimation (Vcmax and Jmax)
  - Vcmax and Jmax estimated by fitting A-Ci data to Farquhar et al. (1980) C3 model using the plantecophys R package (fitacis).
  - Temperature corrections:
    - Vcmax and Jmax estimated from curve fits, then corrected to 25°C and to the site MAT using a temperature response function with parameters from Kumarathunge et al. (2019).
  - Data handling:
    - Included measured Rdark values in curve fitting (adjusted to measurement temperature).
    - Two fitting approaches used:
      - default: nonlinear regression without assuming limiting region
      - bilinear: used when default quality criteria failed
  - Quality control:
    - 144 of 147 individuals retained after QC; 9 Jmax values excluded due to data quality; some curves deemed Rubisco-limited and excluded from Jmax estimation.
  - Output data files:
    - Vcmax and Jmax values, 25°C and site MAT values, stored in VcmaxJmaxData_ColombianAndes_2019.csv.

- Dark respiration (Rdark)
  - Rdark measured on the same leaves after A-Ci measurements, after dark adaptation (foil-covered) for 30 minutes to hours.
  - CO₂ efflux measured every 5 seconds for 1 minute, between 15:00–16:00.
  - 12 measurements per leaf; mean used; measurements taken at the site ambient temperature.
  - Rdark values corrected to 25°C and site MAT using a fixed Q10 exponential relationship, with Q10 varying with site MAT (14°C, 22°C, 26°C).
  - All Rdark data stored in RdarkData_ColombianAndes_2019.csv.

- Data quality, lineage, and limitations
  - Data were collected and analyzed by the study lead author (AJFC).
  - Some values missing due to instrument error or post-processing quality assessment.
  - A subset of curves was excluded due to instability or inappropriate Rubisco limitation assumptions.
  - Data processing steps (code examples) and parameters provided for reproducibility.

- Metadata and dissemination
  - Column names, units, and descriptions are clearly documented (Table 1).
  - Data processing steps, model fitting details, and correction equations explicitly described.
  - Data assets are designed to enable cross-site comparisons of photosynthetic capacity and respiration with explicit provenance and site-specific calibration.

- References and methodological context
  - Key references for methods and models used:
    - Farquhar, von Caemmerer, Berry (1980): biochemical model of C3 photosynthesis
    - Duursma (2015): plantecophys R package
    - Kumarathunge et al. (2019): temperature dependence of photosynthesis
    - Tjoelker et al. (2001); Scafaro et al. (2017): respiration and acclimation context
  - R statistical software used for analysis (R Core Team, 2022).