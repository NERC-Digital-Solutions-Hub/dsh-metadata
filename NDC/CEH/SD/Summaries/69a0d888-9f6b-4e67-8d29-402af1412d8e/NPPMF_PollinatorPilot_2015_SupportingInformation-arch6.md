# NPPMF_PollinatorPilot_2015_SiteVisitConditions.csv

## Overview
- The text describes a pollinator monitoring pilot conducted in 2015 across 14 UK sites, covering four sampling rounds from April to August 2015.
- Half of the sites were agricultural, half semi-natural; rounds were often extended due to weather.
- Aimed to compare sampling methods, evaluate recorder groups, gather feedback on methods, and generate information on implementation costs and support.

## Study design and aims
- Four sampling rounds: Round One (27 April–10 May), Round Two (1–14 June), Round Three (6–19 July), Round Four (17–30 August).
- Objective categories:
  - Compare sampling methods for complementarity and power to detect trends.
  - Compare capacity of different recorder groups (Researcher, Consultant, Volunteer) to implement methods and data generated.
  - Gather feedback on survey methods and willingness to scale up in wider monitoring.
  - Generate detailed information on implementation costs and support needs for each method or combination.

## Recorder types and data resolution
- Researcher protocol: paid staff with training in pollinator sampling and identification.
- Consultant protocol: taxonomic experts for all English and Welsh sites (including amateur contributors via BWARS and related schemes).
- Volunteer protocol: non-expert public volunteers (citizen scientists) collecting data at 12 of 14 sites; no species-level identification for all groups.
- Taxonomic resolution:
  - Researchers and Consultants: species-level for bees (including bumblebees and honeybees) and hoverflies; other groups broadly classified.
  - Volunteers: broad-group classifications only.
- Identification aids: volunteers received an insect identification sheet to distinguish bees vs hoverflies and broad taxonomic groups.

## Sampling methods and protocols
- Methods used across recorder types:
  - Pan trapping (five stations per site, each with three pans; specialist use only by Researcher; volunteers could participate with researcher supervision).
  - Fixed transects pollinator surveys (five transects per site, 200 m each; 1 m width; all recorder types could participate, with varying degrees of involvement).
  - Timed focal flower observations (FFO): standardized 10-minute observations on focal plants within 0.5 x 0.5 m quadrats; conducted twice per site visit.
  - Standardised free search pollinator surveys in good habitats: two fixed areas per site (1000 m2 total) for 30 minutes (or longer arrangements); consultants and volunteers participated; researchers did not perform standardised free searches.
  - Floral surveys along transects: quadrat-based floral abundance counts (1 m2 quadrats) around transects; open to researchers; two methods to estimate floral abundance (within-quadrat counts and transect-wide estimates).
- Focus on enabling self-service data exploration through products like dashboards and reports, with potential early prototypes shared for feedback.

## Site and route logistics
- A single-day protocol designed to be completed within ~8 hours per site.
- A 1 km2 OS grid square defined as a site unit for standardization and comparability with other schemes (WCBS, NPMS).
- Five pan trap stations and five 200 m transects arranged roughly diagonally through each grid square.
- Transect routes: three straight-line transects and two transects that follow linear features (paths, hedges, field margins).
- Transects’ exact location maintained but movable if conditions (grazing, safety) required.
- Floral resource surveys conducted after insect surveys along each transect.
- FFOb and free-search observations scheduled between transects and directed by recorder.

## Data files and contents (data dictionary highlights)
- NPPMF_PollinatorPilot_2015_SiteVisitConditions.csv
  - Contains: Site, Site Type (Agri or SemiNat), Round, Protocol Type, Recorder, Date Collected, Temperature, Section No, Transect Type, Start/End Times, Wind, Cloud, Sun, Habitat Codes (BeeWalk), Notes.
  - Quality control: No specific quality control applied.
- NPPMF_PollinatorPilot_2015_FreeSearchConditions.csv
  - Contains environmental and effort data for consultant free searches.
  - Columns include Site, Round, Area Code, Recorder, Start/End Times, Temp, Cloud, Wind, Area Size, Time allocations, %Time spent on activities (sweep netting, spot recording, targeting flowers), Estimated specimens for ID, Habitat Codes, and Expertise levels for Bumblebee, Solitary Bees, Hoverflies.
  - Quality control: No specific quality control applied.
- NPPMF_PollinatorPilot_2015_FFOBConditions.csv
  - Data on timings, environmental conditions, and floral resources for all focal floral observations (FFOs).
  - Includes Site, Round, Protocol Type, Recorder, Quadrat No, Date, Start/End Times, Temp, Cloud, Wind, Focal Flower (and counts by floral unit), Other Flowers and counts, and Flower Density Score.
  - Quality control: No specific quality control applied.
- NPPMF_PollinatorPilot_2015_AllInsects.csv
  - All insects recorded across four sampling methods (transects, pan traps, FFOs, free searches).
  - Columns include Site, Round, Protocol Type, Recorder, Method, Section No, Free Search Number/FFO Quadrat, Group (broad taxa), Genus, Species, Full Name, Date ID, Number.
  - Quality control: No specific quality control applied.
- NPPMF_PollinatorPilot_2015_FloralTransects.csv
  - Floral abundance estimates along transects.
  - Includes Site, Round, Protocol Type, Recorder, Plant Species, Unit (H, S, Maj U, Min U), Abundance Score, Median Abundance, Quality Control: No.
- NPPMF_PollinatorPilot_2015_FloralQuadrats.csv
  - Flower abundance data for 3–6 1 m2 quadrats around transects and pan traps.
  - Columns: Site, Round, Recorder, Quadrat, Plant Species, Unit.
  - Quality Control: No specific quality control applied.
- Protocol questionnaire or feedback data (qualitative/quantitative evaluation)
  - Columns include: Recorder, Protocol Type, Method (Overall), Question, Strongly Agree, Agree, Neither/Nor, Disagree, Strongly Disagree, Comments.
  - Quality Control: No specific quality control applied.

## Data quality and limitations
- Across data files, explicit quality control and validation are recorded as “No specific quality control was applied to this data.”
- Data resolution varies by recorder type (species-level for researchers/consultants on some groups; broad-group classifications for volunteers).
- The dataset emphasizes standardized protocols and comparability across a 1 km2 grid square framework, but practical movement of transects and site conditions may affect consistency (e.g., weather, grazing, terrain).

## How to use this data
- Compare sampling methods by availability of multi-method data across sites and rounds.
- Assess differences in data resolution by recorder type and identify data quality gaps.
- Analyze floral resource availability and pollinator activity in relation to habitat type (agri vs semi-natural) and season.
- Explore outputs such as dashboards or pivot-table-style summaries to enable self-service data exploration.
- Consider incorporating feedback questionnaire results to inform improvements to protocols and training for different recorder types.

## Notes and references
- The datasets reference Bumblebee Conservation Trust BeeWalk habitat codes (G3) for habitat classification.
- For floral resource assessment, standard floral unit classifications are used (Head, Spike, Major/Minor Umbel).
- No explicit quality control procedures were documented within the provided data descriptions.