# Survey_Changwu

- A social survey dataset collected in 2019 from Chinese rural villages in Changwu County, Shaanxi Province (Loess Plateau) to understand farmers’ and village leaders’ knowledge learning dynamics and perspectives on farming practices, soils, and management.

## Experimental design and sampling
- Target population: local stakeholders including farmers (167 surveyed) and village leaders (11 surveyed).
- Location: Changwu County, Loess Plateau, with survey sites chosen where most scientific research and monitoring stations are located and where village leaders supported the survey.
- Approach: questionnaires with both closed and open-ended questions.
- Sampling basis: number of questionnaires per village varied according to population size.

## Collection methods
- Primary method: social science questionnaires (closed and open-ended items).
- Timing: conducted in 2019.
- Respondents:
  - Farmers: responses captured in For_Survey2nd_Changwu_Farmers.csv.
  - Village leaders: responses captured in For_Survey2nd_Changwu_Village_leaders.csv.

## Data files and structure
- Dataset folder: Survey_Changwu.zip.
- Files:
  - For_Survey2nd_Changwu_Farmers.csv (55 KB): survey results from 167 farmers.
  - For_Survey2nd_Changwu_Village_leaders.csv (8 KB): survey results from 11 village leaders.
- Geographic scope: Changwu County, Loess Plateau (no explicit coordinates provided in the description).
- Data columns: numerous questions labeled (e.g., Q1, Q2, ..., Q30 for farmers; Q1, Q2, ..., Q15 for village leaders) plus derived fields (e.g., Q6a, Q14a) and special sections (e.g., Q14a, Q24, Q25, etc.). Topics cover demographics, farming practices, education/training, information sources, soil knowledge (including red soil and erosion), perceptions of training and government support, barriers to participation, and environmental/production concerns.

## Farmers dataset overview (key themes)
- Demographics and background:
  - Village/town origin, gender, age, education level, and length of family farming.
- Learning and information sources:
  - Where farmers learn farming methods (family, friends, fellow farmers, farm cooperative, village committee, local government, university/college).
  - Details on how learning was obtained and perceived usefulness of knowledge from family, peers, government, seed/fertilizer shops.
  - Awareness of terms like "red soil" and knowledge about soils erosion.
- Knowledge application and attitudes:
  - Perceived helpfulness of different knowledge sources.
  - Interest in learning about red soil erosion/management and willingness to attend training or receive on-site visits, posters, written instructions, or farmer representatives.
- Training and support:
  - History of government training or financial support; types of support received.
  - Perceived sufficiency of local government training and financial support for environment protection/catchment management.
- Farming practices and challenges:
  - Barriers to participation in training (time away from farm, need for compensation, perceived usefulness of training, distance to training sites).
  - Primary concerns (food production rate) and biggest farming challenges (labour, water, land management, technology, fertilizers, regulations, etc.).
  - Expenditure focus and management of animal waste.
  - Environmental issues affecting farms (flooding, landslides, soil erosion, drought, etc.).

## Village leaders dataset overview (key themes)
- Representation and pressures:
  - Areas represented and perceived pressures on farmers (income, soil decline, water-related issues, etc.).
- Support and collaboration:
  - Opinions on the best ways to support farmers to change practices (financial support, training, other), and whether leaders provide advice on new farming practices (types of advice such as new techniques, soil and water conservation, fertilizer use, manure management, etc.).
- Knowledge sharing and partnerships:
  - Methods for sharing information with farmers (training, farm visits, posters/picture books, written instructions, farmer representatives, etc.).
  - Experience working with scientists to understand landscape, human impacts, water quality/quantity, pollution, soil erosion, floods, etc.
  - Interaction with higher-scale government officials and policy implementation for local areas.
- Governance and policy linkage:
  - Whether the organization acts as a key link between local and national policies and farmers.
  - Experience and monitoring of policy implementation; questions regarding regulation of farming activities and who regulates them.
- Policy implementation and outcomes:
  - Types of farm management and water management policies implemented, how they are implemented, and farmers’ interest in applying these policies.
  - Monitoring of policy success and documentation of results or comments.
  - Barriers or enablers to policy adoption from the leaders’ perspective.

## Data quality and considerations
- Quality control details are not specified (noted as N/A in the description).
- Some tables and column definitions are described with repetition and formatting artifacts; users should verify coding schemes and handle potential inconsistencies.
- Spatial data depth is limited to county-level localization; no explicit coordinates or GIS-derived geometry are provided in the text.

## GIS considerations and potential visualizations
- Potential map-based products:
  - Spatial distribution of farmer respondents by village/town within Changwu.
  - Cross-tabulations of knowledge sources, training interest, and perceived usefulness by village to identify spatial patterns in learning dynamics.
  - Overlay with environmental layers (soil types, soil erosion risk, red soil distribution, water resources) to examine correlations with knowledge, training demand, and management practices.
  - Visualization of training needs and barriers by village to prioritize GIS-enabled outreach campaigns.
  - Policy impact indicators by village (e.g., adoption of recommended practices, monitoring presence) derived from leader responses.
- Integration ideas:
  - Link survey data with other GIS layers (catchments, monitoring stations, land use) for spatial analysis of knowledge diffusion and practice adoption.
  - Use village-level aggregations to produce choropleth or heatmap visuals showing engagement, training uptake, or concern about environmental issues.

## Usage notes
- Data can be used to analyze knowledge dynamics, training demand, and governance support for farming practices within Changwu’s Loess Plateau.
- To maximize GIS utility, combine with external spatial data and perform village-level aggregations to support map-based decision-making and outreach strategies.