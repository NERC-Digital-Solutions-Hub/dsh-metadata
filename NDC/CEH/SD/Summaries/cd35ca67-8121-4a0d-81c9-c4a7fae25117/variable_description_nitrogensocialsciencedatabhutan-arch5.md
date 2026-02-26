# NUE and Sustainable Nitrogen Practices Household Survey Data (SANH WP 1.3 Harmonised Household Survey)

## Overview
- Large, multi-topic household dataset focused on nitrogen use efficiency (NUE) drivers, adoption barriers, and decision-making affecting NUE in crop production.
- Part of the SANH WP 1.3 Harmonised Household Survey covering multiple countries, with data captured across multiple seasons and extensive metadata.
- Includes detailed labor, input, management, financial, livestock, household characteristics, and information-use variables to support cross-country analyses.

## Data structure and content
- Labor and labor costs
  - Season-specific labor hours by household members (HM) and hired labor (HL) for activities such as land preparation, seeding, weeding, planting, fertilizing, transplanting (rice), water management, harvesting, and miscellaneous tasks (examples: N6111, N6112, N6121, N61992, N610TotalS26, N631WAGES21, etc.).
  - Total labor hours per season and average wages per activity and season (e.g., N631LandPrepWAGES21, N632SeedWAGES21, N633WeedingWAGES21, N610TotalWAGES21).
  - Gendered labor counts (N621MaleS2, N622FemaleS2) and crop-specific labor coding (CropcodeLABS11, LABS12, LABS21, etc.).
- Crop and season data
  - Crop codes by season with associated activity data (e.g., CropcodeLABS11, CropcodeIRRGS11, CropcodeLABS21, CropcodeIRRGS21, etc.).
  - Season-specific activity data linked to crops and management practices (Season 1, Season 2, Season 3/continued sections) with extensive variable coding for inputs, yields, and management.
- Mechanization and inputs
  - Mechanization levels for land preparation, seed sowing, fertilizer application, irrigation, and harvesting (N681LandprepS11, N682SeedS11, N683FertilizerS11, N684IrrigS11, N685Harvesting1, etc.).
  - Access to machinery and costs associated with mechanization (N69WCOSTS11, N69COSTS21, N69COSTS22, N69COSTS23, N69COSTS24).
  - Animal power usage and costs (N64animalpowerS21, N65CostS21, etc.).
- Irrigation and water management
  - Access to irrigation, irrigation events, proportions, water management methods (N71AcessS11, N72DIrrigateS11, N74WaterMgtS11, N78PayS11, N79SourceS11; similarly for other seasons).
  - Rice-specific water management practices (N74WaterMgtS11 with rice-specific options, N75PuddleS11).
- Pesticides and IPM
  - Pesticide use at crop/season level, types of pesticides (farm-made vs manufactured), frequency of application, and costs (N81UsePesticideS1, N82Whattypeofpesticides, N83TimesapplypestownS1, N85Totalcostpesticide, N86UseIPMS1, etc.).
- Livestock and farming resources
  - Ownership of livestock by species, number of mature animals, reasons for raising, and animal movement/exit from the farm across multiple rounds (N92Animalspeciesown1..N92Animalspeciesown7, N93Whyraised1..N95IAnimalsleavefarm7, etc.).
  - Time allocated to livestock-related activities and days spent in different housing conditions (L1 L2 L3 constructs) across multiple species and years.
- Household characteristics and assets
  - Housing ownership, number of rooms, floor/material, lighting, cooking fuel, drinking water source, technology ownership (TVs, smartphones, internet access), power tillers, irrigation pumps, etc. (N141Ownhouseyoulive1, N142Roomsinthehouse1, N144Sourceoflighting1, N149Haveaccesstointernet1, N1413Ownanytransport1, N1417Havecropinsurance1, N14173Seasoncode1, etc.).
  - Expenditures and assets across monthly and yearly frames (N1311Avgfoodexpendmonth, N1321Clothsexpendyear1, N1323Healthexpendyear1, N1329Fixedassetsexpendyear1, etc.).
- Subsidies and policy context
  - Direct subsidies received in the past 12 months for synthetic fertilizer, agricultural machinery, irrigation charges, output price support, seed, and other subsidies (N151SubsidySynFert, N152SubsidyAgricMac, N153SubsidyIrrig, N154SubsidyOutputsup, N155SubsidySeed, N156SubsidyOthers).
- Decision making and information use
  - Exposure to crop demonstrations and fertilizer/manure trainings; decision-making processes for synthetic and organic fertilizer use; information sources and constraints (N101Attendcropdemo1, N102fertandmanuretrain1, N103Fertuseseekhelp1, N104Fertinforank1, N1081Decisionsonsyntfert1, N1081Decisionsonsyntfert2, N1081Decisionsonsyntfert3, etc.).
  - Attitudes toward decision support tools and adoption of practices (N1101DecisionsuportHeard, N1101BDecisionsuportUsing, N1102GreenmanureUsing, N1103AgroforestUsing, etc.).
  - Risk and technology adoption profiles (N121Describeyouingen, N122Iampreparedtotakerisk1, N126Manureconsiderfert1, N125VariousLikert-scale items on fertilizer/manure perceptions).
- Housing, assets, and credit
  - Household assets, electrical/internet access, debt, savings, credit needs, and access to financial institutions (N1414Neededaloan1, N1415Gottheloan1, N1416Distfinancialinstitution1, N1417Havecropinsurance1, N149 etc.).
- Data provenance and QA indicators
  - Enumerators’ notes and start/end timestamps for data collection, QA checks, and traceability elements (EnumeratorsnoteP18, EnumeratorsnoteP201, EnumeratorsnoteP291, N61Date1, N62Time1, N63Dateend1, N64Timeend1).

## Data governance and stewardship implications
- The dataset is large, multi-topic, multi-season with dense metadata and numerous coded variables (A*, N*, Cropcode*, etc.), requiring robust data governance to ensure interoperability and traceability.
- Key governance activities
  - Metadata and documentation: maintain comprehensive codebooks, data dictionaries, crosswalks, and country/site-specific exceptions; document units, permissible values, and data provenance.
  - Standardization: harmonize variable naming conventions, seasonal nesting, and crop codes across locations/countries; align with SANH harmonised schema where applicable.
  - Provenance and QA: preserve QA history (spot checks, back checks, enumerator notes) and document corrections/imputations traceably.
  - Privacy and sharing: assess disclosure risks due to household-level data; apply de-identification and access controls; clearly state data access conditions and licensing.
  - Interoperability: prepare raw, cleaned, and aggregated data products with clear provenance; provide schemas and data dictionaries for multi-country analyses.

## Practical usage and implications for analysis
- Enables examination of NUE drivers, adoption barriers, fertilizer use (synthetic and organic), subsidies, crop production economics, and labor dynamics across seasons and countries.
- Researchers will rely on detailed crop codes, input types, subsidy indicators, season-specific inputs/outcomes, mechanization levels, and labor allocations to model NUE and adoption decisions.
- Important for cross-country comparability but requires careful handling of season labels and country-specific adaptations.

## Challenges to anticipate
- Incomplete or evolving user needs and priorities across diverse contexts.
- Timeliness and consistency of data submission from data creators.
- Standardization across many systems, formats, and country-specific practices.
- Handling very large datasets with dense, nested seasonal structures and many multi-species livestock modules.
- Maintaining up-to-date documentation and cross-country harmonization in the face of ongoing data collection.

## Recommended next steps for data management
- Develop and maintain a comprehensive codebook and data dictionary mapping coded variables (A*, N*, Cropcode*, etc.) to definitions, data types, and units.
- Create crosswalks to harmonize country- and site-specific elements with the SANH WP 1.3 schema, including seasonal tiers and crop codes.
- Establish a metadata file (readme) detailing data collection protocols, QA procedures, sampling design, and data lineage.
- Implement a data governance plan with access rules, anonymization procedures, versioning, and update cycles for the harmonised dataset.
- Produce a data package including: raw dataset extracts, cleaned datasets, codebooks, data dictionary, QA logs, and enumerator notes index for traceability.