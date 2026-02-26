# Radionuclide transfer to milk: database creation and transfer coefficients

- The document describes creating a centralized database to handle and process data drawn from diverse information sources (books, journals, conference proceedings, institutional reports, and international/national databases).
- Data were individually reviewed and revised, with supplementation from additional English-language literature and a major Russian-language review (Fesenko et al., 2007) to enrich the dataset.
- When data were sufficient, transfer table values were provided with comprehensive metadata: number of data points (N), geometric mean (GM), geometric standard deviation (GSD), arithmetic mean (AM), and standard deviation (SD). For radionuclides with limited data (single-value), only the arithmetic mean is reported.

- Core data elements and structure
  - Cow milk metrics:
    - Cow_milk_Fm_GM_DL-1: transfer coefficient (Fm) for cow milk, GM, DL-1 units (days per litre).
    - Cow_milk_Fm_GSD_DL-1: GM standard deviation (GSD) for Fm.
    - Cow_milk_CR_GM: Cow milk concentration ratio (CR) GM (milk/feed equilibrium ratio).
    - Cow_milk_CR_GSD: CR geometric SD.
    - Cow_milk_N: Number of cow milk data entries for each element.
  - Goat milk metrics:
    - Goat_milk_Fm_GM_DL-1, Goat_milk_Fm_GSD_DL-1: analogous Fm values for goat milk.
    - Goat_milk_CR_GM: Goat milk CR GM.
    - Goat_milk_CR_GSD: Goat milk CR geometric SD.
    - Goat_milk_N: Number of goat milk data entries for each element.
  - Elements tracked (examples): Ag, Am, Ba, Ca, Cd, Ce, Cl, Co, Cs, Fe, I, Mn, Na, P, Pb, Pu, Ru, Se, Sr, U, Y, Zn, Zr.
  - Units note: Fm_DL-1 denotes days per litre; other elements use non-applicable units where stated.

- Scope of elements and matrices
  - Includes both cow and goat milk transfer data for a range of radionuclide elements.
  - Data entries cover transfer coefficients and concentration ratios, facilitating exposure assessments and predictive modelling.

- Data quality, provenance, and documentation
  - Explicit references to authoritative data sources (IAEA Handbook, 2010; Fesenko et al., 2007) to support parameter values and methodology.
  - Emphasizes documentation of work performed on datasets to ensure reproducibility and traceability.

- Data governance and sharing considerations for Data Stewards
  - Multilingual data handling (English and Russian) necessitates clear metadata conventions and interoperability standards.
  - Standardization of metrics (GM, GSD, AM, SD) and unit definitions (e.g., DL-1) to enable consistent sharing and reuse.
  - Clear handling of incomplete data (single-value radionuclides) with partial statistical reporting.
  - Importance of updating datasets as new data become available and respecting data provenance from primary sources.
  - Potential need to align with data-sharing policies and embargoes when integrating with portals and catalogues.

- Implications for use
  - Supports prediction of radionuclide transfer to milk in terrestrial and freshwater environments.
  - Facilitates cross-study comparisons and meta-analyses by providing harmonized transfer parameters and metadata. 

- References
  - International Atomic Energy Agency (IAEA). Handbook of Parameter Values for the Prediction of Radionuclide Transfer in Terrestrial and Freshwater Environment. Technical Reports Series No. 472. IAEA, Vienna, 2010.
  - Fesenko, S., et al. Review of Russian language studies on radionuclide behaviour in agricultural animals: part 2. Transfer to milk. Journal of Environmental Radioactivity, 98 (2007) 104-136.