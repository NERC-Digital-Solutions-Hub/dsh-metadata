# Elemental concentrations in representative species of the ICRP's Reference Animals and Plants and associated soils in terrestrial Mediterranean ecosystems in Spain.

## Overview
- Dataset of stable element concentrations in representative species (RAPs) and associated soils from terrestrial Mediterranean ecosystems in Spain (Cáceres, Monfragüe area).
- Includes 17 soils, 34 plant samples, and 118 animal tissue samples across two sites: a dehesa and Bazagona pinewood.
- Aligns with ICRP reference animals and plants framework; aims to support radiation transfer and environmental risk assessments.
- Data collected between July–November 2014, with GPS-recorded sampling locations and fresh weights reported for all animal samples.

## Sampling design and sites
- Locations:
  - Dehesa (Valero dehesa): large private area with traditional rotating quarter system; near Monfragüe National Park.
  - Bazagona pinewood: natural pine forest, no management.
- Dehesa sampling areas:
  - Pond area (~5000 m²): Earthworms, Bees, Frogs, Rat, Wild Grass RAPs, and soil.
  - Dry riverbed area (~600 m²): soil; proximity ~200 m from Pond area.
  - Rat sampling area (~9500 m²): Bee, Rat, Wild Grass RAPs, and soil; ~4 km from Pond area.
- Pinewood sampling area (~5200 m²): Soil, Wild Grass, Pine tree (leaves, cones, bark, wood, branches); ~16 km from Pond area.
- Deer (Cervus elaphus): tissues from hunted individuals; exact kill location not recorded.
- Sample collection sites recorded via handheld GPS; fresh weight (f.w.) reported for all animal samples.

## Sample collection and preprocessing
- Animal sampling:
  - Earthworms, bees, frogs, rats, and deer tissues collected and processed to obtain relevant tissues (e.g., gut, thyroid area, liver, kidney, carcass).
  - For rats and some deer samples, tissues were separated into defined parts (e.g., muscle, bone) or pooled as needed to estimate whole-organism concentrations.
  - Freeze-drying used for most tissues; dry/fresh ratios recorded.
- Plant and soil sampling:
  - Wild grass (Briza minor) collected ~1 cm above soil; freeze-dried; dry/fresh ratio documented.
  - Pine trees sampled for leaves, cones, bark, wood, and branches; composite samples created from multiple trees.
  - Soil samples 0–10 cm collected at each site; composite within site (minimum six sub-samples); sieved, homogenized, oven-dried.

## Analytical methods and extraction procedures
- Elemental analysis: ICP-MS (iCAP-Q) with multiple modes (He-cell, STD, H2-cell) and internal standards; iodine analyzed separately using 1% TMAH matrix.
- Sample preparation by matrix:
  - Soils: size-reduced; two extraction routes per sample:
    - Acid digestion (HF, HNO3, HClO4) for total element content.
    - 10% TMAH extraction for solubilized fractions; 1% final TMAH for analysis.
  - Plant material: microwave-assisted acid digestion (HNO3) and microwave-assisted TMAH extraction; partial dissolution noted for some samples.
  - Animal tissues: microwave-assisted acid digestion (HNO3 + H2O2) and microwave-assisted TMAH extraction; aliquots may include bone and muscle sub-samples.
- Quality control and standards:
  - Use of certified reference materials (CRMs) for validation:
    - Soil: NIST SRM 2711a Montana soil.
    - Plant: NIST 1573a Tomato Leaves.
    - Animal: NIST 1577c Bovine Liver.
  - Recovery checks: iodine recovery in TMAH extraction ~89–95% for CRM tomato leaves; general recoveries for other elements compared with CRMs.
- Data handling and reporting:
  - External calibration with multi-element standards; internal standards included in the sample line.
  - Detection limits based on 3× standard deviation of reagent blanks.
  - For iodine, standard mode with Re as internal standard; discussed in context of iodine recovery and dissolution efficiency.
- Notable methodological notes:
  - TMAH extraction of plant material sometimes incompletely dissolves tissue; iodine results consider this limitation.
  - Some samples (e.g., RCN122, RCP300, RCP303, RCP125) partially dissolved due to large particle size, potentially affecting iodine accuracy.
  - B and S soil recoveries were poor in some acid digestions, likely due to volatile species formation.

## Data quality, limitations, and caveats
- Partial dissolution and incomplete matrix digestion can influence iodine and certain element results in plant tissues.
- Soil B and S recoveries were not always reliable due to volatilization during digestion.
- Deer tissue data include composite sampling and lack exact geographic provenance for kill locations.
- Documentation notes provide critical context for data interpretation (e.g., tissue dissection strategy, animal tissue composites).

## Data management, governance, and stewardship considerations
- Metadata to capture:
  - Site names, GPS coordinates, sampling dates, and sampling areas.
  - Sample types (species, tissue, soil), number of individuals, fresh and dry weights, and tissue processing details (e.g., bone/muscle separation, composite samples).
  - Preparation methods (freeze-drying, grinding), extraction methods (acid digestion, TMAH extraction), digestion parameters, and analysis mode (ICP-MS settings).
  - QA/QC data: CRM recoveries, detection limits, calibration curves, blanks, and method validation notes.
  - Data limitations: notes on partial dissolution, potential biases due to non-perfect matrices, and deer sample provenance limitations.
- Data sharing and governance:
  - Ensure explicit linkage between tissue-level data and whole-organism concentration estimates, with clear documentation of how whole-body values were inferred (bone/muscle fractions, literature-based weights for certain species).
  - Maintain traceability to CRM reference materials for each analytical batch and report any deviations or partial digestions.
  - Provide clear caveats and methodological context to users assessing applicability to risk assessment or transfer models.
- Next steps for stewardship:
  - Validate and harmonize metadata fields to support discoverability and interoperability across datasets (e.g., standard species codes, tissue abbreviations, unit conventions).
  - Consider embargo or access notes if data sensitivities or collaboration conditions apply.
  - Document data lineage and versioning to reflect updates or re-analyses.

## References and acknowledgments
- Cited works related to RAPs and transfer parameters (Barnett et al.; IAEA Handbook; ICRP publications).
- Acknowledgements of funding and institutional support (TREE project, COMET project, Junta de Extremadura, and related mobility grants).