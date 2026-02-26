# Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar

## Overview
- Compilation of all CAZ investments from 2007 to 2014 from multiple sources (Conservation International Madagascar, national NGOs, international agencies).
- Aim to analyze how investments correlate with deforestation and fire reduction; investments include a mix of monetary and non-monetary incentives, as well as capacity-building activities.
- Data limitations include sensitivities around sharing total investment costs.

## Data Collection and Sources
- Primary sources: reports and financial records from Conservation International Madagascar, national NGOs, and international agencies.
- Documentation inconsistencies: differences in investment types and implementing agencies posed challenges for accurate data collection.
- Use of expert local knowledge (Conservation International Madagascar staff in CAZ) to fill gaps in spatial and temporal information and in missing details from partner reports.

## Spatial and Temporal Coverage
- Finest spatial resolution: fokontany-level (administrative level 4 in Madagascar); some investments mapped to communes when fokontany data unavailable.
- Temporal coverage: investments recorded from 2007 through 2014 (note: the text shows 2007-2104, which appears to be a typographical error; the intended period is 2007-2014).
- Total investments documented: 629; 553 mapped to a fokontany; 76 mapped to a commune.
- Spatial linkage relies on an administrative boundaries dataset for fokontany/commune/district.

## Dataset Structure and Variables
- File format: CSV with 16 relevant columns.
- Key columns include:
  - AppName: Investment type (string)
  - IntPart: Implementing partner (string)
  - BenName: Beneficiary name (string)
  - BenType: Beneficiary type (string)
  - InvestPrjct: Investment name (string)
  - InvestType: Investment type (string)
  - Ctgry: Description of activities (string)
  - Fokontany: Fokontany name (string)
  - Commune: Commune name (string)
  - District: District name (string)
  - Year: Start year of investment (integer)
  - BeginDdmmy / EndDdmmy: Start and end dates (date)
  - Duration: Length of investment (months, float)
  - Patrolling: Whether patrolling activities occurred (binary: 0/1)
  - FCD: Concatenated string of Fokontany, Commune, District
- Administrative names align with Madagascar’s boundary dataset (level 4).

## Investment Attributes and Types
- Inclusions:
  - Conservation Agreements and Conservation Competitions: incentives with payments or non-monetary rewards for livelihood projects (livestock, infrastructure, rice cultivation).
  - Direct implementation projects: funded by IDA World Bank credit; no monetary incentives to communities; implemented by Conservation International-Madagascar to improve small-scale agriculture and irrigation.
  - Node program: small-community grants for forest restoration, management, beekeeping and farming; linked to communities with forest ownership under a Transfer de Gestion (TG) contract.
  - Social safeguard investments: started in 2014; payments for sustainable livelihoods to at-risk communities due to CAZ protections.
  - Other multi-year investments: typically led by national NGOs with funding from World Bank and USAID; included patrolling and capacity-building for natural resource management.
- Note: All TGs were signed before 2007 and undergoing renewal by 2013-2014 within the study period.

## Data Quality, Gaps, and Handling
- Gaps addressed with expert local input to fill spatial and temporal information and to supplement missing reports.
- Spatial resolution limited to fokontany or commune when finer data not available; some investments lack precise location details, affecting granularity.
- Financial data: total investment costs not included due to sensitivities; dataset focuses on investment attributes and timing rather than total monetary value.

## Data Usage and Implications
- Dataset designed to support evaluation of conservation investments’ effectiveness in reducing deforestation and fires within the CAZ.
- Enables analysis of investment type, timing, location, and activity scope to identify patterns and potential correlations with landscape outcomes.
- Findings rely on robust data management, transparent provenance, and triangulation with local expertise to ensure accurate interpretation.

## Provenance and Acknowledgments
- Data compilation supported by contributions from H. Ramiaramanana, A. Ravelomanantsoa, and N. Ralefomanana for initial investments database.
- Cited in: Tabor et al., Evaluating the Effectiveness of Conservation Investments in Reducing Deforestation and Fires in Ankeniheny-Zahemena Corridor, Madagascar (submitted Nov 2016, PlosOne).