# Data Generation Methods

## Overview
- Timeframe: 2007-2104 (as stated), collecting investments in the Ankeniheny-Zahemena Corridor (CAZ) from Conservation International Madagascar, national NGOs, and international agencies.
- Purpose: compile investments to support evaluation of conservation investments’ effectiveness in reducing deforestation and fires.
- Scale and mapping: 629 investments identified; finest spatial resolution at the fokontany level; 553 investments mapped to a fokontany; 76 mapped to the surrounding commune.
- Data gaps and augmentation: gaps filled using expert local knowledge from Conservation International Madagascar staff to complete spatial and temporal information and missing details in partner reports.
- Cost data: total investment costs are not included due to sensitivities around financial information from various institutions.

## Data collection and challenges
- Inconsistencies across documentation in investment types and implementing agencies hinder data accuracy.
- Spatial data challenges: locating communities and determining precise investment locations; resolution limited to fokontany-scale.
- Documentation gaps required expert input to fill spatial and temporal missing data.
- Data discipline: attributes captured include investment type, activities, annual counts, and investment duration.

## Data captured and structure
- Data format: csv file.
- Core attributes (16 relevant columns): AppName, IntPart, BenName, BenType, InvestPrjct, InvestType, Ctgry, Fokontany, Commune, District, Year, Scale, BeginDdmmy, EndDdmmy, Duration, Patrolling.
- Additional field: FCD, a concatenated string of Fokontany, Commune, and District.
- Spatial and administrative naming aligns with Madagascar’s admin Level 4 boundaries dataset.

## Data coverage and context
- Incentive and project types included:
  - Conservation Agreements and Conservation Competitions (incentive payments or rewards for livelihood projects).
  - Direct implementation projects funded by IDA/World Bank and implemented by CI-Madagascar (non-monetary activities to improve agriculture and irrigation).
  - The Node program (small grants to communities for conservation activities, often linked to forest ownership via Transfer de Gestion contracts signed before 2007; renewals around 2013-2014).
  - Social safeguard investments starting in 2014 (payments for sustainable livelihoods for at-risk communities).
  - Other investments by national NGOs with WB/USAID funding (e.g., patrolling, capacity building for natural resource management).
- Activities documented include patrolling, forest management, capacity building, beekeeping, and farming support.
- Data provenance notes: names of administrative units correspond to official Madagascar admin boundaries; dataset citations include the PlosOne study evaluating conservation investments (Tabor et al., submitted Nov 2016).

## Provenance and acknowledgments
- Citation: Tabor, K. et al. (submitted 2016) "Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar."
- Acknowledgments: gratitude to individuals who assisted with research and data compilation.

## Implications for Data Leaders
- Emphasizes the importance of building a cohesive data system across partners, including standardized investment attributes, consistent spatial resolution, and clear metadata.
- Highlights data governance considerations:
  - Managing data sensitivities around financial information (hence omission of total costs).
  - Addressing data quality and consistency across multiple sources and implementing agencies.
  - Ensuring discoverability and updatability of investment data, including provenance and context for each record.
- Opportunities to improve:
  - Harmonize investment categories and spatial granularity.
  - Improve documentation to reduce reliance on expert recollection.
  - Expand data to capture costs where permissible and to document data quality and coverage over time.
  - Leverage such datasets to analyze spatial-temporal dynamics of conservation investments and their relationship to outcomes like deforestation and fires.