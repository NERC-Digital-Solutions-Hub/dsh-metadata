# Spatial and temporal variations in aquatic organic matter composition in UK surface waters

- Study purpose
  - Investigate how aquatic organic matter (DOM) composition varies spatially and temporally across UK surface waters.
  - Combine data on water chemistry, environmental variables, and DOM composition to enable cross-site analyses and interpretation.

- Study design and sampling
  - Timeframe: fieldwork conducted between 2018 and 2021.
  - Locations: four sites across England and Scotland; sampling encompassed catchments with peat or organic soils.
  - Habitat types: pools, headwaters, streams, inlets, reservoirs, lakes, and outlets; multiple locations within each catchment.
  - Site metadata collected to contextualize results; site locations anonymized in published datasets.

- Field measurements and sample collection
  - In situ measurements: pH, conductivity, dissolved oxygen, water temperature; air temperature, pressure, and humidity recorded.
  - Equipment: Hach MM156 portable multi-parameter meter.
  - Sample handling: 50 mL grab samples filtered in the field through 0.45 µm syringe filters; samples kept cold (cool bag in the field, cool box during transit) and stored at 4 °C in the lab.
  - Organic matter processing: large-volume samples filtered to extract particulate organic matter (POM); filtered water concentrated to ~100 mL and dried to collect residue containing colloidal and dissolved organic matter (DOM).

- Analytical methods
  - DOM characterization: elemental composition (C, H, N, O) analyzed with Elementar Vario MICRO cube after acid treatment to remove inorganic carbon.
  - Subset analysis: negative-mode FT-ICR MS performed on a subset of samples.
  - QA and quality control: 10% of samples analyzed in replicate; equipment calibrated at run start and with ongoing checks; replicate data compared, and averages used if within 95% agreement; re-analysis performed if replicates differed; derived metrics restricted based on physical properties after CHNO calculations.

- Datasets and data structure
  - UK_Sites
    - Metadata for each sampling site and visit (Site ID, Visit, Month, Year, Group, and various environmental descriptors).
    - Non-identifying of exact site locations in public access due to access agreements with water companies.
    - Key variables include peat area, elevation, water body type, land use, vegetation cover, catchment area, and peat presence.
  - UK_DOM
    - DOM composition metrics derived from CHNO data and FT-ICR MS where available.
    - Metrics include: proportion of organic carbon, oxidation state, oxidative ratio, double bond equivalents, C/N, H/C, O/C, assigned formulas, mean/SD of m/z, aromatic index, NOM oxidation metrics, diversity indices (Simpson, Shannon), and functional group percentages (lipids, carbohydrates, amino sugars, peptides, oxy-aromatic phytochemicals).
  - UK_Water
    - Environmental variables and water chemistry for each sample/visit.
    - Measurements include pH, conductivity, dissolved oxygen, water and air temperatures, humidity, air pressure, and a broad suite of chemical constituents (DOC, Cl, SO4, SUVA254, E4E6, DON, DIN, DOP, DIP, Ca, K, Mg, Na, Al, Mn, Fe, heavy metals, and a range of trace metals).
    - Dual entries (1 and 2) for many variables reflect replicates or duplicate measurements.
  - Data accessibility and anonymity
    - Site locations are anonymized in published datasets; some reservoir locations restricted by access agreements.
    - Full methodological references and data schemas provided to enable re-use and cross-site comparisons.

- Reference methods
  - Core DOM extraction method reference: Moody, Catherine S. (2020) A comparison of methods for the extraction of dissolved organic matter from freshwaters, Water Research.

- Implications for data use
  - Enables cross-site comparisons of DOM composition and its relationship to environmental drivers.
  - Supports data-driven insights for water quality management and policy via self-serve access to site-level and sample-level metrics.
  - Provides a structured, QA-backed dataset framework that can be integrated with broader water chemistry datasets for UK freshwater systems.