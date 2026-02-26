# Organic waste flow system and nutrients stocks and flows in Leicestershire and Leicester

- Objective and scope
  - Map how nutrients (nitrogen and phosphorus) are embedded in regional organic waste streams to identify intervention opportunities for improved resource use, economics, and environmental performance.
  - Region: Leicestershire County and Leicester City; focus on waste streams generated within the region for 2019 data (data collection occurred 2022–2023).
  - Waste streams mapped: green waste, food waste, slurry/manure, and wastewater (other streams were investigated but not included due to data limitations).

- Approach and outputs
  - Method: Material Flow Analysis (MFA) to quantify stocks and flows of organic waste and nutrient contents, plus mass balances of primary processing units (PUs).
  - Visualizations: Sankey diagrams to depict raw waste streams, processing/disposal outcomes, and nutrient (N, P) contents.
  - Modelling tool: PU mass balances informed by literature; results fed into Excel-based models and SankeyMATIC for diagrams.
  - Key outputs: Overall system diagram and subsystem diagrams (green waste, food waste, slurry/manure, wastewater) for Leicester City and Leicestershire County; nutrient distribution maps (Figure 1.5–1.10).

- Data sources and data handling
  - Waste data interrogator (EA, 2019): datasets on "waste received" and "waste removed," origin by Waste Planning Authority, waste types by European Waste Catalogue (EWC), and processing/disposal codes.
  - Green waste and food production waste: destination mappings (within/beyond county or city) using coded destinations (R and D codes) to infer composting, anaerobic digestion (AD), land spreading, landfill, etc.
  - Food consumption waste: household waste estimated from per-household generation (0.16 t/household/year) and household counts; destinations inferred from residual waste patterns (landfill, incineration, and AD for the city).
  - Slurry/manure: quantities and on-farm application destinations based on Defra/EIDC data.
  - Wastewater: central treatment by Severn Trent (~125 million tonnes/year as an average, accounting for dry/wet year variability) and septic tank sludge data; nutrient contents derived from Severn Trent and EA datasets.
  - Data gaps and assumptions: where EA codes lacked precision, destinations were inferred using facility types and coded tables; some transfer/distribution data could cause double-counting; limitations acknowledged.

- Processing units (PUs) and mass balance
  - Primary PUs modeled: anaerobic digestion of food waste and sewage sludge; composting of organic waste; incineration of food waste, sewage sludge, and green waste; wastewater treatment facility.
  - Mass balance figures are sourced from UK/Western European literature to reflect representative processes; gas emissions considered (CO2, CH4, N2O) where applicable; water content adjustments (e.g., incineration losses) explained.
  - Data sources for PU masses and emissions include Banks et al. (2011), Tezel et al. (2014), Andersen et al. (2010, 2011), IPCC guidance, Henze & Concha (2008), Environment Agency (2019), and other cited studies.

- Limitations and quality considerations
  - Data limitations: reliance on available datasets with gaps; imprecise EA destination codes; potential double-counting for transfer/storage flows; use of representative point values rather than ranges.
  - Scope limitations: only waste streams; exclusion of run-offs, import/export of chemicals/fertilizers, and some data types due to data availability; limited attention to losses and chemical transformations during transport/storage.
  - Uncertainty: results should be treated as indicative; future work should incorporate parameter ranges and a broader set of nutrient flows for a fuller regional picture.

- Findings at a glance (through 1.x and 2.x sections)
  - The MFA framework enables visualization of nutrient stocks and flows across green waste, food waste, slurry/manure, and wastewater streams, highlighting the main sinks and potential recovery paths.
  - The mass balance approach outlines how much nutrient can potentially be recovered via AD, composting, and wastewater treatment facilities, versus how much is lost or transformed in processing.
  - The resulting Sankey diagrams illustrate the scale of flows and nutrient distribution, aiding identification of intervention points to improve nutrient circularity.

- Practical implications for data leadership
  - Demonstrates the value of an integrated, system-wide data approach to understand nutrient flows and identify where data gaps constrain decision-making.
  - Highlights the importance of robust data governance around waste streams, including standardized coding, metadata, and documentation to ensure discoverability and repeatability.
  - Shows the need for cross-sector collaboration and stakeholder engagement to validate data, fill gaps, and co-design data-driven strategies for nutrient recovery.
  - Underlines that future improvements require broader data coverage (e.g., run-offs, fertilizer inputs) and the use of parameter ranges to capture real-world variability.

- Opportunities and next steps
  - Expand data coverage to include additional nutrient flows (e.g., run-offs, imports/exports of nutrients and chemicals) for a more complete regional nutrient circularity.
  - Develop ranges for key parameters to reflect process variability and enhance robustness of MFA results.
  - Improve data standardization and sector coordination to reduce uncertainties and enable more accurate forecasting and policy support.
  - Leverage the findings to inform local strategies for nutrient recovery investments, regulatory alignment, and community engagement in the circular economy.