# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Objective and scope
- Documents investments in the Ankeniheny-Zahemena Corridor (CAZ) from 2007–2014 to evaluate effectiveness in reducing deforestation and fires.
- Aims to support monitoring and inform future decision-making on conservation investments.

## Data sources and collection process
- Sources include Conservation International Madagascar, national NGOs, and international agencies.
- Key challenges: inconsistencies in documentation across investment types and implementing agencies; gaps in spatial and temporal information.
- Expert local knowledge from Conservation International Madagascar staff used to fill spatial/temporal gaps and missing data.
- Investment attributes captured include type, project-level activities, annual counts, and investment durations.
- Total investment costs are not included due to sensitivities around sharing financial information.

## Data attributes and structure
- Dataset is a CSV with 16 relevant columns: AppName, IntPart, BenName, BenType, InvestPrjct, InvestType, Ctgry, Fokontany, Commune, District, Year, Scale, BeginDdmmy, EndDdmmy, Duration, Patrolling; plus a consolidated FCD field (Fokontany-Commune-District).
- Field descriptions and data types provided (e.g., strings, integers, dates, months duration, binary for patrolling).
- Investment attributes recorded: type of investment, activities, yearly counts, duration.
- Data excludes total investment costs.

## Spatial resolution and geography
- Finest recorded spatial resolution is at the fokontany level (Administrative Boundaries Level 4 for Madagascar).
- Where fokontany data were unavailable, investments were mapped to the containing commune.

## Temporal coverage and investment types
- Time frame: 2007–2014.
- Investment programs described:
  - Conservation Agreements and Conservation Competitions (incentive payments or non-monetary rewards for livelihoods projects).
  - Direct implementation projects funded by IDA World Bank and implemented by Conservation International-Madagascar (no monetary incentives to communities).
  - Node program (small grants for community-led conservation, often linked to forest ownership transfers under a Transfer de Gestion).
  - Social safeguard investments (began in 2014; payments for sustainable livelihoods to at-risk communities).
  - Other longer-term investments implemented by national NGOs with World Bank and USAID funding (e.g., patrolling, capacity building).

## Data governance and metadata considerations
- Data quality and usability supported by field notes and expert validation but hampered by inconsistent documentation and metadata gaps.
- Spatial and temporal data gaps addressed through local expertise, highlighting the need for robust metadata and data provenance.
- Some data sharing considerations due to sensitivity of financial information; total costs not disclosed.
- Data intended to be used for monitoring outcomes and informing future conservation investments; underlying data and provenance are acknowledged.

## Data usage and dissemination
- Data used to evaluate the effectiveness of investments in reducing deforestation and fires; findings prepared for publication (PlosOne, submitted 2016).
- Acknowledgments note contributions from researchers and data compilation teams.