# Data Generation Methods

## Overview
- Timeframe: Investments in the CAZ from 2007–2014.
- Sources: Conservation International Madagascar, national NGOs, and international agencies’ reports and financial records.
- Key challenge: Inconsistencies in documentation across investment types and implementing agencies hinder accurate data collection, especially for spatial data.
- Spatial resolution: Finest resolution recorded at the fokontany-scale; some investments mapped to the commune.
- Coverage: 629 investments documented; 553 mapped to fokontany; 76 mapped to commune.
- Methods to address gaps: Expert local knowledge from Conservation International Madagascar staff used to fill spatial and temporal gaps and missing information in financial/project reports.
- Dataset contents: Investment attributes including type, project-level activities, counts per year, and investment duration. Total investment costs are not included due to sensitivities around sharing financial information.
- Format: CSV file with 16 relevant columns.

## Data Scope and Content
- Core attributes (16 columns): AppName, IntPart, BenName, BenType, InvestPrjct, InvestType, Ctgry, Fokontany, Commune, District, Year, Scale, BeginDdmmy, EndDdmmy, Duration, Patrolling.
- Data types and units (as described): Object ID (integer), various string fields (investment type, partner name, beneficiary, category, location), Year (integer), BeginDdmmy/EndDdmmy (dates), Duration (months as float), Patrolling (binary integer: 0/1).
- Location fields aligned to administrative boundaries: Fokontany, Commune, District correspond to Madagascar admin level 4 boundaries; FCD field concatenates Fokontany, Commune, District.
- Additional context: Details of related programs (e.g., Conservation Agreements, Conservation Competitions, Node program, social safeguards) describe incentives, grants, or activities linked to livelihoods and forest management.

## Data Structure and Provenance
- Data structure: The dataset is a CSV with a 16-column attribute table.
- Administrative alignment: Names correspond to Madagascar’s administrative boundaries dataset (Fokontany, Commune, District).
- Data provenance: Collected from multiple project documents and financial records from CI Madagascar and partner organizations; spatial data gaps supplemented by local expert knowledge.
- Documentation support: Describes the nature and scope of investments, including type of activities and project-level details.

## Data Quality, Gaps, and Curation
- Documentation inconsistencies: Variability in how investments and implementing agencies are described across sources.
- Spatial data gaps: Some investments could not be tied to fokontany; others to commune; reliance on expert input to fill gaps.
- Mapping outcomes: 629 investments identified; 553 successfully mapped to fokontany; 76 mapped to commune.
- Data curation: Expert staff contributed to filling gaps and harmonizing spatial/temporal information; dataset notes the various incentive programs and types of investments.
- Temporal coverage: Investments span up to 2014, with some programs continuing beyond; data primarily reflects 2007–2014 activities.

## Sharing, Access, and Documentation Considerations
- Sensitivity and restrictions: Total investment costs are not disclosed due to sensitivities around sharing financial information.
- Program context: Includes details on incentives programs (e.g., Conservation Agreements, Node grants) and non-monetary/community-based activities funded by external sources (World Bank, USAID).
- Intended use: Suitable for evaluating effectiveness of conservation investments, understanding spatial distribution, activity types, durations, and patrolling indicators, while acknowledging data gaps and confidentiality constraints.
- Update and governance: Data were compiled for a specific study window; ongoing updates would require reconciliation of sources and continued use of local expertise to fill gaps.

## Acknowledgments and Citation
- Acknowledgments: Thanks extended to individuals who contributed to data compilation and dataset creation.
- Citation: Tabor, K., K. Jones, J. Hewson, A. Rasolohery, A. Rambeloson, T. Andrianjohaninarivo, and C. Harvey (submitted Nov 2016). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.