# Variable description

- Purpose and scope
  - Provides detailed variable-level descriptions for a large, harmonised household/farm survey dataset focused on labour inputs, fertilizer use, irrigation, mechanisation, pests, livestock, information sources, adoption drivers, attitudes, expenditures, and assets.
  - Uses a highly granular, repeated-measures structure with season-specific variables and crop-specific codes to support cross-season and cross-crop analysis.

- Data structure and coding
  - Variables are systematically coded with prefixes (e.g., N6xx for labour-related measures, N63x–N79x for labour wages and costs, N64x–N69x for mechanisation and irrigation, etc.).
  - Season-specific data are captured across multiple timepoints (e.g., season 1, season 2, up to season 4 and beyond in later sections), with repeated blocks for crops and activities.
  - Data are organised at multiple levels:
    - Crop/season level (e.g., labour hours by activity per crop per season)
    - Household level (e.g., household labour supply, wages, mechanisation ownership)
    - Plot/field level (e.g., land preparation, irrigation inputs)

- Key thematic variable groups
  - Labour and wages
    - Hours spent by activity by season for household members (HM) and hired labour (HL) (e.g., N610TotalS12, N6111LandPrepHMS21, N631LandPrepHMS21 wages, N632SeedHLS11 wages, etc.)
    - Totals and per-activity wages across multiple seasons (e.g., N631, N632, N633…N6399)
    - Sex, counts of labor supply (e.g., N621MaleS1, N622FemaleS1)
  - Farming operations and timing
    - Land preparation, seed sowing, weeding, planting, fertilizing, transplanting, water management, harvesting (across HM and HL and multiple seasons)
    - Crop codes and crop-specific labour variables (e.g., CropcodeLABS11, CropcodeIRRGS11)
  - Mechanisation and inputs
    - Level of mechanisation for land preparation, sowing, fertiliser application, irrigation, harvesting (e.g., N681LandprepS11, N682SeedS11, N683FertilizerS11, N684IrrigS11, N685Harvesting1)
    - Use of machinery, animal power, and costs (e.g., COSTS, UsemachS, TypesS)
  - Irrigation and water management
    - Water source, pricing mechanism, payments, proportions irrigated, and crop-specific water management methods (e.g., N71AcessS11, N72DIrrigateS11, N74WaterMgtS11, N78PayS11)
  - Pesticides and IPM
    - Pesticide usage, types (farm-made vs manufactured), application frequency, costs, IPM adoption, crop codes (e.g., N81UsePesticideS1, N82Whattypeofpesticides, N86UseIPMS1, Nq8CropCodepestS1)
  - Fertiliser and manure decisions
    - Decisions on synthetic and organic fertilisers, guidance documents, calculators, records of fertiliser use and yields, and decision-support tools (e.g., N1081Decisionsonsyntfert1, N109Keeprecordfertilizer1, N1010Keeprecordyield1, N1101DecisionsuportHeard)
  - Information sources and advisory uptake
    - Exposure to guidance (government, extension, traders, media) and use of decision-support tools (e.g., N2FertInfoFertilizertrader, N1081Decisionsonsyntfert1)
  - Attitudes, risk, and perceptions
    - Likert-scale attitudes toward fertiliser use, risk tolerance, openness to new technologies, soil/weather perceptions (e.g., N122Iampreparedtotakerisk1, N126Ifrequentlytrynew, N123WHATchangehowusefert1)
  - Household economics and assets
    - Expenditures by category (food, electricity, fuel, transport, health, education, etc.) over months/years, and annual expenditures on assets and repairs (e.g., N1311Avgfoodexpendmonth, N1329Fixedassetsexpendyear1)
    - Household ownership and access indicators (e.g., N141Ownhouseyoulive1, N149Haveaccesstointernet1, N410Ownapowertiller1)
  - Other contextual measures
    - Enumerator notes, training attendances, decision-support adoption, crop insurance, loans, financial distance, and season codes (e.g., EnumeratorsnoteP18, N101Attendcropdemo1, N1415Gottheloan1, N1417Havecropinsurance1, N14173Seasoncode1)

- Data quality, provenance, and access
  - The dataset emphasizes data provenance and metadata, with structured quality-control procedures during collection (spot checks, paper back checks, data transfer checks, etc.).
  - Metadata-rich variables and repeated sections support reproducibility and discoverability within data portals.
  - The harmonised, multi-country framework enables cross-country comparisons, but users should account for regional coding differences, boundaries, and potential missingness.

- Analytical opportunities and caveats
  - Suitable for correlational analyses, regression, and predictive modelling of NUE-related outcomes, fertilizer practices, and adoption decisions across households, farms, plots, and crops.
  - The two-season (and multi-season) structure enables analysis of seasonal variation and short-term dynamics in inputs and outputs.
  - Potential challenges include high dimensionality and sparsity for less-represented crops or seasons, regional/generalizability limits (Terai focus), and the need for careful harmonisation when combining country-specific codes and units.