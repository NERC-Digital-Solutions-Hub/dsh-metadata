# Elemental concentrations (Ca, Cs, K, Mg, Sr) in a range of crops and associated soils from the UK and Spain

## Overview
- Dataset of elemental concentrations (Ca, Cs, K, Mg, Sr) plus NH4-N and NPOC in crops, soils, soil pore waters, and irrigation water from the UK and Spain.
- Plant growth studies conducted in spring/summer 2018–2019 at CEH Lancaster (UK) and a study in summer 2018 at the University of Extremadura (Spain); seeds and potato tubers exchanged between sites.
- Crops studied at maturity include radish, lettuce, grass, chard, courgette, strawberry, and potato; grown in diverse soil types with varying pH (4.5–7.9) and organic matter (LOI 3.1–23.7%).
- Sample types: crops (both edible and in-leaf/peel contexts), soils, soil pore waters, and irrigation waters.
- Data capture focused on enabling environmental health monitoring and policy evaluation by linking soil properties, crop uptake, and water chemistry.

## Data scope and structure
- Elements and associates: Ca, Cs, K, Mg, Sr, NH4-N, NPOC; additional measurements include pore water variables and irrigation water chemistry.
- Sample breadth: multiple crops per soil type, with both UK and Spanish soils, plus cross-site crop transfer (UK seeds/tubers used with Spanish soils and vice versa in some combinations).
- Data organization: detailed metadata and measurement results organized into structured datasets, including extensive data dictionaries to support reuse and interpretation.

## Methods and provenance
- Sample processing and quality control:
  - Lab practices aimed at preventing metal contamination; non-metallic containers and gear; use of agate equipment where possible.
  - Crop samples freeze-dried, ground (<2 mm); soils air or oven dried and ground.
- Analytical methods:
  - Elemental analysis by ICP-MS (Cs, Sr) and IC-ICP-OES (Ca, K, Mg).
  - Pore waters and irrigation waters analyzed directly after filtration and acidification.
  - Total dissolution via aqua regia digestion at 175°C for 12 minutes (microwave system) for soil/crop digests.
  - Alternative extraction for soils using 0.1 M BaCl2 (BaCl2 extraction) to compare with AR digests.
  - NPOC measured with Shimadzu TOC-L; samples acidified and purged prior to analysis.
- Calibration and quality control:
  - External calibration with internal standards (Ga, In, Re) to correct drift/matrix effects.
  - Instrument detection limits (LOD) derived from blanks; recovery considerations noted for AR digests.
- Data capture and validation:
  - Data recorded in Excel; approximately 20% of data validated by a second person.
  - References to established methodologies for LOI and pH (Allen 1989; Lofts et al. 2001).

## Data quality, limitations, and uncertainties
- Recovery and extraction caveats:
  - AR (aqua regia) extraction showed 51–63% recovery for K in soils, indicating incomplete dissolution of clays and underestimation relative to total extracts.
  - BaCl2 extraction used as a comparison method for some soil elements.
- Detection and reporting limitations:
  - Cs values sometimes reported as below detection limits; some entries flagged as below LOD.
  - Some data entries indicate non-applicable or bulk/replicate-only samples (e.g., “Unused” soils, multiple fruits per replicate).
- Metadata and traceability:
  - Comprehensive data dictionaries (14 tables) accompany the dataset to document sample lists, pore water samples, pH/LOI measurements, and crop-specific measurements.
  - Some complexity arises from multi-crop, multi-soil, and multi-year design, requiring careful interpretation of tables and units.
- Data accessibility and sharing:
  - The document emphasizes data provenance, metadata completeness, and governance as critical for reuse; actual public data sharing barriers are noted as a general concern for monitoring frameworks.

## Relevance for monitoring frameworks and policy
- Indicators for environmental health and food-chain exposure:
  - Provides baseline concentrations of key elements in crops linked to soil properties and irrigation water, enabling monitoring of uptake and potential dietary exposure.
- Cross-site comparability and soil-crop relationships:
  - Variation across soil types, pH, and LOI allows assessment of how soil chemistry influences elemental transfer to crops.
- Data governance and transparency:
  - Detailed metadata and QA procedures support reproducibility, benchmarking, and transparent reporting in policy evaluations.
- Data gaps and governance recommendations:
  - Highlighted barriers (data access, data silos, metadata adequacy, timely updates) align with common monitoring framework challenges; the dataset demonstrates good practice in documentation and QA, while also illustrating where governance improvements could help future monitoring efforts (e.g., standardized formats, open data sharing, ongoing updates).

## Key data components and metadata support
- Core data tables (as per CONFIDENCE data schema) include:
  - PlantGrowthStudy_Crop_SampleList: crop-specific sampling metadata.
  - PlantGrowthStudy_Soil_SampleList: soil-specific sampling metadata.
  - PlantGrowthStudy_PoreWater_SampleList: pore water sampling metadata.
  - PlantGrowthStudy_pH_LOI_Values: soil chemistry context (pH, LOI) by sample.
  - PlantGrowthStudy_RadishLeafAndEdibleRoot_FM_DM, StrawberryFruitAndLeaf_FM_DM, PeeledPotatoAndPeel_FM_DM, Courgette_FM_DM, Grass_FM_DM, Chard_FM_DM, Lettuce_FM_DM: crop-specific biomass and yield contexts with fresh and dry mass measurements and related ratios.
  - PlantGrowthStudy_Crop_ElementalConcentrations: crop tissue element concentrations (Ca, K, Mg, Sr, Cs) with notes on detectability and recovery considerations.
  - PlantGrowthStudy_Soil_ElementalConcentrations: soil elemental concentrations (AR and BaCl2 extracts) with detailed extraction-specific values and notes.
  - PlantGrowthStudy_PoreWater_ElementalConcentrations: pore water element concentrations (Ca, Cs, K, Mg, Sr, NPOC, Ti, etc.) with detection notes.
- Data provenance and references:
  - Clear provenance trail for sample origins, crop varieties, soil descriptors, and years harvested.
  - References to established soil and analytical methodologies inform interpretability and comparability with other monitoring datasets.

## Contact, provenance, and acknowledgments
- Acknowledges funding under the CONFIDENCE project (CONCERT EJP, Horizon 2020, grant No 662287) and supporting colleagues.
- Data generation involved CEH Lancaster and University of Extremadura collaborators, with explicit notes on sample transfer logistics and plant material exchanges.

## Implications for future monitoring work
- Use this dataset as a model for: transparent data lineage, multi-factor soil-crop-water integration, and QA-driven analytical workflows in environmental health monitoring.
- Consider adopting standardized metadata schemas and open data publication practices to minimize data-sharing barriers highlighted in monitoring frameworks.
- When using AR-based soil digests, apply caveats around recoveries for elements like potassium and the implications for interpreting total soil pools versus extractable fractions.