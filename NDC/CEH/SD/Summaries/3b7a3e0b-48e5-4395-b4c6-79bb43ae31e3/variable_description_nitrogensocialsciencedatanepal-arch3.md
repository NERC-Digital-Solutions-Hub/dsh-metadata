# Variable description

- The dataset comprises extensive variable-level descriptions for a multi-season agricultural survey, capturing labor inputs, wages, mechanization, irrigation, input use, pest management, livestock, and household economics across crops and seasons.
- It is designed to support monitoring frameworks by documenting how farmers allocate labor, procure and use inputs, and manage resources, enabling policy evaluation and informed decision-making.

## Key variable groups and their focus

- Labor and wages
  - Season-specific labor inputs and hours spent by household members (HM) and hired labor (HL) across activities such as land preparation, seed/sowing, weeding, planting, fertilizing, transplanting, water management, harvesting, and other tasks.
  - Season-specific wage data for each labor activity (e.g., Land Preparation, Seed/Seedling, Weeding, Planting, Fertilizing, Transplanting, Water management, Harvesting, Others) and total wages per season.
  - Counts of labor supply by gender (e.g., MaleS1, FemaleS1) and season-wise totals.
- Mechanization and inputs
  - Mechanization levels for land preparation, seeding, fertilization, irrigation, and harvesting across seasons (e.g., fully mechanized, partially mechanized, fully manual).
  - Costs associated with land preparation when machinery or animal power is used.
  - Crop codes linked to labor and input activities (CropcodeLABS11, LABS12, LABS21, etc.) to tie activities to specific crops and seasons.
- Irrigation and water management
  - Variables on access to irrigation, water source, pricing mechanisms, and payments for irrigation across seasons.
  - Proportions and methods of water management for rice (e.g., flooded, alternate drainage, aeration) and sector-specific water-related decisions.
- Fertilizers and manure
  - Decisions and records related to synthetic vs. organic fertilizers, manure use, and associated keep-record practices for each target crop and season.
  - Use of decision-support tools, guidance documents, and information sources (government, extension, traders, media, internet) influencing fertilizer use.
  - Attitudes and beliefs about fertilizer effectiveness, risks, and environmental/health implications.
  - Training, demonstrations, and adoption of fertilizer-related practices (e.g., IPM, foliar application, green manures, anaerobic digestion) with whether they were heard, used, or dis-adopted.
- Pesticides and IPM
  - Types of pesticides and herbicides used, frequency of applications, total pesticide costs, and integration of IPM techniques across seasons.
  - Crop-specific pesticide codes and whether information sources or demonstrations influenced usage.
- Crop and crop management
  - Crop codes for season-specific crops, with detailed activity indicators (land prep, sowing, irrigation, fertilization) tied to crops.
  - Source and level of mechanization for each crop management stage and season, plus crop-specific costs.
- Livestock and small ruminants
  - Detailed livestock data including species, ownership, numbers of mature animals, reasons for raising animals, and movements off the farm (sale, slaughter, etc.) across multiple rounds.
  - Patterns of time allocation and space use for livestock (yard/open/closed housing) and associated enumerator notes.
- Household economics and assets
  - Expenditures categories (food, clothing, education, health, tax, festivals, durable assets, savings/investments, debt repayment, etc.) and annual vs monthly figures.
  - Household ownership of assets (house, rooms, flooring, lighting, fuel sources, water sources, electronics, transport) and related indicators (access to internet, irrigation pumps, power tillers).
- Subsidies and direct support
  - Direct subsidy indicators across inputs and outputs (synthetic fertilizer, agricultural machinery, irrigation, price support, seed, other subsidies) by season.
- Information, training, and decision-making
  - Attitudes toward risk, openness to new technologies, perceived soil fertility effects of inputs, and decision-making processes for fertilizer and manure use.
  - Exposure to crop demonstrations, fertilizer/manure training, and sources of fertilizer information; behaviors around following advice and keeping records.
- Enumerators’ notes and metadata
  - Enumerators’ notes (e.g., Enumerator’s note P17, P18, P21, P24, P25, P26, P28, P291, P301) indicating contextual details, data collection issues, and qualitative observations.
  - Metadata elements for data collection timing (start/end dates and times) to support auditability and traceability.

## Design and longitudinal aspects

- Seasonality and time framing
  - Variables span multiple seasons (e.g., season 1, season 2, season 3, season 4) with season-specific measures for labor, wages, mechanization, irrigation, and input use.
  - Crop codes and activity codes align with season-specific crop management to enable cross-season analysis.
- Cross-activity and cross-crop linkage
  - CropCodeLABS, CropCodepestS, CropcodeIRRGS links connect labor, input usage, pest management, and irrigation data to specific crops and seasons.
  - Detailed activity-by-activity labor hours by HM and HL facilitate decomposition of labor intensity and cost structure.
- Data quality and governance indicators
  - Extensive enumerator notes and checks indicated by enumerator-specific fields; presence of start/end timestamps and date/time fields enhances traceability and data governance.
  - The breadth and depth of variables imply a need for careful harmonization and rigorous data management to maintain cross-season and cross-country comparability.

## Practical considerations for monitoring framework authors

- Rich, multi-season, multi-topic dataset enables robust monitoring of:
  - Labor intensity and labor use efficiency across farming activities.
  - Adoption and diffusion of mechanization and input technologies.
  - Irrigation management practices, water use, and associated costs.
  - Fertilizer and pesticide usage patterns, including IPM adoption and decision-making influences.
  - Production inputs subsidies and their sectoral impact.
  - Household resilience indicators through livestock management and asset ownership.
- Data governance implications:
  - The need to maintain comprehensive metadata, keep consistent crop/activity coding, and manage data quality across seasons and regions.
  - Address potential data gaps or inconsistencies due to seasonality, recall bias, or cross-country differences.
- Policy evaluation and monitoring design:
  - The dataset supports baseline-to-intervention-to-impact analyses, given its longitudinal design and detailed input–output–labor linkages.
  - Harmonized coding and rich metadata support reproducibility, auditability, and cross-country benchmarking of agricultural practices and environmental health outcomes.