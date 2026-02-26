# Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016). Beresford et al., 2021

- Purpose and scope
  - Describes datasets and metadata underlying a study of soil biological activity in the Chernobyl Exclusion Zone (CEZ) for 2005 and 2016.
  - Provides column heading explanations (Tables 1–5) and the materials and methods used to generate the data files.
  - Data support a linked paper: Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016).

- Data files and structure
  - 2005 data
    - Radionuclide_concentration_data_2005.csv
    - Bait_lamina_2005.csv
  - 2016 data
    - Reader_1_bait_lamina_2016.csv
    - Reader_2_bait_lamina_2016.csv
    - Main_data_2016.csv
  - Additional data
    - Concentration_ratios.csv
  - Each file is documented with detailed column definitions (Tables 1–5) to enable interpretation, reuse, and integration with other datasets.

- Table-level metadata (column heading explanations)
  - Table 1 (Radionuclide_concentration_data_2005.csv): defines sample identifiers, sample type, sampling date, location, site, GPS coordinates, plot, and activity concentrations for Cs-137, Sr-90, Cs-134, K-40, Co-60 (including detectable minima where applicable).
  - Table 2 (Bait_lamina_2005.csv): defines radionuclide activities associated with bait lamina material (e.g., Am-241, Eu-154/Eu-155, Pu isotopes) and related mass units.
  - Table 3 (Reader_1_bait_lamina.csv and Reader_2_bait_lamina.csv): explains site, plot, replicate, bait lamina strip identifiers, bite/pierce records for each hole (1–16), and environmental variables (soil pH, soil moisture).
  - Table 4 (Main_data_2016.csv): provides location metadata (site, plot, latitude, longitude), ambient dose rate, radionuclide concentrations (Cs, Sr, Am, Pu isotopes), dose-rate components for different biotic groups, reader-derived bite totals, derived bite metrics, soil properties (pH, moisture, bulk density, temperature), habitat classification, and field notes.
  - Table 5 (Concentration_ratios.csv): explains concentration ratios used for annelids and detritivorous arthropods across nuclides (Cs, Sr, Am, Pu) and indicates corresponding occupancy assumptions and related units.

- Study design and data collection (methods snapshot)
  - 2005 CEZ sites (four locations): Red Forest (High, Dead), Izumrudnoe (Low), Novoshepel Forestry (Medium); site classification based on anticipated soil activity concentrations. Soil pH and moisture recorded; sampling date 27 September 2005.
  - 2016 CEZ sites (18 locations): within CEZ, including Red Forest (8 sites) and various deciduous/coniferous woodland sites; ambient dose rates measured in situ. Three 1x1 m plots per site; 16 bait lamina strips per plot inserted in a 4x4 grid during 17–19 April 2016; retrieval around 18 days later (5–7 May 2016). Soil temperature and moisture recorded.
  - Bait lamina assay: strips with 16 holes filled with bait; two readers recorded “pierced” vs “unpierced” (presence of bait removal). Results read blind and averaged across readers.
  - Soil sampling: five cores per plot (top 10 cm), bulked and homogenised; pH and moisture measured; dry mass determination for radionuclide analyses.
  - Radionuclide analyses: Cs-137, Sr-90, Cs-134, K-40, Co-60 measured by gamma spectroscopy or beta spectroscopy with specified detection limits and uncertainties; Am-241 and Pu isotopes measured via high-purity germanium detectors with referenced methodologies.
  - Dose rate estimation: external and internal dose rates estimated using ERICA Tool (annelids, detritivorous arthropods) and R&D128 (bacteria) with occupancy assumptions (100% for soil column) and use of site-specific concentration ratios where available.

- Data quality, documentation, and reuse
  - Comprehensive metadata and explicit tabled column definitions provide high transparency for data reuse, interoperability, and cross-study integration.
  - Data include measurement uncertainties, detection limit indicators (< denotes minimum detectable activity for several radionuclides), and explicit handling notes (e.g., averaging results from two readers).
  - The dataset links to an accompanying peer-reviewed work (Beresford et al., 2021) and cites ISO standards (ISO 18311:2016) and established dose calculation tools (ERICA Tool, R&D128) to support reproducibility of analyses.

- Governance, access, and caveats for data stewards
  - Clearly structured data with standardized column definitions across multiple files facilitates data discovery, governance, and reuse.
  - The documentation addresses data provenance (sampling dates, sites, plots, replication), measurement methods, and analysis approaches, enabling traceability and accountability.
  - Users should consult the linked 2005 and 2016 datasets together with the Methods section to ensure consistent interpretation of units, detection limits, and dose-rate calculations.
  - Licensing and data access terms are not specified in the provided excerpt; practitioners should refer to the data repository or publication for reuse permissions and any access constraints.