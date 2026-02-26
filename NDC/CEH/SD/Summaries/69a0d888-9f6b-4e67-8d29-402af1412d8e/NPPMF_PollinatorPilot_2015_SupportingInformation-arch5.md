# NPPMF_PollinatorPilot_2015

## Overview
- A pollinator monitoring pilot from 2015, collecting data on pollinating insects, floral resources, and environmental conditions across 14 UK sites over four sampling rounds (April–August 2015).
- Rounds sometimes extended due to weather; roughly half sites in agricultural habitats and half in semi-natural habitats.
- Data collected to compare sampling methods, assess recorder capabilities, gather user feedback, and estimate implementation costs and support needs.

## Dataset scope and sampling design
- Sites: 14 across the UK; 4 sampling rounds within 2015.
- Target outcomes include method complementarity, capacity of recorder groups, user feedback on methods, and cost/support requirements.
- Site square unit: 1 km2 OS grid square used to standardize site definition and sampling scale.
- Each site visit included pan traps, transects, focal floral observations, and standardized free searches, with floral surveys conducted along transects.

## Recorder types and protocols
- Recorder types:
  - Researcher: paid staff with training in pollinator sampling/ID.
  - Consultant: taxonomic experts (England/Wales); represented professional and amateur contributors.
  - Volunteer: citizen scientists; non-experts identifying insects at broad taxonomic levels.
- Taxonomic resolution:
  - Researchers/Consultants: species-level IDs for bees (Bombus, Apis) and hoverflies; some groups identified to species level.
  - Volunteers: broad group classifications only (e.g., bumblebees, honeybees, hoverflies, etc.).
- One-day protocols (~8 hours) for standardized site work, covering pan traps, transects, and floral resource surveys.

## Data files and schemas (key datasets)
- NPPMF_PollinatorPilot_2015_SiteVisitConditions.csv
  - Site, Round, Protocol Type, Recorder, Date Collected, Temperature, transect details, wind, cloud, habitat codes, notes.
  - Quality Control: No specific QC applied.
- NPPMF_PollinatorPilot_2015_FreeSearchConditions.csv
  - Environmental/effort data for consultant-led free searches (area, timing, weather, habitat, expertise, etc.).
  - Quality Control: No specific QC.
- NPPMF_PollinatorPilot_2015_FFOBConditions.csv
  - Timed focal floral observations: timing, weather, focal flower, floral counts by unit, companion flowers.
  - Quality Control: No specific QC.
- NPPMF_PollinatorPilot_2015_AllInsects.csv
  - All insects observed/collected across methods (transects, pan traps, FFOB, free searches); fields include site, round, method, group, genus, species, date identified, count.
  - Quality Control: No specific QC.
- NPPMF_PollinatorPilot_2015_FloralTransects.csv
  - Floral abundance estimates along transects by plant species, unit type, and abundance score.
  - Quality Control: No specific QC.
- NPPMF_PollinatorPilot_2015_FloralQuadrats.csv
  - Flower abundance data around transects/pan traps via 1 m2 quadrats; multiple quadrats per transect.
  - Quality Control: No specific QC.
- PollinatorPilot_2015_SurveyQuestions (illustrative)
  - Questionnaire data capturing recorder feedback on methods (recorder, protocol type, method, question, response, comments).
  - Quality Control: No specific QC.

## Data collection methods and protocols
- Pan trapping: 5 stations per site visit with 3 pans (blue, white, yellow) in each station; used only by researchers (volunteers could observe with researchers).
- Transects: Five 200 m transects per site visit; recording all insects visiting flowers within 1 m of transect.
- Timed focal floral observations (FFOs): 10-minute focal plant observations within a 0.5 x 0.5 m quadrat, repeated per site visit; two focal observations per site.
- Standardised free search: 30 minutes in good habitats, with fixed areas; conducted by consultants and volunteers in some configurations; not conducted by researchers alone.
- Floral surveys: Transects accompanied by floral surveys with quadrats (1 m2) to estimate floral abundance and diversity; some measures included flower density scoring.
- Floral resource surveys: Quantification of floral resources along each transect (quadrats at 0, 50, 100, 150, 200 m).
- Site and transect consistency: Transects followed consistent routes within each site visit; location of transects/pan traps designated at initial site visit but movable if conditions required (e.g., safety, grazing).

## Data quality, provenance, and limitations
- No explicit quality control applied across datasets (noted in each file’s QC section).
- Data resolution varied by recorder type (species-level IDs for researchers/consultants vs broad groups for volunteers); some fields may be NA where IDs were not determined.
- Data are observational and protocol-specific; some metadata (e.g., transfer/logistics) existed but might require harmonization for cross-study reuse.
- BeeWalk habitat codes and collaboration with wider schemes (WCBS, NPMS) suggest potential for cross-walks but require careful mapping.

## Governance, access, and reuse considerations
- Provenance: Data originate from a UK pollinator pilot (2015) with explicit intentions for comparing methods and understanding implementation costs.
- Metadata and standardization: BeeWalk-like habitat codes used; standardization advisable for reuse with other monitoring schemes.
- Data licensing and sharing: Not specified in the provided text; practitioners should verify license, usage rights, and any embargo or access constraints before reuse.
- Updates and maintenance: Protocols support updates across rounds; documentation should capture any adjustments to transect routes or site conditions over time.
- Documentation needs: Comprehensive data dictionaries (as provided) and crosswalks to other pollinator datasets would aid discoverability and interoperability.

## Challenges and considerations for Data Stewards
- Incomplete user needs picture: Align future data releases with explicit user needs and typical reuse workflows.
- Timeliness and completeness: Ensure timely ingestion and metadata completeness across all recorder types and methods.
- Standards and interoperability: Harmonize disparate data (species-level vs group-level identifications) and align with existing biodiversity data standards.
- Heterogeneous systems and formats: Manage multiple protocols and data schemas; provide data transformation pipelines and clear mapping guides.
- Large dataset management: Facilitate efficient transfer and storage, especially with rich metadata and multiple files per site.
- Legacy/updated data handling: Plan for updates and versioning as protocols evolve or follow-up surveys are added.

## Summary for Data Stewardial action
- Ensure thorough, consistent metadata documentation across all files; map species-level IDs to a common taxonomy where possible.
- Document data licensing, access rights, and any embargoes; provide guidance on reuse and attribution.
- Develop a data dictionary and crosswalk to standard monitoring schemes (e.g., WCBS, NPMS) to improve interoperability.
- Create data processing workflows to harmonize fields (e.g., habitat codes, units, time formats) and handle NA values.
- Establish QC processes and an audit trail for future updates to maintain data quality.
- Prepare a data release package with example queries and usage notes to aid discovery and reuse by researchers, policymakers, and citizen science initiatives.