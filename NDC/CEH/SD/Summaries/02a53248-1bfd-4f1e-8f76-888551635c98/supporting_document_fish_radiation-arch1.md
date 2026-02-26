# Impact of Environmental Radiation on the Health and Reproductive Status of Fish from Chernobyl

## Study scope and objective
- Investigates health and reproductive status of fish (perch and roach) exposed to environmental radiation across lakes in Belarus and Ukraine.
- Combines radiological measurements, physiological indices, and reproductive histology to assess potential dose–response effects.
- Aims to enable correlations between radiation exposure and health/reproductive outcomes, using multiple datasets and dose estimates.

## Sampling design and study sites
- Fish collected: 124 perch and 82 roach (similar weight/length) in September 2014 from seven lakes; 38 perch and 60 roach in September 2015 from four lakes in Ukraine; 38 additional samples of perch/roach in March 2015 before spawning.
- Relative abundance of species in each lake evaluated in June 2015.
- Lakes categorized by radiation contamination: high (H), medium (M), and low (L), with distances from Chernobyl NPP ranging from 1.5 to 225 km.
- Lakes represented: Glubokoye, Yanovsky, Cooling Pond (high); Svyatoye Lake (medium); Stoyacheye, Dvoriche, Gorova (low).
- Ethical handling: fish euthanized humanely following UK Home Office procedures to limit suffering.

## Measurements and biological endpoints
- Morphometrics and condition
  - Body weight, total length; Fulton condition index (K); hepatosomatic index (HSI); gonadosomatic index (GSI).
- Radiological measurements
  - External: 137Cs measured in sediment and whole-body for external dose estimation.
  - Internal: 137Cs, 90Sr, 238Pu, 239,240Pu, and 241Am measured in fish tissues (liver, muscle) with different sampling schemes depending on proximity to NPP.
  - Uncertainties: 137Cs/90Sr up to ~20%/15%; transuranics up to ~25% (at 95% CI).
- Dose calculations
  - External dose derived from 137Cs gamma radiation using ERICA-based approach; sediment-based activity in surface layer (≈15 cm) with assumed density 1300 kg/m3; occupation factor 0.5 at sediment surface.
  - Internal doses calculated per radionuclide using tissue-specific dose conversion factors; different factors for 137Cs, 90Sr, 241Am, 238Pu, 239,240Pu.
- Liver chemistry
  - ICP-MS analysis of major and trace elements in liver tissue after nitric acid digestion; elements include B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U.
- Genotoxicity and reproductive physiology
  - Micronucleus test on erythrocytes: 1000 cells per fish scored blindly to detect micronuclei.
  - Histology of ovaries: assessment of immature and mature oocytes; quantification of germ cell stages by area, calculating relative frequencies of each stage.
- Data collection details
  - Data points include site, date, species, sex, weight, length, gonad and liver weights, health indices (K, HSI, GSI), and a suite of radiological and chemical measurements.

## Radiological and chemical data specifics
- 137Cs and 90Sr activity concentrations measured in whole fish or tissues; transuranics (238Pu, 239,240Pu, 241Am) measured primarily in liver and muscle near the NPP.
- Methods include gamma spectrometry (DGDK-100, Li-drifted Ge detector) for 137Cs; radiochemical separation and alpha spectrometry for Pu isotopes and 241Am; β radiometry for 90Sr.
- Internal and external dose assessments combine measured activities with dose coefficients to estimate organ- and body-level doses.

## Data handling, datasets, and metadata
- Several datasets described with explicit data structures and columns:
  - fish_biometry.csv: lake/site, date, gender, species, weight, total_length, gonads_weight, liver_weight, Fulton index (K), GSI, HSI.
  - fish_composition.csv: date and per-lake presence or abundance data for each lake (geographical region).
  - fish_whole.csv: site, species (perch or roach), and radionuclide levels (e.g., 137Cs, 90Sr) in whole fish.
  - fish_tissue.csv: tissue-specific radionuclide concentrations (Cs-137, Sr-90, Am, Pu-239, Pu-238) by tissue.
  - fish_liverchem.csv: liver chemistry data, including tissue masses (wet/dry), and macro- and trace-element concentrations (e.g., B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U).
  - fish_micronucleus.csv: micronucleus counts by site, species, sex, and percent of micronucleus-bearing cells.
  - fish_oocyte.csv: oocyte metrics including counts of immature and cortical alveolar oocytes, perinuclear oocytes, measured per defined area.
- Each dataset includes clear column headers and units/methodology, enabling cross-dataset integration and reproducible analyses.

## Analytical opportunities and potential correlations
- Cross-link radiological exposure (external/internal dose) with health indices (K, HSI, GSI) and condition metrics.
- Relate micronucleus frequency and ovarian oocyte development stages to radiation dose and tissue-specific radionuclide burdens.
- Compare biochemical liver composition with exposure levels to identify potential physiological or metabolic responses.
- Use dataset structures to build predictive models of health and reproductive status as a function of lake contamination gradient and distance from Chernobyl NPP.
- Address data gaps and scale issues by leveraging the multi-lake, multi-year design and standardized measurement protocols.

## Challenges and data stewardship
- Heterogeneous data streams across multiple lakes, years, and tissue types require careful standardization and normalization.
- Uncertainties in radiological measurements and dose estimates must be propagated in analyses.
- Data accessibility and traceability are supported by detailed metadata and explicit data structures, aiding reproducibility and reuse.