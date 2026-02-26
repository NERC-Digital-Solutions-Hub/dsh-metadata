# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Aim
- Assess effectiveness of conservation investments in reducing deforestation and fires within the Ankeniheny-Zahemena Corridor (CAZ), Madagascar.
- Compile and standardize data to enable monitoring and policy scrutiny over time.

## Data Generation Overview
- Collected details on all CAZ investments from 2007 to 2014 using reports and financial records from multiple sources (Conservation International Madagascar, national NGOs, international agencies).
- Identified and attempted to reconcile inconsistencies in investment types and implementing agencies.
- Used expert local knowledge to fill gaps in spatial and temporal information for partner investments and reports.

## Sources, Coverage, and Spatial Resolution
- Sources: Conservation International Madagascar, national NGOs, international agencies; includes Conservation Agreements, Conservation Competitions, IDA World Bank-funded activities, and USAID-funded activities.
- Coverage: Investments across CAZ during 2007–2014; spatial data finest at the fokontany level; some investments mapped to commune when fokontany-level mapping was not possible.
- Total investments recorded: 629; 553 mapped to a fokontany; 76 mapped to a commune.
- Spatial boundary reference: Fokontany, Commune, and District correspond to Madagascar admin level 4 boundaries.

## Data Structure and Attributes
- Data format: CSV file with 16 relevant columns.
- Key columns (examples):
  - AppName: Investment type
  - IntPart: Implementing partner
  - BenName, BenType: Beneficiary and type
  - InvestPrjct, InvestType: Investment name and type
  - Ctgry: Description of activities
  - Fokontany, Commune, District: Geographic entities
  - Year, BeginDdmmy, EndDdmmy: Timeframe
  - Duration: Length of investment (months)
  - Patrolling: Presence of patrolling activities (binary)
  - Scale: Resolution of investment data
  - FCD: Concatenated Fokontany-Commune-District string
- Data note: The dataset intentionally excludes total investment costs due to sensitivity around sharing financial information.

## Temporal and Program Context
- Programs and incentives documented:
  - Conservation Agreements and Conservation Competitions (incentive payments or non-monetary rewards for livelihood projects such as livestock, infrastructure, rice cultivation).
  - Direct implementation projects funded by IDA/World Bank and implemented by CI-Madagascar for agriculture and irrigation improvements.
  - The Node program: small community grants to support conservation activities (e.g., forest restoration, management, beekeeping, farming); often linked to communities with transferred forest management rights (TGs).
  - TGs: existing pre-2007 contracts renewed around 2013–2014.
  - Social safeguards investments began in 2014, targeting at-risk livelihoods due to CAZ establishment.
  - Other long-duration investments by national NGOs, World Bank, and USAID covering patrolling, capacity building, and NRM activities.

## Data Use, Quality, and Gaps
- Primary use: Support standardized monitoring of conservation investments and their geographic distribution over time.
- Quality considerations:
  - Documentation inconsistencies across investment types and implementing agencies.
  - Spatial data gaps requiring expert local input to fill gaps.
  - Finest spatial resolution limited to fokontany when available; some data only to commune.
- Data modification and QA: Expert staff contributed local knowledge to reconstruct missing spatial and temporal details.

## End Notes and Citation
- Publication context: Data underpinning the evaluation of conservation investments’ effectiveness in reducing deforestation and fires in CAZ (cited as PlosOne manuscript, 2016).
- Acknowledgments: Thanks to individuals contributing data compilation and research efforts.