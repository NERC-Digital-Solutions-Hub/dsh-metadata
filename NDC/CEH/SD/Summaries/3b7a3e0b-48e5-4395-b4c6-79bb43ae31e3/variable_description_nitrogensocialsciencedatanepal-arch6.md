# Variable description

- Purpose and scope
  - Part of a harmonised SANH Household Survey aimed at understanding fertilizer use and nitrogen-use efficiency (NUE) at the household and farm level across Bangladesh, India, Maldives, Pakistan, and Sri Lanka.
  - Captures detailed labour inputs and wages, farm and plot characteristics, crop production, fertilizer and pesticide use, irrigation, mechanisation, livestock, information sources, adoption drivers/barriers, and household expenditure/assets.
  - Includes season-specific (e.g., Season 1, Season 2) and multi-country comparability to enable cross-country NUE analyses.

- Data structure and organization
  - Highly nested, multi-level design:
    - Household and individual (core units), with farm-level data nested under households.
    - Farm data further broken into plots, crops, seasons, and activities.
    - Seasonal repetition (Season 1, Season 2, etc.) with season-specific variables and codes.
  - Large set of coded variables (e.g., N6xxx, N7xx, N12x, N14x, etc.) covering time use, wages, labour hours by activity, mechanization, irrigation, input use, yields, subsidies, and more.
  - Rich payload includes both quantitative measures (hours, wages, costs, yields) and qualitative indicators (information sources, opinions, adoption attitudes).

- Key thematic data areas and example variables
  - Labour and time use
    - Season-specific hours spent on activities (e.g., land preparation, seed, weeding, planting, fertilizing, transplanting, water management, harvesting) and household vs hired labour (HM vs HL).
    - Total labour hours per crop/season (e.g., N610TotalS12, N610TotalS21, N610TotalS22, etc.).
    - Labour supply counts by gender (e.g., N621MaleS1, N622FemaleS1, etc.) and season-specific labour force data.
  - Wages and costs
    - Average wages by activity and labour type (e.g., N631LandPrepHMS11, N632SeedHLS11, N633WeedingHLS11, etc. for season 1 and season 2).
    - Total land preparation costs and mechanization costs (e.g., N69WCOSTS11–N69WCOSTS24, N631LandPrepWAGES21, etc.).
  - Crop, plot, and input data
    - Crop codes per season (e.g., CropcodeLABS11/12/21/22/23/24) and crop inventories per plot/season.
    - Plot- and crop-level input data (synthetic vs organic fertilizer use, seed sources, yields, input costs, subsidies).
  - Irrigation and water management
    - Season-specific irrigation data, water sources, pricing mechanisms, and payments (e.g., N71AcessS11, N72DIrrigateS11, N74WaterMgtS11, N78PayS11, N79SourceS11; similarly for other seasons).
    - Rice-specific water management methods and puddling questions (e.g., N74WaterMgtS11; N75PuddleS11).
  - Mechanisation and equipment
    - Level of mechanization for land preparation, seed sowing, fertilizer application, irrigation, and harvesting (e.g., N681LandprepS11, N682SeedS11, N683FertilizerS11, N684IrrigS11, N685Harvesting1–N685Harvesting4).
    - Types of machinery used and related costs (e.g., N66UsemachS11, N67TypesS11, N69COSTS21–N69COSTS24).
  - Pesticides, IPM, and decision-making
    - Pesticide use, types (farm-made vs manufactured), application frequency, costs, and IPM techniques (e.g., N81UsePesticideS1, N82TypeS21, N86UseIPMS21).
    - Fertiliser decision processes, sources of information, and record-keeping (e.g., N1081Decisionsonsyntfert1, N104Fertinforank1, N105Whatpreventbetterinfo1, N1010Keeprecordyield1).
  - Livestock and other farm activities
    - Livestock ownership by species, weeks spent on farm, reasons for keeping animals, and movement off-farm (e.g., N91Raisedlivestock, N92Animalspeciesown1–N95IAnimalsleavefarm1, etc. with multi-year extensions).
  - Household socioeconomics and assets
    - Expenditure categories (food, electricity, fuel, transport, health, education, etc.), annual and monthly figures, and asset ownership (e.g., N1311Avgfoodexpendmonth, N132xxExpendyear1–N13299Othersexpendyear2, N141Ownhouseyoulive1–N149Haveaccesstointernet1, N410Ownapowertiller1).
    - Housing characteristics and utilities (floor material, lighting, drinking water, transport, internet access) across waves (e.g., N1411Ownhouseyoulive1, N143Materialofthefloor1, N146Sourceofdrinkingwater1, N149Haveaccesstointernet1).
  - Information sources, guidance, and demonstrations
    - Exposure to and use of decision-support tools, green manures, agroforestry, anaerobic digestion, drainage practices, foliar fertilisers, and other innovations (e.g., N1101DecisionsuportHeard, N1102GreenmanureUsing, N1105DrainageUsing, N1106FoliarUsing1, N1107OtherUsing1).
  - Subsidies and policy context
    - Direct subsidies for fertilisers, machinery, irrigation, output prices, seeds, and others (e.g., SubsidySynFert, SubsidyAgricMac, SubsidyIrrig, SubsidyOutputsup, SubsidySeed, SubsidyOthers in later waves).

- Country harmonisation and data quality
  - Instrument designed for cross-country comparability under the SANH WP 1.3 framework.
  - Harmonisation considerations include unit consistency (areas, weights, prices), crop-code mappings, and handling missing values across seasons and countries.
  - Data quality features referenced include enumerator notes and potential QC flags to guide data cleaning and reliability assessment.

- Data use and potential outputs for Data Support
  - Enable exploration of NUE and sustainable nitrogen practices at household/farm level.
  - Analytics and dashboards to compare NUE patterns across seasons, crops, plots, and districts; explore adoption drivers/barriers and subsidy impacts.
  - Plot-level productivity analyses linked to input costs; cross-country NUE comparisons and cross-season trend analyses.
  - Self-serve data products such as district-, country-, season-, and crop-level summaries; visualisations of fertilizer type usage, subsidy uptake, and adoption drivers.
  - Data preparation and governance considerations include documenting assumptions for multi-season and multi-country aggregations, ensuring metadata transparency, and enabling reproducible cross-country analyses.

- Analysts and data engineers considerations
  - Expect complex multi-way joins across seasonal datasets (household, farm, plots, crops, activities) and cross-country codes.
  - Maintain strict unit consistency (area, weight, price) and ensure accurate crop-code mappings.
  - Leverage enumerator notes and QC flags to assess reliability and identify cleaning steps.
  - Provide clear documentation and data dictionary to support cross-country comparisons and reproducible analyses.