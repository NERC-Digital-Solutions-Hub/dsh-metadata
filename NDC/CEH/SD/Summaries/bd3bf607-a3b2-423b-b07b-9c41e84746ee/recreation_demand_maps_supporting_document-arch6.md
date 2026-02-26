# Predicted recreation demand across the UK

- Purpose and scope
  - Maps predicted recreation demand (local recreation such as walking, hiking, cycling) across the UK at 250 m resolution.
  - Recreation demand is estimated as the number of projected visits to local recreation target cells using the universal law of human mobility.
  - Urban target cells are removed; outputs focus on the wider landscape.

- Core concept and equation
  - Demand for target cell i: Demand_i = Attractiveness_i × sum over all source cells j of (Population_j) / (Frequency_ij × TravelDistance_ij)^α, with α = 2.17.
  - Frequency represents visits per year (three scenarios: once per year, once per month, once per week).
  - Distance decay accounts for population, travel distance, and target cell attractiveness to estimate visits to i from all sources.
  - Rounding: low-density visit densities (<1 per km^2) are rounded to 0.

- Data inputs and parameterization
  - Population density: WorldPop 2020 (0.0008333° resolution; resampled to 250 m grid; UK).
  - Visit frequency scenarios: 1/year, 12/year (monthly), 52/year (weekly).
  - Travel distance: combination of long-range cost-weighted distance (2.5 km grid) derived from UK road network and short-range Euclidean distance to nearest road (250 m).
  - Road network and cost-weights: OpenStreetMap data; cost-weights derived from average UK road speeds (2014) per road type; overseas links included; some cells assigned high cost to reflect remote travel; explicit weighting table provided.
  - Attractiveness proxies: UK protected areas (UNEP-WCMC IUCN categories). IUCN II best (weight 1); No status 0.2; III 0.8; IV 0.6; V 0.4. This models higher attractiveness for better-protected areas.

- Outputs and data products
  - Six main raster datasets per frequency: Weekly, Monthly, Yearly × with attractiveness included (Attrac) and excluded (NoAttrac).
  - File naming examples: Weekly_250m_NonUrban_Attrac.tif, Weekly_250m_NonUrban_NoAttrac.tif, Monthly_..., Yearly_...
  - Rasters are 250 m × 250 m, British National Grid (EPSG 27700), 2854 × 5200 grid cells, units: estimated number of visits per 250 m cell.
  - Outputs reflect non-urban target cells, but source cells can be urban.

- Data structure, format and metadata
  - Format: raster TIFF (.tif) with explicit descriptions in filenames.
  - Coverage: full UK map at 250 m resolution; non-urban targets; units are number of visits per target cell for the specified frequency.

- Quality control and reproducibility
  - Internal team review by four authors; external peer review for Ecological Indicators.
  - Input data drawn from peer-reviewed or widely accepted sources.
  - Code available at GitHub: dhooftman72/RecreationalValue.

- Funding and references
  - Funded by NERC under AgZero+; references include Schläpfer et al. (2021) for the universal visitation law, WorldPop, UK Land Cover 2020, UNEP-WCMC protected areas, and OpenStreetMap data sources.

- Practical implications for data use
  - Provides a ready-to-use data product to explore and map cultural ecosystem service demand.
  - Can be combined with other spatial data to support planning, policy, and public communication about recreation and CES.
  - Encourages transparency and potential for feedback and iterative product development; datasets can inform better data creation and sharing practices.