# Impact of Environmental Radiation on the Health and Reproductive Status of Fish from Chernobyl

- Aims and scope
  - Assess health and reproductive status of perch (Perca fluviatilis) and roach (Rutilus rutilus) across multiple lakes in Belarus and Ukraine with a gradient of radiation exposure.
  - Collect biometrics, chemical/physiological indices, and radionuclide measurements to evaluate external and internal radiation doses and associated biological effects.

- Sampling and study design
  - 124 perch and 82 roach with similar weight/length collected in September 2014 from seven lakes; 38 perch and 60 roach collected in September 2015 from four Ukrainian lakes; 38 perch and 60 roach also collected in March 2015 before spawning.
  - Relative abundance assessed in June 2015 with additional sampling.
  - Fish were processed humanely, scales used for age determination, and multiple health metrics recorded (weight, total length, external signs, tumors).

- Measurements and analyses
  - Body condition and organ indices
    - Fulton condition index (K), hepatosomatic index (HSI), and gonadosomatic index (GSI) calculated from body weight, liver weight, gonad weight, and total length.
  - Radiological measurements
    - 137Cs measured in whole body (five fish per lake, 2014 sampling) using gamma spectrometry.
    - 90Sr measured in whole body (five fish per lake for select lakes) using radiochemical procedures.
    - 238Pu, 239,240Pu, and 241Am measured in liver and muscle from near-NPP lakes; 241Am also via gamma detection.
    - Reported uncertainties: 137Cs, 90Sr ≤ 20% and transuranics ≤ 25% at 95% confidence.
  - Dose calculations
    - External doses from 137Cs gamma radiation using ERICA-based methodology; surface sediment assumed to be the main reservoir (15 cm), density 1300 kg/m3.
    - Dose rate calculation: external, with occupation factor 0.5, conversion factors provided.
    - Internal doses for 137Cs (all lakes) and for 90Sr, 241Am, 238Pu, 239,240Pu (near-NPP lakes only) using specified dose conversion coefficients and lake-specific activities.
  - Liver chemistry
    - Acid digestion of livers; ICP-MS analysis for major elements (Na, Mg, S, K, Ca) and trace elements (As, Sr, Cd, Cs, Pb, U) with internal standards; two calibration sets for major and trace elements.
  - Genotoxicity assessment
    - Micronucleus test on erythrocytes: 1000 cells scored per fish; assessment of micronuclei as indicators of genetic material loss.
  - Reproductive biology
    - Histological analysis of oocytes: fixed gonad sections stained (H&E); immature and mature oocytes counted; oocyte surface area measured; germ cell stage distribution calculated as percentages.

- Lake contamination gradient and geography
  - Lakes categorized by contamination level relative to Chernobyl NPP:
    - High (H): Glubokoye, Yanovsky, Cooling Pond
    - Medium (M): Svyatoye Lake
    - Low (L): Stoyacheye, Dvoriche, Gorova
  - Distances from NPP range from 1.5 to 225 km, reflecting a gradient of long-term exposure.
  - Map references indicate regional groupings: Mogilev (Svyatoye), Gomel (Stoyacheye, Dvoriche), CEZ near NPP (Glubokoye, Yanovsky, Cooling Pond), and eastern Kiev region (Gorova).

- Data structure and datasets
  - fish_biometry.csv
    - Variables include Site, Date, Gender, Species, Weight, Total_length, Gonads_weight, Liver_weight, Fulton condition index (FC), GSI, HSI.
  - fish_composition.csv
    - Variables include Date and multiple lakes (Dvorishche, Stoyacheye, Svyatoye, Glybokoye, Yanovsky, Cooling_Pond, Gorova) describing species composition by site.
  - fish_whole.csv
    - Variables include Site, Species (P or R), 137-Cs_(Bq/kg), 90-Sr_(Bq/kg) for whole-fish measurements.
  - fish_tissue.csv
    - Variables include Tissue, Date, Site, Species, Weight_(g), Cs-137_(Bq/kg), Sr-90_(Bq/kg), Am_(Bq/kg), Pu239_(Bq/kg), Pu238_(Bq/kg).
  - fish_liverchem.csv
    - Variables include Sample, Lake, Mass_(mg,ww), Mass_(mg,dw), and a broad panel of elements (B, Na, Mg, P, S, K, Ca, Al, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Pb, U) with units (mg/L or µg/L).
  - fish_micronucleus.csv
    - Variables include Site, Species, Sex, No._micronucleus, No_of_cells, % (micronucleus per 1000 erythrocytes or per area).
  - fish_oocyte.csv
    - Variables include Date, Site, Species, Oocyte_(micro_m2), Perinuclear_oocytes_(count/area).

- Data quality and interpretation
  - Data include both whole-fish and tissue-specific measurements with explicit blank fields indicating non-recorded values.
  - Methodologies and detection limits are specified for radiological analyses (γ spectrometry, radiochemical procedures, alpha spectrometry) and for chemical analyses (ICP-MS with collision cell technology and internal standards).
  - Uncertainties are reported for radionuclide measurements, enabling downstream uncertainty propagation in data use.

- Potential data supports and applications
  - Creation of integrated dashboards or self-serve reports combining biometric, chemical, radiological, and histological data across lakes and years.
  - Cross-dataset analyses to link exposure (external/internal doses) with health indices (K, HSI, GSI), genetic endpoints (micronucleus), and reproductive metrics (oocyte development).
  - Data validation and harmonization opportunities across sampling times and sites to support policy or environmental monitoring discussions.
  - Reproducibility and traceability through clearly defined data structures and measurement methodologies, suitable for metadata documentation and data curation in future studies.