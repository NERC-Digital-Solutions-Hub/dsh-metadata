# NPPMF_PollinatorPilot_2015

## Overview
- A 2015 pollinator monitoring pilot across 14 UK sites, with four sampling rounds from April to August 2015 (weather-led extensions common).
- Half the sites in agricultural habitats, half in semi-natural habitats.
- Aimed to evaluate sampling methods, recorder capacity (researchers, consultants, volunteers), gather method/protocol feedback, and generate implementation cost and support data.

## Aims and Scope
- Compare sampling methods for complementarity and ability to detect trends over time.
- Assess how different recorder groups implement protocols and how this affects data.
- Gather feedback on survey methods/protocols, including usability and willingness to scale.
- Generate detailed information on implementation costs and support requirements for each method or protocol combination.

## Recorder Types and Roles
- Researcher protocol: paid, trained staff with pollinator sampling/ID expertise (primarily at research institutes).
- Consultant protocol: professional taxonomic experts (England and Wales); includes unpaid amateur contributors via recording schemes.
- Volunteer protocol: citizen scientists (non-experts) collecting data for 12 of 14 sites; species-level ID limited; broad group classifications used.
- Across protocols, data were categorized into broad taxonomic groups; researchers/consultants collected species-level data for bees and hoverflies, while volunteers used broad groups and provided an identification sheet to aid classification.

## Sampling Methods and Protocols
- Pan traps: 5 stations per site, one trap at each transect start; researchers used pan traps (volunteers could assist under supervision); colors: blue, white, yellow; water and detergent solution.
- Fixed transects pollinator surveys: five 200 m transects per site; all recorder types could conduct; 1 m width.
- Timed focal flower observations (FFOs): standardized 10-minute observations on focal plants within a 0.5 x 0.5 m quadrat; repeated twice per site visit.
- Standardised free searches: two 1000 m² fixed areas for 30 minutes; used by consultants (spatially standardized); researchers specified roles regarding use.
- Floral resource surveys on transects: 3–6 one-metre quadrat samples along transects to assess species-level floral abundance; plus an overall scaled flower abundance estimate across the transect.
- Floral transects and quadrats: floral surveys conducted to quantify flower availability around transects and at pan trap locations.

## Study Design and Site Protocol
- The protocol defined a site as a 1 km² Ordnance Survey grid square to standardize area and align with other monitoring schemes.
- Five pan trap stations and five transects per grid square; transects included a mix of straight and linear-feature-following routes.
- Transect sections and floral resources were recorded after insect surveys; follow-up floral observations occurred between transects.
- All recorder types walked the same transect routes; floral resource surveys were conducted per transect.

## Data Collected and Files
- SiteVisitConditions (NPPMF_PollinatorPilot_2015_SiteVisitConditions.csv): date, recorder, weather, transect details, habitat codes, and notes per site visit.
- FreeSearchConditions (NPPMF_PollinatorPilot_2015_FreeSearchConditions.csv): environmental and methodological details for consultant free searches, including habitat codes and expert levels.
- FFOBConditions (NPPMF_PollinatorPilot_2015_FFOBConditions.csv): timings, weather, focal plant species, floral units, and density scoring for focal floral observations.
- AllInsects (NPPMF_PollinatorPilot_2015_AllInsects.csv): insect records across all four methods (transects, pan traps, focal observations, free searches); includes site, round, protocol, recorder, method, taxonomic group, genus, species, full name, date ID, and count.
- FloralTransects (NPPMF_PollinatorPilot_2015_FloralTransects.csv): plant species, floral unit counts, and abundance scores for transect-based flower surveys.
- FloralQuadrats (NPPMF_PollinatorPilot_2015_FloralQuadrats.csv): 1 m² quadrat-based flower counts around transects/pan traps.
- Survey Evaluation (questionnaire data): recorder responses on protocol-related questions (strongly agree to strongly disagree) with comments.
- Quality control: No formal quality control applied across the datasets.

## Data Governance, Metadata, and Quality
- The pilot explicitly captures protocol-level data to inform measurement choices and feasibility for different recorder types.
- Noted lack of formal quality control across datasets, highlighting metadata completeness and data quality considerations for monitoring frameworks.
- Data management considerations include consistent site definitions (1 km² grid), standardized transect/pan trap layouts, and clear metadata fields (weather, habitat codes, recorder identity).

## Implications for Monitoring Frameworks
- Demonstrates the value of standardized, cross-recorder protocols to compare methods and assess scalability in policymaking contexts.
- Highlights that different recorder types produce different data resolutions (species-level vs broad-group), which affects trend detection and indicators.
- Provides a structured approach to capturing implementation costs and required support, essential for budgeting and governance in monitoring programs.
- Reveals potential data governance barriers, such as data sharing requirements and metadata completeness, that need to be addressed when designing open, transparent monitoring datasets.

## Challenges and Lessons for Authors of Monitoring Frameworks
- Data availability and standardization: ensuring consistent site definitions and taxonomic resolution across observer groups.
- Data access and timeliness: coordinating data sharing across researchers, consultants, and volunteers.
- Silos and coordination: aligning workflows across organisations and roles to avoid fragmentation.
- Metadata and data transformation: ensuring comprehensive metadata and reducing the burden of data cleaning/formatting.
- Communicating complex findings: balancing detail with clarity for policy decisions and public dissemination.
- Data governance: establishing clear storage, sharing, and update procedures to maintain data quality over time.

## Takeaways for Developing Monitoring Frameworks
- Use a multi-recorder approach to test method feasibility, data quality, and user experience across researcher, professional consultant, and citizen-science inputs.
- Standardize spatial units (e.g., 1 km² OS grid) to enable integration with other monitoring schemes and long-term trend analyses.
- Collect comprehensive contextual data (weather, habitat type, transect route) to support robust interpretation and comparability.
- Incorporate evaluation components (recorder feedback) to inform protocol refinement and adoption at scale.
- Plan for data governance and metadata quality from the outset to reduce barriers to data sharing and reuse.