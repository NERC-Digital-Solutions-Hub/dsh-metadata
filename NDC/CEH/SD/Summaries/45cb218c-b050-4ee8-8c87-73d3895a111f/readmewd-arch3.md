# Gridded data of water debt for year 2000

- Purpose and scope
  - Defines water debt (WD) as the number of years required by the hydrological cycle to replenish water resources used for annual production of nine major crops.
  - Applies globally to crops: wheat, maize, rice, soybean, sugar cane, sugar beet, cotton, barley, sorghum.
  - Delivered as gridded data at 5 arcminute resolution for approximate year 2000, with global coverage.

- Key concepts and calculations
  - WD for a grid cell and year 2000: WD = total annual water footprint (WF) for all nine crops divided by the cell’s average renewable water volume per year.
  - Water footprint (WF) for each crop and source: WF_cr_l = CWF_s_cr_l × P_cr_l
    - CWF_s_cr_l: crop water footprint per ton from source s (groundwater, surface water, or soil moisture).
    - P_cr_l: annual production of crop cr in location l (tons).
  - Crop WD across all sources: WD_cr_l equals the maximum WD across sources s, reflecting simultaneous replenishment by precipitation.
  - Total WD for the cell: sum of WD_cr_l across all nine crops.
  - Long-term annual renewability used to define the denominator: average renewability rate computed over 1987–2013 to smooth extreme years.

- Data design and references
  - The full methodology is provided in open access: doi.org/10.1029/2018WR023146.
  - Temporal context: data focus around year 2000 with a broader temporal framing 1997–2003 for the dataset period.
  - Units: years ( WD is expressed as years).

- Metadata and format
  - Spatial scope: global; spatial resolution: 5 arcminutes.
  - Coordinate system: WGS 84.
  - Temporal scope and resolution: annual; approximate reference year 2000.
  - File format: text (.txt) files, ASCII-compatible for easy import into GIS and analysis software.
  - Accessibility: can be imported into MATLAB, Python, or R; can be loaded into GIS by changing the file extension to ".ascii".

- File naming and structure
  - Each file corresponds to the WD for all nine crops for one water source or a combined set:
    - 'GW' (groundwater), 'SW' (surface water), 'SOILMOISTURE' (soil moisture), and 'allsources' (combined across all three sources).

- Practical use for monitoring and decision-making
  - Provides a spatially explicit measure of long-term water scarcity risk tied to agricultural production.
  - Enables comparison across regions and crop types to identify priority areas for water governance, data validation, or targeted interventions.
  - Supports development of dashboards, maps, and reports for environmental health monitoring and policy evaluation.
  - Can inform data governance and transparency efforts by illustrating data structure, sources, and metadata requirements.