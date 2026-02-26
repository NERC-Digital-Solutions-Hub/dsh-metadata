# Predicted recreation demand across the UK

- The study develops a spatially explicit map of predicted local recreation demand (a proxy for cultural ecosystem services) at 250 m resolution across the UK. It focuses on outdoor non-vehicular recreation such as walking, hiking, and cycling.  
- Predicted demand is derived from a bespoke application of the universal law of human mobility, producing a measure of projected visits to each grid cell.

## What it measures and why

- Measure: Predicted number of visits per target grid cell per time period (weekly, monthly, yearly), with variants that include or exclude an attractiveness component.  
- Purpose: To provide a scalable, policy-relevant indicator of cultural ecosystem services for scrutiny, monitoring, and informing future decisions in landscape and recreation planning.  
- Rationale: CES are important but underrepresented in monitoring due to difficulties in identification, quantification, and mapping; this framework yields spatially explicit, decision-relevant insights.

## Methodology

- Core equation (Predicted recreation demand for cell i):
  Demand_i = Attractiveness_i × sum over all source cells j of [ Population_j / (Frequency_ij × TravelDistance_ij)^α ], with α = 2.17.  
  - i = target cell; j = source cell; Frequency_ij = visits per year (scenarios: weekly, monthly, yearly).  
  - TravelDistance_ij = distance between i and j, adjusted for travel cost.  
- Frequency scenarios: three outputs for each dataset corresponding to visits per week (52/year), per month (12/year), and per year (1/year).  
- Attractiveness: derived from protected areas using IUCN categories; higher protection equals higher attractiveness. Values allocated so that II (highest protection) equals 1.0, III 0.8, IV 0.6, V 0.4, and no status 0.2.  
- Distance calculation: long-range cost-weighted distance at 2.5 km resolution along roads plus short-range Euclidean distance to the nearest road. Road speeds (UK, 2014) are converted to cost-weights via a table; remote cells with no roads weighted to reflect walking speeds.  
- Urban areas: target cells dominated by urban land cover are removed to focus on the wider landscape (urban sources still contribute).  
- Target and source grids: 250 m resolution; calculations executed by ArcGIS Pro and Matlab; 39,968 unique target-cell distance maps generated.  
- Data fusion: integration of population density (WorldPop, 2020), road network (OpenStreetMap), distance layers (cost-weighted and Euclidean), and protected-area information (UNEP-WCMC, IUCN-based attractiveness).  
- Outputs: six raster datasets for the UK at 250 m resolution, named to reflect frequency and attractiveness:
  - Weekly_250m_NonUrban_Attrac
  - Weekly_250m_NonUrban_NoAttrac
  - Monthly_250m_NonUrban_Attrac
  - Monthly_250m_NonUrban_NoAttrac
  - Yearly_250m_NonUrban_Attrac
  - Yearly_250m_NonUrban_NoAttrac

## Data inputs and preparation

- Population density: WorldPop unconstrained density (2020) at ~75 m resolution, resampled to 250 m and scaled by area.  
- Travel distance: combination of a 2.5 km-cost-weighted road network raster and a 250 m Euclidean distance to roads; roads derived from OpenStreetMap (Geofabrik).  
- Road speeds and cost-weights: UK speeds by road type (e.g., motorways fastest; secondary/tertiary much slower) used to generate per-cell cost weights; extreme remote cells assigned high weights to reflect travel difficulty.  
- Attractiveness proxy: Protected areas (UNEP-WCMC) classified by IUCN categories II–VI and other designations; attractiveness values assigned as described above.  
- Urban mask: 2020 UKCEH Land Cover Map used to exclude urban-dominated target cells.  
- Data sources: peer-reviewed or widely accepted datasets; provenance and processing details documented in the study.

## Computation and outputs

- Processing environment: Rasters (.tif) representing recreation demand across the full UK at 250 m scale; coordinate system: British National Grid (EPSG 27700).  
- File structure: outputs are consistently named, with explicit indicators of frequency and attractiveness inclusion.  
- Expression of results: provides estimated number of individual visits per 250 m grid cell for a given frequency, enabling spatial prioritization and monitoring of recreation demand patterns.

## Data availability, reproducibility and governance

- Reproducibility: code for the analysis is publicly available at github.com/dhooftman72/RecreationalValue.  
- Quality control: full internal team review plus external peer review for publication; inputs drawn from peer-reviewed or well-accepted sources.  
- Data governance and openness: outputs are shared as rasters; underlying data are described and sourced from publicly available datasets; dissemination is designed to support transparency, though data sharing barriers are acknowledged in related contexts (e.g., metadata gaps, access to some datasets).

## Implications for monitoring frameworks

- Demonstrates a concrete approach to operationalizing cultural ecosystem services into measurable, spatially explicit outputs suitable for monitoring and policy scrutiny.  
- Provides a framework that can be integrated into dashboards and reports to inform land-use planning, recreation management, and conservation prioritization.  
- Highlights the importance of data integration, metadata quality, and governance when establishing monitoring measures for CES.

## Limitations and considerations

- Assumptions: fixed visit frequencies (weekly, monthly, yearly) and the attractiveness proxy based on protected areas; may not capture all drivers of recreation behavior.  
- Data limitations: urban removal may exclude some relevant recreational demand in peri-urban areas; reliance on historical road speeds and infrastructure may affect current travel costs.  
- Methodological considerations: aggregation to 250 m may obscure fine-scale patterns; the model emphasizes accessibility and protection status as proxies for attractiveness, which may not reflect all social or cultural drivers of recreation.

## Funding and references

- Funding: Natural Environment Research Council (NERC) under AgZero+ (NE/W005050/1).  
- Key data sources and references: WorldPop, UNEP-WCMC Protected Areas, OpenStreetMap, Land Cover Map 2020, and the universal visitation law study (Schläpfer et al. 2021).  
- Code and supplementary materials: accessible via the cited GitHub repository; study underwent internal and external reviews prior to publication in Ecological Indicators.