# UK water chemistry and greenhouse gas emissions study, LOCATE, 2021-2022: Supporting information

- Project aims and design
  - Multidisciplinary LOCATE project (involving CEH, NOC, BGS, PML, and others) to improve understanding of carbon flow from land to ocean.
  - Field campaign focused on characterising diurnal greenhouse gas emissions from inland water bodies and how these vary by water body type and season.
  - Method: use floating chambers placed on selected waterbodies for 24 hours; compare gas samples taken at the start and end to determine 24-hour emissions.

- Sampling locations and scope
  - Sampling conducted across the UK at ponds, streams, lochs, dykes, broads, and wetlands.
  - Timeframe: July 2021 to March 2022.
  - Site selection aimed to maximise geographical and land-type variation.
  - Details of sampling sites provided in Table 1 and Figure 1 (sampling locations map).

- In-field sample collection and protocols
  - Water chemistry samples collected for:
    - Dissolved Organic Carbon/Total Dissolved Nitrogen (DOC/TdN)
    - Total Phosphorus (TP)
    - Soluble Reactive Phosphorus (SRP)
  - Sampling approach:
    - 60 mL syringe used; SRP and DOC samples filtered through 0.45 µm filters; filtered into sterile tubes (DOC/TdN stored in 30 mL bottles).
    - TP samples syringed directly into sterile tubes to accommodate freezing.
  - Physicochemical measurements:
    - pH, conductivity, Dissolved Oxygen (DO), and temperature measured with a two-channel HACH multimeter.
    - Calibrations performed prior to each sampling day (pH with buffers; conductivity with standard solution).
  - Floating chamber deployment:
    - Inverted plastic basins with floats, sealed with a three-way tap; chambers reflect sunlight to stabilise temperature.
    - Chambers floated in duplicates or triplicates to enclose air above water.
    - Gas samples retrieved after 24 hours via syringe and stored in Exetainer vials.
  - Dissolved gas sampling:
    - Headspace method used to sample dissolved CH4, CO2, and N2O at time 0 (start).
    - Gas samples drawn into syringes, equilibrated by shaking, then transferred to Exetainer vials.

- Sample storage and handling
  - TP, SRP, and spare filtered samples stored at -18°C for later analysis.
  - DOC/TdN and UV/Vis samples stored at 4°C and analysed within a week.
  - Greenhouse gas samples stored at room temperature until batched analysis.

- Laboratory analyses and methods
  - DOC and TdN
    - Instrument: Shimadzu TOC-LCPH with TNM L unit and ASI-L autosampler.
    - Method: 680°C combustion catalytic oxidation; samples sparged after acidification to remove inorganic carbon, reporting non-purgeable organic carbon (NPOC) as DOC.
    - Quality control: NPOC standards (5–20 mg/L), TdN standards (2–10 mg/L), blanks, calibration checks for TC and TN; duplicate analyses with a 2% CV threshold; outliers excluded.
  - UV/Vis and SUVA
    - Instrument: PerkinElmer UV/Vis Lambda 365; absorbance from 230–800 nm; blanked with deionised water.
    - SUVA254 calculation to indicate DOC aromacity (absorbance at 254 nm, adjusted to 1 cm path length and DOC concentration).
  - Total Phosphorous (TP)
    - Instrument: SEAL AQ2 Discrete Analyzer with acid digestion (potassium persulfate) to convert all P to orthophosphate.
    - Colorimetric detection: molybdenum blue with ascorbic acid; calibration using a 0.2 mg/L top standard and serial standards (0.1–0.2 mg/L) with blanks interspersed.
  - Soluble Reactive Phosphorus (SRP)
    - Filtered samples analysed on SEAL AQ2 using the same acid-molybdenum-blue method.
  - Greenhouse gases (GHG)
    - Instrument: Agilent 7890B GC with μECD for N2O and FID for CH4 and CO2.
    - Calibration against mixed standards; concentrations reported as ppmv and converted to µg/L using Henry’s law.
    - Duplicates averaged per site for final values.

- Data structure, units, and metadata
  - Dataset layout described (columns A–F sampling information; G–M field data; O–AD lab results).
  - Table 3 provides column descriptions and units for the MERLIN 2022-2023 dataset, including:
    - Site_name, Site_type, Date, Latitude, Longitude, Time
    - Field measurements: Conductivity, Conductivity_temp, pH, pH_temp, DO, DO_temp, Temp_av
    - Chemical data: DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP
    - GHG data: CH4_C, CO2_C, N2O_N, Chamber_CH4_C_time_0/24, Chamber_CO2_C_time_0/24, Chamber_N2O_N_time_0/24
  - Values are provided with specified decimal places and units (e.g., µS/cm, mg/L, µg/L, ppmv, ppb).

- Data quality, completeness, and exclusions
  - Table 4 documents data exclusions and reasons:
    - Examples include missing or not recorded determinants (e.g., pH, pH_temp), sample contamination, not recorded time, and missing samples for various sites.
    - Exclusions occur across multiple sites and determinants (Auchencorth Pond, Hoveton Broad, Dunsapie Loch, St Margaret’s Loch, Bush Estate Pond, Loch Lucy Pool variants, Llyn Cefni, Loch Leven, Dragonfly Pool, etc.).
  - Indicates emphasis on maintaining data integrity through exclusions where recording errors or contamination occurred.

- Acknowledgements and references
  - Acknowledgements to organisations enabling site access and sampling permissions.
  - References include methodological sources for SUVA and downstream dissolved inorganic carbon dynamics.

- Overall interpretation for data-driven analysis
  - Provides a comprehensive, methodically documented dataset enabling analysis of diurnal GHG fluxes from diverse UK inland waters.
  - Includes robust QA/QC processes (duplicates, blanks, calibration checks, CV thresholds) and standardized laboratory protocols.
  - Data are structured with extensive metadata and explicit reasons for data exclusions, supporting reproducibility and local-scale, cross-site comparisons.