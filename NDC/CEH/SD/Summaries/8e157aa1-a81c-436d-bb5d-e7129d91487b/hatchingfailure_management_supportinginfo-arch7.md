# Supporting documentation for the dataset ' Avian hatching failure and management interventions in published studies of wild and captive populations '

## Overview
- Compiles hatching failure rates, threat status, and management interventions for 244 bird species across 233 published studies.
- Original aim: support a meta-analysis of mean hatching failure across threatened vs. non-threatened species under different management levels.
- Data are free to reuse with acknowledgement; preferred citation is Marshall AF et al. 2023, Biological Reviews.
- Methods and definitions adapted from Marshall et al. (2023), an open-access publication.

## Data sources and inclusion criteria
- Data collection drew from:
  - Web of Science Core Collection search (Feb 16, 2020) yielding 6,799 results.
  - Previous comparative analyses (e.g., Briskie & Mackintosh 2004; Spottiswoode & Møller 2004; others).
  - February 2020–September 2020 Google Dataset Search and Google Scholar alerts.
- Inclusion criteria:
  - Peer-reviewed articles or theses/dissertations online; exclude predatory sources.
  - Accessible via publisher or institutional libraries.
  - Focus on wild or captive birds (not domesticated poultry/gamebirds or intensively bred for the pet trade).
  - No in-ovo injections or eggshell manipulations unless appropriate controls exist.
  - Clear definition of hatching failure; sufficient information to calculate failure/success; minimum sample size of 10.
  - Data extractable from text, tables, figures, or supplementary material (WebPlotDigitizer used for figures).

## Data extraction and processing
- Each study record was assessed for qualitative and quantitative data on hatching failure, its influencers, and reporting format.
- When needed, WebPlotDigitizer extracted data from figures.
- Where exact data were unavailable, sources were traced to original datasets; otherwise recorded as NA.
- Multiple species/populations within a study treated as separate records.
- When means were not directly reported, calculations/estimates were derived from available data (noting potential biases, e.g., nests classified as abandoned or desertion).

## Geographic information
- Study site coordinates converted to decimal degrees (DD) via Google Maps when GPS data were provided.
- Central points used for ranges; where only location names were given, coordinates derived from the location.
- If no location data were available, latitude/longitude set to NA.
- For species with restricted distributions (e.g., Mauritius Fody), location approximations cross-checked with IUCN Red List and Birds of the World.

## Threat status and population type classifications
- Threat status:
  - Current IUCN Red List classification used when available; global status preferred over regional if both exist.
  - Subspecies statuses use regional/national lists when necessary; otherwise parent species status.
  - Only species recognized by BirdLife International and listed on IUCN Red List included.
- Population type (captive, wild, wild managed) classifications:
  - Captive: adults in captivity; eggs hatched/reared in captivity; includes interventions like artificial insemination, incubation, or fostering.
  - Wild: adults in the wild with no management interventions beyond monitoring.
  - Wild managed: wild populations with management interventions (e.g., predator control, nestboxes, supplementary feeding, egg manipulations).
- Some records could not be verified from original sources and are marked NA; where older comparative analyses were used, classifications are inferred or NA if uncertain.
- Inference rules:
  - When studies mention partial interventions but data can’t be separated, whole-population intervention assumed.
  - Specific details often missing; some records excluded or NA due to insufficient information.

## Management interventions
- Interventions often not fully reported; assumptions made where necessary:
  - Captive populations assumed to be supplementary fed unless stated otherwise; no artificial nests unless stated.
  - Non-captive populations assumed to have no management unless mentioned.
  - If any part of the population experienced an intervention and results can’t be separated, the intervention is attributed to the whole population.

## Hatching failure proportion extraction and calculation
- Primary metric: proportion of hatching failure across the population (eggs at incubation end that did not hatch, excluding predation/desertion/accidents/unknown factors).
- Sample size handling:
  - Direct sample size available for 59.2% of records (n ≈ 483 records total).
  - If not available, estimated (e.g., from number of successful nests times mean clutch size).
  - Additional sources used for mean clutch size when not reported (e.g., Cooney et al. 2020; New Zealand Birds Online; Birds of the World).
- Potential biases noted in estimation (e.g., misclassification of abandoned eggs; nests reported only for successful nests).

## Terminology and data standardization
- Captured varied terminology across studies (hatching success/failure, hatchability, etc.).
- All non-standard terms homogenized to standard definitions; hatching failure definitions inverted to align with hatching success for comparability.
- Resulted in 51 distinct definitions of hatching success and 12 definitions of hatchability in the final dataset.

## Data structure and variables (high-level)
- The dataset comprises a wide range of fields, including:
  - Publication year, study name, title, journal, and notes.
  - Geographic coordinates (latitude/longitude) and location details.
  - Population classification (wild, wild managed, captive) and incubation type (natural/artificial).
  - Nestboxes/burrows sites and supplementary feeding indicators.
  - Clutch size data (from multiple sources) and various calculations for total eggs and hatchings.
  - Hatching failure/success proportions, standard errors/deviations, and definitions used.
  - Taxonomic and threat-status fields (IUCN status, regional status, subspecies handling).
  - Data provenance flags (Web of Science, Google Scholar, etc.).
  - Calculations and estimations explanations for derived values.

## Quality control
- Data extraction performed by a single researcher (A.F.M.), with about 10% of records checked by a second researcher (P.B.) for consistency and potential outliers.

## Usage and attribution
- Dataset designed for map-based analyses of hatching failure in relation to geography, threat status, and management interventions.
- Users should cite the Marshall et al. (2023) Biol. Rev. paper alongside this data resource.

## References
- Core references span foundational hatching studies, systematic reviews, and supportive data sources (e.g., Briskie & Mackintosh 2004; Møller et al. 2010; Reding 2015; Cooney et al. 2020; and Marshall et al. 2023).