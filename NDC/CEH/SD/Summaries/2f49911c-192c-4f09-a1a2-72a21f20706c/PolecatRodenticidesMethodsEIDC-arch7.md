# Secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain 1990 - 2016

- Purpose of the document
  - Summary of data collection and laboratory methods used in the study on long-term exposure to anticoagulant rodenticides (SGARs) in European polecats in Great Britain (2018 Environmental Pollution paper).

- Data collection and sample types
  - National carcass collection (Vincent Wildlife Trust) 2013–2016; 68 polecats selected for rodenticide analysis.
  - Stratified sampling by sex, location, and collection date; majority were road traffic casualties (82%).
  - For each carcass: recorded collection date and location; assessed sex; measured body length, mass, and fat; many carcasses too damaged for body condition scoring.
  - Biological samples collected:
    - Liver tissue for rodenticide analysis.
    - Whiskers for stable isotope analysis.
    - Teeth for aging (cementum analysis).

- Laboratory analyses
  - Rodenticides (SGARs) in liver
    - Target compounds: bromadiolone, difenacoum, brodifacoum, flocoumafen, difethialone (five SGARs licensed in GB).
    - Method: liquid chromatography–tandem mass spectrometry (LC–MS/MS) with rigorous QA/QC.
    - Sample prep: liver sub-sample ground and dried; internal standard added; double extraction; cleanup via size-exclusion chromatography and solid-phase cartridges; multiple solvent exchanges.
    - Quantification: HPLC–MS/MS (APCI, negative mode); matrix-matched calibration with R² > 0.99; blanks included.
    - Quality metrics: mean limit of detection (LOD) per compound ~0.0014 µg/g (0.0022 µg/g for difethialone); mean total recovery ~68%.
    - Reporting: concentrations expressed on a wet weight basis; summed SGAR concentration (ΣSGAR) computed per animal; zeros assigned for non-detected compounds.
  - Stable isotope analysis (dietary signals)
    - Tissue: whiskers; segmental analysis along the length to capture temporal diet changes.
    - Preparation: whiskers cleaned, dried, cut into ~1 mm segments, weighed ~0.68 mg per sample.
    - Analysis: δ15N and δ13C measured with elemental analyzer–isotope ratio mass spectrometer (EA-IRMS).
    - Standards and replication: multiple standards (USGS) and in-house references; typical replicate precision reported (standard deviations for δ15N 0.05–0.29 ‰; δ13C 0.05–0.22 ‰).
  - Cementum aging (age at death)
    - Teeth prepared, sectioned, decalcified, stained; annual cementum growth layers counted to estimate age.
    - Birth date set to 1 May for monthly age estimation.
  - Calibration with historical data
    - Combined new data with historical Shore et al. (2003) dataset.
    - Applied historical LODs (higher than current study) to ensure comparability and reduce bias from analytical sensitivity changes.

- Data quality and interpretation considerations
  - Many carcasses were in poor condition, limiting clinical signs assessment and some measurements.
  - Liver SGAR data are not recovery-corrected and reported as wet weight.
  - Sampling biased towards road-kill and readily found carcasses; spatial and temporal coverage influenced by survey design.
  - Non-detections treated as zero concentration for ΣSGAR calculations.

- Spatial-temporal scope and applicability for GIS
  - Geographic scope: Great Britain; temporal span includes 1990–2016 (with carcass sampling 2013–2016 and historical data from 1992–1999/earlier studies).
  - Data types suitable for GIS products:
    - Geolocated carcass data (location + date) linked to liver SGAR concentrations for exposure mapping.
    - Age, sex, and body condition metadata to support stratified analyses.
    - Isotopic diet signals (δ15N, δ13C) as contextual layers related to trophic level and habitat use.
  - Potential map-based products
    - Spatial distribution maps of ΣSGAR liver concentrations across Great Britain.
    - Temporal trends of exposure by year and by region.
    - Diet-dynamics layers derived from whisker isotope profiles correlated with exposure indicators.
    - Age-structure and sex-based exposure patterns to inform risk assessments.

- Practical implications for GIS Specialists
  - Integrate carcass locations, exposure data, and sample metadata to produce informative, policy-relevant maps.
  - Account for sampling biases (e.g., road-kill bias) when interpreting spatial patterns.
  - Harmonize data with historical datasets using consistent LODs and units to enable robust temporal comparisons.
  - Combine exposure data with environmental layers (land use, rodenticide usage, roads) to explore drivers of exposure hotspots.

- References (primary sources cited)
  - Croose 2016; Shore et al. 2003; Matson et al. 1993; McDonald et al. 1998; Schulte-Hostedde et al. 2005; Mariotti 1983; Walker et al. 2017.