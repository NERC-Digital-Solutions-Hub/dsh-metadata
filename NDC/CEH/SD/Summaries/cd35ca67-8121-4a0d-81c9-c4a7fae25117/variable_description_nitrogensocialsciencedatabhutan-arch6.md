# Variable description

- Purpose and scope
  - Documents time-use, labor, input decisions, and management practices for crops within a harmonised multi-country agricultural survey.
  - Supports analyses of labor allocation, irrigation, mechanization, fertilizer and pesticide use, and decision-making related to sustainable nitrogen practices.

- Data context and scope
  - Part of a cross-country harmonised household survey covering multiple South Asian countries (e.g., Nepal, Bangladesh, India, Maldives, Pakistan, Sri Lanka).
  - Observations at the crop/plot level within households over multiple seasons (season-specific data across seasons 1, 2, and beyond as indicated by variable suffixes).

- Variable structure and coding
  - delineated by activity and input categories, with season-specific indicators:
    - Labor and time use by household members (HM) and hired labor (HL) for season 1 and season 2, including:
      - Land preparation, seed/seedling sowing, weeding, planting, fertilizing, transplanting (rice), water management, harvesting, and others.
    - Wages and total wages by season for each labor activity.
    - Total labor hours per season and counts of workers (e.g., total males/females contributing in season 2).
  - Mechanization and inputs
    - Mechanization levels for land preparation, seed sowing, fertilizer application, irrigation, and harvesting.
    - Types of machinery used (with a predefined list) and total land preparation costs when using machinery or animal power.
    - Animal power usage and livestock-related variables (species owned, numbers, reasons for keeping, how animals leave the farm, etc.).
  - Crop and plot identifiers
    - Crop codes for crops grown in each season, with cross-season crop coding (e.g., season 1, season 2, season 3, season 4 where present).
    - Information on land plots, land ownership, tenancy, and plot-specific inputs and outputs.
  - Irrigation and water management
    - Source of irrigation water, water pricing mechanism, irrigation payments, access to irrigation, and methods specific to rice (e.g., flooding, drainage, alternating wetting and drying).
  - Pesticides and integrated pest management (IPM)
    - Pesticide use by crop/season, types (farm-made vs manufactured), frequency of application, and total costs.
    - IPM usage and related questions about decision making and training.
  - Fertilizer decisions and management
    - Decisions on synthetic fertilizers and manure use, including guidance sources, calculators/tools, and whether records are kept.
    - Repeated sections (N108x, N109x) capture decision processes for synthetic and organic fertilizers across multiple crops/seasons.
    - Attitudes and beliefs about fertilizer benefits, risks, and management practices.
  - Decision support tools and information sources
    - Exposure to and use of decision support tools (e.g., leaf colour chart) and other agronomic guides.
    - Sources of information and how strictly advice is followed.
  - Training, demonstrations, and adoption
    - Attendance at crop demonstrations or trainings and whether participants actively seek help when making fertilizer or manure decisions.
    - Perceived barriers to information and factors enabling adoption of improved practices.
  - Household economics and assets
    - Expenditures on food, utilities, transport, education, health, taxes, festivals, and other categories.
    - Household assets, housing characteristics, access to internet, smartphones, and ownership of productive assets (e.g., power tillers, irrigation pumps).
  - Subsidies and policy context
    - Direct subsidies for synthetic fertilizer, agricultural machinery, irrigation, output price support, seeds, and other subsidies over the past 12 months.
  - Other indicators
    - Enumerator notes and metadata (start/end dates and times of data collection), and additional prompts for data quality and context.

- Seasonal and cross-crop structure
  - Season-specific labor and input data for multiple crops per household, enabling cross-season comparisons and cross-country harmonisation.
  - Variables exist for season 1, season 2 (and later seasons in some sections), facilitating longitudinal-like cross-sectional analysis within the harmonised framework.

- Data quality and harmonisation considerations
  - High granularity with season- and crop-specific detail requires careful cleaning and documentation to maintain consistency across households, plots, crops, and countries.
  - Cross-country coding nuances (crop codes, mechanization classifications, input categories) must be aligned to ensure comparability.
  - Patchiness and variations in season coverage or mechanization reporting may affect completeness; appropriate imputation and metadata practices advised.

- End-use and outputs
  - Designed to support self-serve analysis via dashboards and pivot tables, focusing on labor allocation, input use, and management practices.
  - Enables analysis of nitrogen use efficiency (NUE) drivers, fertilizer subsidy impacts, adoption drivers, and the socio-economic determinants of farm inputs.
  - Supports policy analysis, targeted interventions, and farmer engagement through harmonised, comparable microdata.