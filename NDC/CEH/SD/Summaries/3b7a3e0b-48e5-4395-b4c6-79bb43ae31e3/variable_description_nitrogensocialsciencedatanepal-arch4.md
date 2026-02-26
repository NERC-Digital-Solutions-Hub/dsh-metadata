# Variable description

## Overview of content and purpose
- Detailed variable-level descriptions for labour, wages, mechanization, irrigation, pesticides, fertilizers, manure, IPM, livestock, information sources, costs, and household characteristics.
- Data spans multiple seasons and activities (e.g., season 1 to season 4, with HM and HL distinctions; male/female labour counts; time and wage data).
- Designed to support cross-season, cross-country analysis within a harmonised survey framework, enabling analysis of labour costs, input use, mechanization adoption, water management, pest and nutrient management, and household expenditures.

## Key variable themes and structure
- Labour and time
  - Hours spent on crop labour by season (e.g., N610TotalS12) with breakdowns by household members (HM) and hired labour (HL), and by activity (land preparation, seed, weeding, planting, fertilizing, transplanting, water management, harvesting, others).
  - Season-specific labour totals (e.g., N610TotalS21, N610TotalS22, etc.) and counts of workers (e.g., N621MaleS1, N622FemaleS1).
- Wages
  - Average wages for various labour activities by season and worker type (e.g., N631LandPrepHMS11, N632SeedHLS11, N633WeedingHLS11, N634PlantingHLS11, N635FertilizingHLS11, N636TransplRICEONLY11, N637WatermgtHM1, N638HarvestingHM1, N6399OthersHMS11; similarly for subsequent seasons).
  - Season-specific wage data for HM and HL, plus total wages (e.g., N610TotalWAGES21, N610TotalWAGES22, etc.).
- Mechanization and inputs
  - Level of mechanization for each labour activity (e.g., N681LandprepS11, N681LandprepS21, N682SeedS11, N683FertilizerS11, N684IrrigS11, N685Harvesting1, etc.), with categories Fully mechanized, Partially, Fully manual across seasons.
  - Related costs when machinery is used (e.g., N69WCOSTS11, N69COSTS21, N69COSTS22, etc.).
- Irrigation and water management
  - Crop irrigation and water management specifics (e.g., sources, pricing mechanisms, and payments: N71AcessS11, N72DIrrigateS11, N74WaterMgtS11, N75PuddleS11, N78PayS11, N79SourceS11; and parallels for subsequent seasons).
  - Crop-code scoping and irrigation attributes (e.g., CropcodeIRRGS11, CropcodeIRRGS12, CropcodeIRRGS21, etc.).
- Pesticides and IPM
  - Pesticide use indicators, type of pesticides (farm-made vs manufactured), application frequency, and total costs; integration with IPM (N81UsePesticideS1, N82TypeS1, N83TimesapplypestownS1, N85Totalcostpesticide, N86UseIPMS1; and corresponding sets for seasons 2–4).
  - Crop-code references for pest data (e.g., Nq8CropCodepestS1, Nq8CropCodepestS21, Nq8CropCodepestS22, Nq8CropCodepestS23, Nq8CropCodepestS24).
- Fertilizers and decision-making
  - Fertilizer use decisions and guidance sources (N1081Decisionsonsyntfert1, N109Keeprecordfertilizer1, N1010Keeprecordyield1; and repeated sets for further seasons 2–4).
  - Decision-support tools and information sources (N1101DecisionsuportHeard1, N1101BDecisionsuportUsing1, N1102GreenmanureHeard, N1104AnerobicUsing1, etc.).
  - Attitudes and beliefs about fertilizer and manure (N122–N128 series), including risk tolerance, soil fertility beliefs, and willingness to adopt new practices.
  - Records and prompts for fertilizer management information and decision support (N123WHATchangehowusefert1, N1242Betterharvmoreorgfert1, N125Nolimittaddingsytfert1, N1251Nolimittaddingorgfert1, etc.).
- Manure and soil management
  - Perceived importance and applications of manure and related practices (N1271–N12713 series; N1281–N1289 series on manure uses and attitudes).
  - Scenarios regarding willingness to adopt or evaluate manure-based options.
- Livestock and farm assets (selected indicators)
  - Households’ livestock ownership indicators and related reasons for keeping animals (N91Raisedlivestock, N92Animalspeciesown1–N94Animalreasonraised1, etc. with multi-animal type expansions).
- Household assets, expenditures, and living conditions
  - Monthly and annual expenditure categories (N1311Avgfoodexpendmonth, N1312Tobacoexpendmonth, N1323Healthexpendyear1, N1329Fixedassetsexpendyear1, N141Ownhouseyoulive1, N144Sourceoflighting1, N145sourceoffuelforcooking1, N149Haveaccesstointernet1, N410Ownapowertiller1, etc.).
  - Access to services and infrastructure (internet access, transport ownership, crop insurance, loans, financial distance, etc.).
- Administrative and metadata
  - Enumerators’ notes and miscellaneous metadata (EnumeratorsnoteP18, EnumeratorsnoteP211, P24, P25, P26, P281, P291, etc.), timing data (N61Date1, N62Time1, N63Dateend1, N64Timeend1).

## Data governance and usability considerations for Data Leaders
- Data dictionary and metadata
  - The dataset relies on explicit variable names, coding schemes, and cross-season identifiers to support discoverability and reuse.
- Data quality and standardization
  - Standardized variable naming across labour, wages, mechanization, irrigation, pests, fertilizers, manure, livestock, and household characteristics; QA-like notes embedded in fieldwork metadata.
- Data integration and linkage
  - Structure supports linking household-, farm-, and plot-level data across seasons, crops, inputs (synthetic and organic), and subsidies to enable system-wide analysis.
- Access, privacy, and governance
  - Granular household/farm data necessitate appropriate access controls and anonymization strategies; data products should align with wider communities of practice and be suitable for policy colleagues and partners.
- End-to-end stewardship implications
  - The instrument facilitates assessment of management-level data strategy (coverage, gaps, standards) and operational data practices (collection, QA, harmonisation) essential for effective data stewardship and informed decision-making in agricultural policy and extension.