# Impact of Environmental Radiation on the Health and Reproductive Status of Fish from Chernobyl

- Scope and aim
  - Assess health and reproductive status of perch and roach exposed to environmental radiation across lakes in Belarus and Ukraine.
  - Collect and analyze biometric, chemical, radiological, and histological data to understand relationships between radiation dose and fish health.

- Study design and sampling
  - Sampling times: September 2014 (seven lakes) and September 2015 (four lakes) with additional March 2015 collections prior to spawning.
  - Species: Perch (Perca fluviatilis) and Roach (Rutilus rutilus); use homogeneous mature groups.
  - Sampling methods: three gill nets (20 m, 21 mm mesh); selection of lakes along a radiation-dose gradient (high, medium, low contamination) relative to Chernobyl NPP.
  - Additional abundance sampling in June 2015.
  - Ethical considerations: fish euthanized following UK Home Office Animals (Scientific Procedures) Act guidelines to minimize suffering.

- Measurements and indices (biometrics and health)
  - Morphometrics: body weight, total length; external disease signs and macroscopic tumors recorded.
  - Age and condition: scales used for age; Fulton condition index (K), hepatosomatic index (HSI), and gonadosomatic index (GSI) calculated.
  - Data capture format: dedicated data structures for biometry and tissue analyses.

- Radiological analyses and dose assessment
  - Radionuclides measured:
    - 137Cs: whole-body activity; external dose estimated from surface sediments.
    - 90Sr: whole-body activity (some lakes only).
    - Transuranics: 238Pu, 239,240Pu, 241Am measured in liver and muscle near NPP vicinity.
  - Analytical methods and uncertainty:
    - Gamma spectrometry for 137Cs; radiochemical methods for 90Sr; alpha spectrometry for Pu and Am; detection limits specified (e.g., 0.6 Bq for 137Cs; 0.01 Bq for 90Sr β channel; 0.001 Bq for Pu/Am via alpha).
    - Overall measurement uncertainties: up to 20% for 137Cs, 15% for 90Sr, 25% for transuranics (95% confidence).
  - Dose calculations:
    - External doses dominated by 137Cs gamma radiation; external doses estimated with ERICA tool using sediment concentrations and a dose conversion factor.
    - Internal doses calculated for 137Cs in all lakes; internal doses for 90Sr, 241Am, 238Pu, 239,240Pu focused near NPP vicinity using corresponding dose conversion coefficients.
    - Sediment assumptions: majority of 137Cs in upper 15 cm of surface sediment; sediment density ~1300 kg/m3; occupation factor of 0.5 at sediment surface.
  - Data types linked to dose: site-specific internal and external dose estimates used to relate to health indicators.

- Liver chemistry and tissue analyses
  - Liver chemistry: nitric acid digestion of livers; major and trace element concentrations measured by ICP-MS with internal standards; calibration in two ranges (major elements 0–30 mg/L, trace elements 0–100 μg/L).
  - Micronucleus test: assessed genetic material loss in erythrocytes; 1000 cells scored per fish to detect micronuclei.
  - Histology of oocytes: fixed gonads, paraffin-embedded, H&E stained; maturation stages quantified by oocyte counts (perinuclear and cortical alveolar) and surface area measurements for oocyte stage distribution.

- Data structure and datasets
  - fish_biometry.csv: records site, date, gender, species, weight, total_length, gonad and liver weights, Fulton index (FC), GSI, HSI; notes missing fields where data were not recorded.
  - fish_composition.csv: date and species presence across lakes; location fields per lake and geographical region.
  - fish_whole.csv: whole-body radionuclide activity for perch and roach (137-Cs, 90-Sr) by site; units in Bq/kg.
  - fish_tissue.csv: tissue-specific radionuclide levels (e.g., Cs-137, Sr-90, Am, Pu isotopes) by tissue (muscle or liver) and site; weight of tissue samples recorded.
  - fish_liverchem.csv: liver tissue chemical composition (mass in mg, mg/L) and a wide panel of elements (B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U); separate measurements for wet and dry weights where applicable.
  - fish_micronucleus.csv: micronucleus results by site and species/sex; number of micronuclei per 1000 erythrocytes and percentage.
  - fish_oocyte.csv: oocyte metrics by date, site, and species; counts of cortical alveolar and perinuclear oocytes per defined area (micrometres squared).
  - Data identifiers emphasize cross-lake comparability and temporal coverage; dataset fields include clear units and methodology notes.

- Data quality, gaps, and considerations for data leaders
  - Heterogeneity in data collection across lakes and times; careful harmonization needed for cross-site analyses.
  - Missing fields: some samples have blank gender or weight records; data governance should establish imputation or exclusion criteria.
  - Measurement uncertainties explicitly quantified for radiological analyses; internal vs external dose separation aids exposure assessment.
  - Metadata complexity: multiple data structures with specialized units and methodologies require robust data dictionaries and standardization for discoverability and reuse.
  - Potential data uses: cross-lake comparisons of health indicators vs radiation dose; linkage of biometric health data with internal/external dose estimates and liver chemistry profiles; examination of reproductive status via histology and oocyte metrics.

- Governance and applicability for data-driven decision-making
  - The study demonstrates end-to-end data lifecycle: from sample collection and biometric/health assessments to radiological analyses, dose modeling, and rich multi-omics-like tissue data.
  - For data leaders, the work illustrates the importance of clear data structures, metadata, and data quality controls to support analyses across broader networks and timeframes.
  - Data products could be co-owned with the wider radiation-ecology research community; standardization of datasets and documentation would enhance discoverability and reuse.