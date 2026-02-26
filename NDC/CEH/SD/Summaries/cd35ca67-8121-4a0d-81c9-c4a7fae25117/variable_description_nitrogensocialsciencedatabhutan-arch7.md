# Variable description

- Overview of the dataset focus
  - A longitudinal cross-season household/farm survey capturing crop production, input use, labor, irrigation, livestock, and household characteristics.
  - Variables are organized by season (e.g., season 1, season 2) and by crop, with codes such as CropcodeLABS11, CropcodeIRRGS11, etc., enabling cross-season and cross-crop analyses.
  - Includes data on labor hours by household members and hired labor, wages, mechanization, input costs, irrigation practices, pest management, and farmer attitudes/decision processes.

- Labor and labor costs
  - Detailed labor activity hours by season and by worker type (household members HM, hired labor HL) for activities such as Land Preparation, Seed/seedling sowing, Weeding, Planting, Fertilizing, Transplanting, Water management, Harvesting, and other activities.
  - Wages data by activity and season (e.g., LandPrepWAGES, SeedWAGES, etc.) and total wages per season.
  - Totals for labor hours per season and counts of laborers by gender are included (e.g., N610TotalS26, N621MaleS2, N622FemaleS2).

- Crop and input details by season
  - Crop codes by season (e.g., CropcodeLABS11, CropcodeIRRGS11) and crop-specific input/delivery details (seed sources, seed varieties, fertilizer types, irrigation sources, mechanization levels).
  - Mechanization indicators for land preparation, sowing, fertilizer application, irrigation, and harvesting (LandprepS11, SeedS11, FertilizerS11, IrrigS11, Harvesting1, etc.).
  - Season-specific measures of inputs such as animal power usage, machinery use, and associated costs (animal power indicators, total land preparation cost, etc.).

- Irrigation and water management
  - Access to irrigation and actual irrigation activities per season (AcessS11, DIrrigateS11, ProportionS11).
  - Rice-specific water management practices (WaterMgtS11) and puddling decisions (PuddleS11).
  - Sources and pricing of irrigation water (SourceS11, WPricingS11) and water payments (PayS11).

- Pest management and agrochemical use
  - Pesticide usage by crop/season, including whether pesticides were used, types of pesticides (farm-made vs manufactured), number of applications, and total cost.
  - Integrated Pest Management (IPM) adoption indicators and related questions.

- Livestock and livestock management
  - Livestock ownership by species and period, reasons for keeping animals, and how animals leave the farm (sales, slaughter, etc.) across multiple sub-entries (N92–N97 blocks for different rounds).

- Attitudes, information sources, and decision processes
  - Attendance at crop demonstrations/training, fertilizer/manure training, and whether farmers seek help when deciding on fertilizer use.
  - Information sources for fertilizer guidance (government, extension agents, private sector, leaflets, calculators, etc.) and whether farmers follow recommendations exactly or modify them.
  - Exposure to and adoption of decision-support tools (e.g., leaf color charts) and other practices (green manure, agroforestry, anaerobic digestion, drainage, foliar fertilizer, etc.).

- Subsidies, subsidies-related subsidies use
  - Direct subsidies received in the past 12 months for synthetic fertilizer, agricultural machinery, irrigation charges, output price support, seeds, and other subsidies.

- Household assets, expenditures, and living standards
  - Monthly and annual expenditures across food, fuel, electricity, transport, mobile/Internet, clothing, education, health, taxes, festivals, assets, durable assets, repairs, savings/investments, debt repayment, and other categories.
  - Household housing characteristics (ownership of home, number of rooms, floor material, lighting, fuel for cooking, drinking water source) and communication/technology access (TVs, smartphones, Internet).
  - Availability of transport, irrigation pumps, power tillers, and crop insurance.

- Geographic and data-structure notes relevant to GIS
  - The data are organized by crop and season with standardized prefixes (e.g., CropcodeLABS11, N64..., N68..., N74... across seasons 11, 12, 21, 22, 23, 24), enabling longitudinal spatial linking.
  - Explicit geocoordinates are not present in the extract; spatial analyses would rely on village/zone identifiers, plot proxies, slope/distance attributes, and other geographic proxies included elsewhere in the full package.
  - The instrument is large and highly detailed, with cross-season repetition, requiring careful data cleaning and harmonization to enable GIS-oriented analyses such as spatial patterns of input use, labor allocation, irrigation practices, and adoption of sustainable practices.

- Example GIS-focused applications suggested by the variables
  - Map spatial patterns of fertilizer and manure usage by crop, season, and location, linked to soil or land characteristics.
  - Analyze spatial variation in irrigation access, water sources, pricing, and water management practices across villages or plots.
  - Visualize adoption of IPM, pest management practices, and decision-support tools by location and season.
  - Combine crop-year data with plot-level attributes (where available) to explore spatial-temporal trends in cropping systems, input costs, and labor allocation.
  - Integrate household asset and subsidy data to assess socio-economic gradients in agricultural practices across geographic areas.