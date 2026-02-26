# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Data Generation Methods
- Collected data on all CAZ investments from 2007 to 2104 from multiple sources: Conservation International Madagascar, national NGOs, and international agencies.
- Faced inconsistencies in documentation across investment types and implementing agencies, complicating data accuracy, especially for spatial data.
- Spatial granularity was at the fokontany level; 629 investments identified, with 553 mapped to a fokontany and 76 mapped to a commune.
- Expert local knowledge from Conservation International Madagascar staff used to fill gaps in spatial and temporal information and in missing financial/report details.
- Recorded investment attributes include type, project-level activities, count per year, and investment duration. The dataset intentionally does not include total investment costs due to sensitivities.
- Data structure includes a concatenated FCD field (Fokontany–Commune–District) based on official admin boundaries dataset.

## Dataset Structure and Units
- Format: CSV file with 16 relevant columns: AppName, IntPart, BenName, BenType, InvestPrjct, InvestType, Ctgry, Fokontany, Commune, District, Year, Scale, BeginDdmmy, EndDdmmy, Duration, Patrolling, plus a concatenated FCD.
- Data types: Object ID (integer), strings for names/types, Year (integer), BeginDdmmy/EndDdmmy (date), Duration (months, float), Patrolling (binary integer 0/1), Scale (string).
- Fokontany/Commune/District names correspond to the Madagascar Administrative Boundaries dataset (Level 4).

## Data Coverage and Sources
- Timeframe: Investments between 2007 and 2014.
- Spatial coverage: Investments localized to fokontany (finest) with many also mapped to communes.
- Data sources include Conservation International Madagascar records, national NGOs, and international agencies; spatial and programmatic details cross-validated with local inputs.

## Data Quality, Gaps, and Limitations
- Primary challenges: inconsistencies in documenting investment types and implementing agencies; patchy data across formats and systems.
- Some investments could not be precisely mapped to the fokontany level and were only linked to communes.
- Financial data: total investment costs are not included due to sensitivities around sharing financial information.

## Content Details and Interpretive Notes
- Describes several investment types and incentive programs:
  - Conservation Agreements and Conservation Competitions: include payments or non-monetary rewards for livelihood-related projects (livestock, infrastructure, rice cultivation).
  - Direct implementation projects: non-monetary or donor-funded activities (World Bank IDA credits) to improve agriculture and irrigation, managed by CI-Madagascar.
  - Node program: small community grants for conservation activities (forest restoration/management, beekeeping, farming); linked to community forest ownership via Transfer de Gestion contracts signed before 2007.
  - Social safeguard investments: began in 2014, targeting at-risk communities to sustain livelihoods amid CAZ protections.
  - Other longer-term investments: typically NGO-led with World Bank/USAID funding, including patrolling and capacity building.
- The dataset captures activities and governance mechanisms but not monetary amounts; it supports analysis of program types, durations, locations, and temporal distribution.

## Potential Uses and Considerations for Data Support
- Enables exploration of where and when investments occurred, what activities were implemented, and which communities were involved.
- Supports self-serve analysis and visualization (e.g., dashboards, charts) for end users in policy or conservation contexts.
- Helpful for assessing alignment of investments with conservation outcomes, while acknowledging gaps in financial data and potential data quality issues.

## Citation and Acknowledgments
- Data and methods described in: Tabor et al. (submitted Nov 2016) PlosOne. Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.
- Acknowledgments to H. Ramiaramanana, A. Ravelomanantsoa, and N. Ralefomanana for data compilation and initial investments database development.