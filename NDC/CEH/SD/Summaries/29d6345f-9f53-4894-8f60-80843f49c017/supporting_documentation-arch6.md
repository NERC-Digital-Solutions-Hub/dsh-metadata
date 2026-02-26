# Data resource: Questionnaire survey data on perceptions of experimentally manipulated urban meadows in Bedford and Luton

## Overview
- Dataset describing questionnaire responses from greenspace users regarding perceptions of experimentally manipulated urban meadows that vary in floral diversity and sward height.
- Location: four sites in Bedford and Luton; data collected by the authors with informed consent.
- Part of the Fragments, functions and flows NERC BESS project (2014); subsequently re-analysed in 2021 for a paper in People and Nature.
- Data resource used in later analyses (e.g., Jones et al., 2021) to model cultural ecosystem services.

## Experimental design
- Nine meadow types per site (3 diversity levels × 3 height levels) across four sites.
- 30 respondents surveyed at each location.
- Sites and coordinates:
  - Bedford: Chiltern Ave. (CA), Goldington Green (GG), Brickhill Heights (BH)
  - Luton: Bramingham Road (BR)
- Experimental meadows located at specified coordinates within Bedford and Luton.

## Data collection and content
- Method: structured questionnaire administered to greenspace users.
- Recorded outcomes include:
  - Perceived diversity in each plot (Q1_PerceivedDiversity)
  - Overall impression/preference scores on a 10-point scale (Q2_PrefScore)
  - Socio-economic and personal attributes (e.g., gender, age, income, employment, education, UK resident status, ethnicity)
  - Eco-knowledge proxy (plantid_EcoKnowledge) and landscape/wildlife related measures
  - Visit behavior metrics (visitlength, visitfreq, visitcount, othergsfreq, etc.)
  - Treatment descriptors describing meadow type by diversity and height
- Data are primarily categorical and ordinal with some numeric measures.

## Data structure and units
- Data resource: Data_Phase 2_AsUsed_ForPublicArchive.csv
- Size: 1020 data rows, 21 columns
- Key columns (examples):
  - SITE: location code for meadow group (CA, BK, GG, BR)
  - Sample / SampNo: respondent identifiers
  - Diversity: meadow diversity level (low, medium, high)
  - Height: meadow sward height level (short, medium, tall)
  - Treatment description: nine-level category combining diversity and height
  - Q1_PerceivedDiversity (numeric perception of diversity)
  - Q2_PrefScore (10-point preference score)
  - plantid_EcoKnowledge: number of correctly identified plants from a list
  - Various socio-demographic and visit-related variables (visitlength, visitfreq, visitcount, gender, age, income, employ, edu, ukresident, ethnic)
- Data use notes: NA indicates no response; some entries are coded to reflect age/income brackets midpoints.

## Analytical context
- The dataset as provided has not undergone analysis within this resource.
- Prior analyses (Southon et al. 2017, 2018) used multivariate analysis and mixed-effects models in R to relate meadow characteristics to user responses.
- Jones et al. (in press 2021) applied mixed-effects and Bayesian modeling to evaluate how user characteristics shape perceptions within a cultural services framework.

## Quality control and ethics
- Ethically approved by the University of Sheffield Research Ethics Committee (Landscape Architecture Ethics Panel).
- Data entry quality checks performed; responses that did not match categorical options were excluded.

## Provenance and related literature
- Original related works:
  - Southon, Jorgensen, Dunnett, Hoyle, Evans (2017). Biodiverse perennial meadows have aesthetic value and increase residents' perceptions of site quality in urban greenspace. Landscape and Urban Planning.
  - Southon, Jorgensen, Dunnett, Hoyle, Evans (2018). Perceived species-richness in urban green spaces: Cues, accuracy and well-being impacts. Landscape and Urban Planning.
  - Jones et al. (2021, in press). Can we model cultural ecosystem services, and are we measuring the right things? People and Nature.

## Usage notes
- Suitable for analyses relating meadow design (diversity and height) to user perceptions and socio-demographic factors.
- Can be used to explore self-serve data tools, visualization dashboards, or reports illustrating links between experimental treatments and public perception.
- Appropriate for validating models of cultural ecosystem services and informing data-sharing practices for similar urban greenspace studies.