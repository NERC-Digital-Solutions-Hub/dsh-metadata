# environmental biodiversity '

- Purpose and aims
  - Develop effective, cost-efficient agri-environmental policies that balance productive agriculture with biodiversity and ecosystem services.
  - Design spatially targeted schemes that reward farmers for collaborating with neighbors to maximize habitat gains and connectivity.
  - Quantify transaction costs and provide data-driven guidance for future public funding decisions and policy appraisal.

- Core approach
  - Combine literature synthesis on biodiversity values with empirical data collection to inform cost-benefit analysis and spatial targeting.
  - Use discrete choice experiments (DCEs) to elicit farmers’ willingness to participate and to identify cost drivers.
  - Apply species distribution modelling (SDM) to quantify ecological benefits, particularly for pollinators (Apis mellifera) in the UK.

## Data and methods

- Discrete Choice Experiments (DCEs)
  - Two DCEs conducted with 309 farmers in northern England (Cumbria, Northumberland, County Durham); 348 respondents in total completed the panels.
  - Scheme concepts:
    - Scheme 1: Habitat creation on retired land with annual payments; attributes include land area, location on land (field boundary, river edge, in-field), land quality, and type of habitat (planted trees vs natural regeneration).
    - Scheme 2: Adds a coordination bonus to connect habitats via ecological corridors between farms; includes corridor width (10 m vs 20 m), number of neighboring collaborators, and a coordination bonus.
  - Experimental design
    - Each respondent faced eight choice tasks per scheme, plus a status-quo option.
    - Priors and design choices based on hedonic theory and efficiency considerations (D-efficient design).
  - Data structure
    - Two CSV datasets (experiment1 and experiment2) with 26 columns each; panel format with 8 tasks per respondent; includes demographics and farm characteristics.

- DCE interpretation and key results (Willingness To Accept, WTA)
  - Scheme 1 (habitat creation only)
    - Location of features is more important than land quality.
    - Relative WTA effects (vs baseline in-field location):
      - River edge: -271 £/year (lower compensation needed)
      - Field boundary: -232 £/year
      - Planted trees vs natural regeneration: positive small effect (85 £/year)
      - Land quality: high-quality land adds +36 £/year (vs poor quality)
      - Feature size: 1 m² increases WTA by ~£1.80 per year (per m²)
    - Socioeconomic controls
      - AES participation reduces WTA by ~£247/year
      - Higher education substantially reduces WTA (e.g., A-levels -£361/year; postgraduate -£351/year)
      - Age increases WTA modestly (~£7.4/year per year)
      - Farm size: small positive effect per hectare; larger farms tend to require higher compensation
      - Primary income and other demographics also show notable effects
  - Scheme 2 (habitat connectivity with coordination)
    - Coordination with neighbors generally adds costs, but effects are nuanced:
      - Coordination with one neighbor: slight negative shift in WTA (~-£26/year)
      - Coordination with two neighbors: positive WTA shift (~+£54/year)
      - Corridor width: 20 m increases WTA by £157/year vs 10 m
      - Coordination bonus: negative WTA (-£0.23 per year per coordinating farmer)
      - AES participation remains associated with lower WTA (-£226/year)
      - Education and age show stronger effects (higher education lowers WTA; older age increases WTA modestly)
      - Sharing equipment with neighbors reduces WTA (about -£146/year)
      - Shared land boundaries have a small positive effect on WTA
- Species distribution modelling (SDM)
  - MaxEnt model using UK National Biodiversity Network (NBN) honeybee presence data (2019)
  - Predictors: monthly temperatures (min/max), precipitation, land use, distance to water, PM2.5, population density
  - Spatial resolution: 25 m; cross-validated AUC indicates predictive performance is informative
  - Key ecological findings
    - Land use is the strongest predictor of honeybee presence; arable land is less suitable than broadleaved woodland or acid grassland
    - Distance to freshwater and population density significantly influence presence
    - Winter minimum temperatures strongly affect hive survival; cold summers with high precipitation also reduce presence
  - Implications
    - Converting arable land toward woodland or grassland could substantially improve pollinator habitat suitability
    - Spatial targeting of schemes should prioritize areas currently less suitable for pollinators but with potential for gains through habitat restoration

## Results and interpretation

- Sample characteristics (descriptive)
  - 348 farmers; two-thirds male; average age ~53; average farm size ~232 ha (higher than regional average)
  - 72% report farming as primary income; 54% enrolled in an agri-environmental scheme
  - Geographic distribution: majority in Cumbria, North Yorkshire, Lancashire; postcode matching limitations noted
  - Flood risk perception: 28% not concerned; 6% very concerned

- Implications of DCE results
  - To maximize uptake, target payments should reflect opportunity costs, with higher payments required for larger or higher-yield land and for middle-field locations versus field edges or river edges
  - Targeted information and incentives can lower participation costs for those already in AES or with higher education
  - Coordination-based schemes have more complex cost dynamics; benefits of coordination increase with more participants but also raise required compensation, and corridor width matters for costs
  - Social factors matter: sharing equipment and existing neighbor collaboration reduce participation costs; general community engagement has less pronounced effects on willingness to coordinate

- Implications of SDM results
  - Policy should prioritize habitat types that enhance pollinator presence, notably broadleaved woodlands and grasslands over arable land
  - Landscape-scale connectivity via narrow corridors can be effective if costs are managed; narrower corridors preferred for cost efficiency without sacrificing connectivity
  - Spatially explicit modelling provides a basis for targeting where habitat restoration yields the greatest pollination benefits

## Conclusions and policy implications

- Economic viability and targeting
  - Preliminary financials suggest annual payments between £200 and £500 for creating 500–1000 m² features can incentivize farmers in northern England
  - A coordination bonus can improve habitat connectivity but must balance additional coordination costs; narrower corridors are generally preferable for cost efficiency

- Demographics and uptake
  - Younger, more educated farmers with prior exposure to government Environmental Land Management (ELM) schemes are more likely to participate
  - Farmers who share equipment with neighbors are more willing to participate in connectivity schemes

- Costs and biodiversity benefits
  - Land retirement to field-edge features incurs lower government transfer costs than interior field features
  - The pollination literature suggests potential UK welfare gains from pollinator conservation in the order of £189–£378 million in avoided yield losses

- Next steps
  - Extend models to improve precision (address sampling bias, taste heterogeneity)
  - Integrate updated spatially explicit cost-benefit analyses to demonstrate where habitat gains are most valuable
  - Develop policy tools to evaluate spatially targeted schemes using the combined DCE and SDM framework

- Data and references
  - Data sources include farmer surveys, UK AES participation records, and UK pollinator and land-use datasets (NBN, Land Cover Map 2019, HadUK-Grid)
  - Methodological foundations draw on established DCE and SDM literature, with explicit priors, efficient experimental design, and presence-only modelling approaches

- Overall takeaway for analysts
  - The study demonstrates a robust, data-driven pathway to design, cost-justify, and spatially target agri-environmental schemes that balance agricultural productivity with biodiversity benefits, especially pollinators
  - Combined DCE and SDM results provide actionable parameters (costs, corridor specifications, land-use targets) to inform policy design and funding decisions.