# Questionnaire data on greenspace users' perceptions of experimentally manipulated urban meadows in Bedford and Luton

## Overview
- Data describe questionnaire responses from greenspace users assessing perceptions of urban meadows that varied in floral diversity and sward height.
- Experimental meadows located in Bedford and Luton across four sites; nine meadow types per site (3 diversity levels × 3 height levels); 30 respondents per site.
- Data were collected in 2014, ethically approved, and later re-analysed for Jones et al. (in press 2021) in People and Nature.
- The dataset is suitable for GIS-enabled exploration of spatial patterns in perceptions by meadow treatment and site, with potential integration of socio-economic variables.

## Data content and structure
- File: Data_Phase 2_AsUsed_ForPublicArchive.csv
- Size: 1020 data rows × 21 columns
- Core variables:
  - Spatial/locations: SITE (location code: CA Chiltern Ave, BK Brickhill Heights, GG Goldington Green, BR Bramingham Road), SampNo ( respondent data point), along with site coordinates referenced in the site descriptions.
  - Experimental factors: Diversity (low/medium/high), Height (short/medium/tall), Treatment description (9-level combination of diversity and height).
  - Perceptions: Q1_PerceivedDiversity (perceived plant diversity in plot), Q2_PrefScore (liking on a 1–10 scale).
  - Biodiversity awareness: plantid_EcoKnowledge (number of correctly identified plants from a list).
  - Related variables: eco-centricity indicators (totalWL_EcoCentrism), visit metrics (visitlength, visitfreq, othergsfreq, visitcount), and typical residency patterns (visit patterns to countryside and other urban greenspaces).
  - Demographics and socio-economics: gender, age, income, employ, edu, ukresident, ethnic, with NA indicating no response.
- Data coding: NA = no response; categorical options used where applicable.

## Experimental design
- 4 sites with 9 meadow types each (3 diversity × 3 height) across 4 locations.
- 30 greenspace users surveyed per site, totaling 1020 responses.

## Data collection and processing
- Data collected via questionnaire administered to greenspace users; informed consent obtained.
- Ethical approval through University of Sheffield's Research Ethics Committee (Landscape Architecture Ethics Panel).
- Data entry checks performed; responses outside predefined categorical options excluded.

## Data provenance and context
- Original datasets: Southon et al. (2017) and Southon et al. (2018) on aesthetic value and perceived species richness in urban meadows.
- Subsequent analysis: Jones et al. (2021, in press) examined modeling of cultural ecosystem services using this data.
- The current data resource supports reanalysis for exploring relationships between meadow characteristics, user demographics, and perceptions.

## Analytical context
- Prior analyses used multivariate methods and mixed-effects models in R to link meadow traits with user characteristics (Southon et al. 2017, 2018).
- Jones et al. (2021) employed mixed effects and Bayesian modeling to assess how user characteristics shape perception within a cultural services framework.

## GIS considerations and usage
- Spatially attributable data exist at the site level (four sites) with explicit site coordinates provided in the description.
- The dataset enables mapping perceptions and preferences by meadow treatment at a coarse spatial scale; individual respondent locations are not provided beyond site-level coding.
- Suitable GIS workflows: join the dataset to a spatial layer of the four sites, create choropleth or symbol maps by treatment type, and analyze spatial patterns of preferences alongside socio-economic variables.

## Quality control and ethics
- Respondents’ answers validated against allowed categories; inconsistent entries excluded.
- Ethical approval and informed consent documented; data anonymized for public release.

## Key references
- Southon, G.E., Jorgensen, A., Dunnett, N., Hoyle, H., Evans, K.L. (2017). Biodiverse perennial meadows have aesthetic value and increase residents' perceptions of site quality in urban greenspace. Landscape and Urban Planning, 158, 105-118.
- Southon, G.E., Jorgensen, A., Dunnett, N., Hoyle, H., Evans, K.L. (2018). Perceived species-richness in urban green spaces: Cues, accuracy and well-being impacts. Landscape and Urban Planning, 172, 1-10.
- Jones, L. et al. (in press 2021). Can we model cultural ecosystem services, and are we measuring the right things? People and Nature.