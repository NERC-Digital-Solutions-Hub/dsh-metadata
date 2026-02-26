# Summary

- This dataset provides key photosynthesis and respiration measurements from three common garden sites along an elevation/temperature gradient in the Colombian Andes, collected between June and August 2019.
- It comprises three CSV files:
  - MontaneAcclim-ACiData2019.csv (A-Ci curve data)
  - VcmaxJmaxData_ColombianAndes_2019.csv (Vcmax and Jmax values)
  - RdarkData_ColombianAndes_2019.csv (R dark values)
- Variables and their units are described in Table 1, including: leaf A (photosynthesis), Ci (internal CO2), gsw (stomatal conductance), Tleaf, RH, Qin, Patm, Vcmax25, VcmaxTg, Jmax25, JmaxTg, Rdark25, RdarkTg, plus identifiers (ID, Date, Time).

- Experimental design
  - Three sites at different altitudes with mean annual temperatures (MAT) of ~14°C, ~22°C, and ~26°C.
  - Each site uses a common soil mix and irrigation to maintain constant soil moisture; plants were nursery-grown for two years before planting in 2018.
  - Data come from eight species across 123 individuals planted in 6x15 plant plots (4x90 plants per site), with one fertilized block highlighted.

- Data collection methods
  - A-Ci curves measured with a LI-6800 portable photosynthesis system under standardized cuvette conditions (29°C, 65% RH, 410 ppm CO2) across eight ambient CO2 levels to span different Ci.
  - Light intensity was set to saturating levels specific to each species.
  - Raw A-Ci data are in MontaneAcclim-ACiData2019.csv.

- Derivation of physiological parameters
  - Vcmax and Jmax estimated from A-Ci data by fitting Farquhar et al. (1980) C3 photosynthesis model using the plantecophys R package.
  - Both measured Rdark values and A-Ci data were incorporated in the curve-fitting process.
  - Two fitting approaches used: default non-linear regression (preferred) and bilinear regression when data quality or curve characteristics warranted it.
  - A-Ci curves and parameter estimates were quality-checked; outliers removed. From 147 individuals, 144 were retained; 9 Jmax values were excluded due to fitting issues or limitations in the data.

- Temperature corrections
  - Vcmax and Jmax values were corrected to both 25°C and the site MAT using a temperature response function incorporating activation energy (Ea), entropy (ΔS), and deactivation (Hd) parameters, with reference to Kumarathunge et al. (2019).

- R dark data
  - Rdark values were measured after A-Ci measurements by dark-adapting leaves and recording CO2 efflux at 5 s intervals for 1 minute.
  - Rdark values were temperature-adjusted to the A-Ci measurement temperature and then corrected to 25°C and site MAT using a fixed Q10 approach (Tref-based) with Q10 temperature dependence tied to site MAT (Tg).

- Data processing and reproducibility
  - Analyses were conducted in R (v4.2.1) using the plantar-eophys 'fitacis' function with options for different fitting methods and inclusion of Rdark.
  - An example code snippet is provided to illustrate the workflow.
  - All data and derived results are available in the accompanying CSV files.

- Data quality, limitations, and governance
  - Rigorous quality checks led to the exclusion of a small number of curves (unusual Vcmax/Jmax estimates; some Rubisco-limited curves).
  - The dataset includes notes on isolated missing values due to instrument error or post-processing exclusions.
  - The data are designed to support analyses of thermal acclimation potential in tropical montane forest species and can inform cross-site comparisons of photosynthetic capacity under different temperature regimes.

- References and methodological context
  - Farquhar, von Caemmerer, and Berry (1980) photosynthesis model and curve-fitting approaches.
  - Key methods for enzyme kinetics and temperature responses (Kumarathunge et al. 2019; Scafaro et al. 2017; Tjoelker et al. 2001).
  - Software and statistical approaches using R and the plantecophys package.