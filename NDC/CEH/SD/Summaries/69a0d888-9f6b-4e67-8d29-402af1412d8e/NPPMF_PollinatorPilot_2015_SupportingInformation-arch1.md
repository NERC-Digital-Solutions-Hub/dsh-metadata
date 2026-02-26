# NPPMF_PollinatorPilot_2015

## Overview
- Pollinator monitoring pilot conducted in 2015 across 14 UK sites, focusing on pollinating insects, floral resources, and environmental conditions.
- Four sampling rounds from April to August 2015; rounds sometimes extended due to poor weather.
- Half the sites were agriculture-dominated; half semi-natural habitats.
- Aimed to compare sampling methods, assess recorder group capacity, gather protocol feedback, and generate implementation cost information.

## Study Setting and Rounds
- 14 sites across the UK sampled in four rounds: Round 1 (27 Apr–10 May), Round 2 (1–14 Jun), Round 3 (6–19 Jul), Round 4 (17–30 Aug).
- Each site visit followed standardized 1 km2 OS grid square, with five pan trap stations and five 200 m transects per site.
- Habitat balance: equal representation of agricultural and semi-natural environments.
- Weather and environmental conditions were recorded for each site visit.

## Recorder Types and Protocols
- Researcher: paid staff with training in pollinator sampling and identification; data mainly at species level for bees and hoverflies.
- Consultant: professional taxonomic experts; includes role of unpaid amateur recorders; species-level data for bees and hoverflies.
- Volunteer: citizen scientists; data at broad taxonomic group level (no species-level IDs) except via researcher collaboration; trained with identification sheets.
- All recorder types used a standardized set of methods, with data collected across multiple protocols to assess complementarity and practicality.

## Sampling Methods and Protocols
- Pan trapping: five stations per site; used by researchers only; volunteers could participate alongside researchers to assess suitability.
- Fixed transects pollinator survey: five 200 m transects per site; all recorder types involved.
- Fixed transects flower survey: five 200 m transects; all recorder types involved.
- Timed focal flower observations (FFOs): two 10-minute focal observations per site; conducted by all recorder types.
- Standardised free search pollinator survey in good habitats: two fixed 1000 m2 areas for 30 minutes; used by consultants (sp) and some groups; researchers did not routinely perform this method alone; volunteers not typically responsible for free searches without supervision.
- Floral surveys of transects: 1–6 1 m2 quadrats per transect to assess floral abundance by researchers; additional scaled flower abundance estimates per transect by all researchers.

## Data Collected and Files
- SiteVisitConditions: date, recorder, environmental conditions, site type, round, protocol type, weather, wind, temperature, habitat codes, notes.
- FreeSearchConditions: environmental conditions for consultant-led free searches; includes habitat codes, expertise levels, timing, and effort data.
- FFOBConditions: timings, environmental conditions, and floral resources for focal floral observations (per site and quadrat).
- AllInsects: data on all insects recorded across transects, pan traps, FFOB, and free searches; includes site, round, protocol, recorder, method, section, group, genus, species, full name, date ID, and counts.
- FloralTransects: floral abundance data along transects; includes plant species, unit type, abundance scores, and median abundance.
- FloralQuadrats: flower abundance data around transects/pan traps; includes quadrat location, plant species, and floral unit counts.
- Protocol Feedback: questionnaire-style data on recorder views about each method; includes responses (strongly agree to strongly disagree) and comments.
- Note: Across the data files, no explicit quality control was applied to the data.

## Key Variables and Data Structure
- Site identifiers: OS grid references; site type (Agri vs SemiNat); round; protocol type; recorder ID.
- Environmental conditions: temperature, wind, cloud cover, sun exposure; habitat codes.
- Methods and effort: type of method, replication within 1 km2 square; transect start/end times; transect type (adjusted or determined); area sizes for searches; floral unit counts and plant species.
- Biological data: insect groupings (e.g., bumblebee, honeybee, solitary bee, hoverfly, beetle, butterfly, fly, moth, other/unknown); genus and species (where identified); full taxonomic name when available.
- Flower/resource data: plant species, floral unit type, counts, and density scores; transect-based floral abundance estimates.
- Attitudinal data: Likert-style responses on protocol questions with optional comments.

## Data Quality, Access, and Limitations
- No formal quality control applied to the datasets.
- Data collection constraints include weather-driven delays, scale limitations (1 km2 grid squares), and varied capability across recorder types (species-level data more complete for researchers/consultants; volunteers restricted to broad groups).
- Data integration challenges implicit in unifying methods across recorder types, scales, and taxonomic resolution.
- Some fields indicate methodological choices (sp = species-level for certain taxa; grp = broad groups), highlighting the need for careful harmonization in analyses.

## Potential Analyses and Uses for Analysts
- Compare method performance and complementarity: consistency of insect detections across pan traps, transects, FFOs, and free searches by recorder type.
- Assess data richness and taxonomic resolution by recorder group (species-level for researchers/consultants vs broad groups for volunteers).
- Explore correlations between environmental factors (habitat type, weather) and pollinator activity or floral abundance.
- Evaluate the practicality and scalability of standardized one-day protocols within 1 km2 grid squares for broader monitoring.
- Use protocol feedback to refine methods, workload, and training for future monitoring frameworks.
- Inform cost and support requirements for each method or combined protocol as part of implementation planning.

## Considerations for Practitioners
- When aggregating across methods and recorder types, standardize taxonomic resolution and account for potential biases in data collection effort.
- Incorporate environmental covariates (round, weather, habitat) to contextualize pollinator observations.
- Leverage the attitudinal data to identify methods that are more acceptable or feasible for citizen scientists and other non-experts.
- Recognize the absence of formal QC; implement downstream QC and validation steps when using these datasets for decision-making or policy support.