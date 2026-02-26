# Data Generation Methods

- Overview
  - Collected details on all CAZ investments from 2007-2104 from Conservation International Madagascar, national NGOs, and international agencies.
  - Faced inconsistencies across documentation, especially for spatial location of communities; finest spatial resolution recorded at fokontany scale.
  - Documented 629 investments; only 553 mapped to a fokontany, 76 mapped to a commune.
  - Filled gaps in spatial and temporal information using expert local knowledge from Conservation International Madagascar staff.
  - Included investment attributes such as type, project activities, number of investments per year, and investment duration. Total investment costs are not included due to sensitivities.

- Spatial Data and Geography
  - Spatial resolution is fokontany (finest), with some investments mapped to communes.
  - Administrative boundaries referenced: fokontany, commune, and district (Boundaries dataset used: Madagascar Admin Level-4 boundaries).
  - Fokontany-Commune-District concatenation (FCD) provided for reference.
  - Scale field indicates the data resolution; BeginDdmmy and EndDdmmy provide the investment duration dates.

- Data Structure and Attributes
  - Data format: CSV file with 16 relevant columns:
    - AppName, IntPart, BenName, BenType, InvestPrjct, InvestType, Ctgry, Fokontany, Commune, District, Year, Scale, BeginDdmmy, EndDdmmy, Duration, Patrolling
  - FCD: Concatenated string of Fokontany, Commune, District used for linkage to administrative boundaries.
  - Additional contextual notes describe the types of investments and activities (e.g., Conservation Agreements, Conservation Competitions, Node program, social safeguard investments).

- Data Gaps, Limitations, and Quality Considerations
  - Documentation inconsistencies and data stored across multiple sources posed challenges for data accuracy.
  - Spatial data gaps filled with input from local staff; some investments could not be precisely localized at the fokontany level.
  - No monetary investment costs included due to sensitivities; data focuses on types, timing, locations, and activities.
  - Some investments have longer time frames and involve broader NGO or government programs, with cumulative impacts difficult to parse.

- Data Sources and Context
  - Investments originate from varied programs and funding streams (World Bank, USAID, IDA credits) and include incentives, direct implementation projects, and beekeeping/farming training under various programs.
  - Notable program types and periods:
    - Conservation Agreements and Conservation Competitions (incentive payments or rewards for livelihoods activities).
    - Node program (small grants for community conservation activities; TG contracts prior to 2007).
    - Social safeguard investments (since 2014) targeting vulnerable communities.
    - Direct implementation projects funded by external agencies (e.g., irrigation, agriculture improvements).
  - The dataset supports evaluation of conservation investments’ effectiveness in reducing deforestation and fires (as per cited study).

- Practical Implications for GIS
  - Enables map-based visualization of investment distribution across fokontany, communes, and districts.
  - Can be joined with admin boundary datasets via FCD or Fokontany/Commune/District fields for spatial analysis.
  - Useful for time-based GIS analyses using BeginDdmmy, EndDdmmy, and Year to visualize investments over time.
  - Absence of financial totals means analyses rely on categorical and temporal attributes rather than cost-based metrics.
  - Requires careful handling of spatial uncertainties due to inconsistent documentation and partial localization.

- Citation and Acknowledgments
  - Source: Tabor, K., et al. (submitted Nov 2016). Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar.
  - Acknowledgments to researchers who contributed data compilation and initial investments database.