# Survey_Changwu

- 2019 social science survey conducted in Changwu County, Shaanxi Province, Loess Plateau, China
- Purpose: understand knowledge, learning dynamics, and preferences of local farmers and village leaders to inform farming practices and policy support
- Stakeholders surveyed: Farmers (167 respondents) and Village Leaders (11 respondents)

## Data Collection and Methods

- Experimental design: social surveys in rural Chinese villages to local stakeholders to capture knowledge and learning dynamics
- Collection method: questionnaires with closed and open-ended questions; sampling size per village based on population
- Coverage: surveys in Changwu County and surrounding towns where research and monitoring stations are located; village leaders supportive of the survey
- Fieldwork and instrumentation: Calibration and analytical methods not applicable or not provided
- Data nature: social science survey data; stored as CSV files with encoded responses
- Quality control: not specified in the documentation

## Data Files and Structure

- Two CSV data files in the Survey_Changwu dataset:
  - For_Survey2nd_Changwu_Farmers.csv (55 KB): survey results from farmers in Changwu County
  - For_Survey2nd_Changwu_Village_leaders.csv (8 KB): survey results from village leaders in Changwu County
- Dataset metadata
  - Year: 2019
  - County: Changewu (Changwu)
  - Landscape: Loess Plateau
  - Stakeholders: Farmers (167), Village Leaders (11)
  - File naming reflects respondent group and location
- Content structure
  - Both files include a set of Q-numbers (e.g., Q1–Q30) with corresponding questions and response options
  - Farmers file focuses on demographics, learning sources, knowledge about soil, training needs, government and market influences, farm practices and environmental issues
  - Village Leaders file focuses on leadership representation, advisory roles to farmers, collaboration with scientists and higher-level government, policy implementation, monitoring, and perceptions of regulation
- Example question coverage
  - Demographics: village/town origin, gender, age, education level
  - Learning sources: where farmers learn farming methods (family, friends, fellow farmers, cooperatives, village government, university, etc.)
  - Knowledge and attitudes: learning about red soil, soil erosion, soil management and conservation
  - Training and support: desire for training, government support, barriers to participation
  - Farm challenges and economics: biggest farming challenges, most expensive inputs, waste management, environmental issues
  - Policy and governance: perceived usefulness of policies, monitoring of policy outcomes, regulation of farming activities
  - Village leaders' governance questions: best ways to support change, collaboration with scientists and higher-level governments, policy implementation and monitoring

## Variables and Question Mapping (Key Points)

- Farmers dataset (sample questions)
  - Q1: home village/town; Q2: gender; Q3: age; Q4: highest education; Q5: how long farming family has cultivated land
  - Q6–Q7: primary learning sources and details on learning methods
  - Q8–Q11: perceived usefulness of knowledge from family, friends, government, seed shops
  - Q12–Q13: awareness of "red soil" and knowledge of soil erosion
  - Q14: sources of relevant soil erosion knowledge
  - Q15–Q30: farming practices, impacts on nearby land, desired productivity improvements, training and government support, environmental issues, barriers to participation, concerns about food production, challenges and costs, waste management, and environmental risks
- Village Leaders dataset (sample questions)
  - Q1: village/town represented
  - Q2: greatest pressures on farmers (income, soil, water, etc.)
  - Q3–Q4: preferred support methods and advisory practices
  - Q5: methods to share training/advice
  - Q6–Q7: collaboration with scientists and higher-level government; potential usefulness of such collaboration
  - Q8–Q12: role as a link between policies and farmers; policy implementation and monitoring; list of implemented management and water policies; methods of implementation
  - Q13–Q15: farmer interest and monitoring of policy success; regulation of farming activities and related details
- Data curation notes
  - Response definitions are embedded per question; some items show duplicated wording or formatting variations
  - Open-ended fields capture additional details (e.g., Q14a, Q24a, Q25a)

## Data Quality and Limitations

- Quality control and calibration details are not provided (N/A)
- Potential data quality considerations for Data Support use
  - Encoding: categorical codes need decoding to human-readable labels
  - Consistency: cross-file alignment by village/town required to enable comparisons between farmers and leaders
  - Open-ended responses require text normalization and coding
  - Language provenance: original survey content is Chinese; some metadata is in English, so careful translation/interpretation may be needed
  - Missing values: not explicitly described; handle with standard imputation or exclusion as appropriate

## Potential Data Products and Uses (Data Support Perspective)

- Descriptive dashboards and pivot analyses
  - Demographic profiles of farmers (gender, age, education)
  - Primary learning sources and preferred training formats
  - Perceived usefulness of knowledge from different sources
  - Knowledge about red soil and soil erosion; levels of awareness
  - Training interest, barriers to participation, and desired support (financial, training, policy)
  - Environmental concerns and most expensive farming inputs
- Comparative analyses
  - Farmers vs. village leaders: perspectives on policy effectiveness, preferred support, and monitoring practices
  - Village-level comparisons to identify targeted intervention needs
- Policy and practice insights
  - Correlations between training/training access and willingness to adopt new practices
  - Relationship between perceived government support and farmer engagement in environmental programs
  - Identification of regulatory areas with high farmer concern or low compliance
- Data linking and integration
  - Use Q1 (village) as a key to join farmers and leaders by location for integrated community analyses
  - Derive derived variables (e.g., training interest yes/no, regulatory exposure) for streamlined reporting

## Access and File Details

- Data accessibility
  - Two primary CSV files:
    - For_Survey2nd_Changwu_Farmers.csv
    - For_Survey2nd_Changwu_Village_leaders.csv
- Data preparation recommendations for Data Support
  - Create a data dictionary mapping Q numbers to questions and codes to labels
  - Normalize and harmonize variable names across both files
  - Decode categorical responses into human-readable categories
  - Build derived variables for key analyses (e.g., training interest, perceived usefulness)
  - Validate village/town identifiers to enable cross-group comparisons
- Suggested deliverables for end users
  - Interactive dashboards showing demographic patterns, learning sources, and training needs
  - Reports comparing farmer and leader perspectives on policy support and environmental management
  - Visuals mapping responses by village to identify regional variation