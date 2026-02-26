# Experimental design/collection method: Life history data

- Purpose and scope
  - Provides life-history, reproductive, and wing morphology data for newly hatched larvae reared under controlled conditions.
  - Four laboratory populations from two Belgian landscape types (woodland: Lauzelle, St. Hubert; agricultural: Lillois, Hoegaarden).
  - Data enable exploration of effects of host-plant treatment (control vs drought-stressed) and landscape origin on development, reproduction, and wing traits.

- Experimental design
  - Larvae: randomly selected, three per plant, from each lab stock population.
  - Treatments: control host plant vs drought-stressed host plant.
  - Sample sizes: 178 larvae in control, 390 in drought-stress, with each population contributing evenly to both treatments.
  - Measures tracked from egg to adult: development time, survival, adult mass, sex, and subsequent reproduction and wing morphology.

- Datasets stored (CSV format)
  - Life_history_data.csv
  - Female_reproductive_output_data.csv
  - Wing_data.csv
  - Each file includes explicit headers and descriptions; empty cells indicate missing data (e.g., due to death).

- Spatial and site metadata
  - Population: site in Belgium where the population originated.
  - Landscape: woodland vs agricultural origin.
  - Use of Population and Landscape fields supports spatial mapping and landscape-level analyses.

- Data content highlights (per dataset)
  - Life_history_data.csv
    - Fields: Description, Population, Landscape, Treatment, ID, Adult_mass (mg), Total_development_time (days), Square_root_Total_devtime, sex (m/f)
  - Female_reproductive_output_data.csv
    - Fields: Population, Landscape, Treatment, ID, Adult_mass (mg), Mean_egg_size (mm^2), Longevity (days), Days until first egg, Fecundity (total eggs), Arcsine sqrt % Eggs hatched, %Eggs hatched
  - Wing_data.csv
    - Fields: Population, Landscape, Treatment, ID, Adult_mass (mg), Total_development_time (days), sex, Wing_loading (mg/mm^2), Mean_forewing_Melanin, Mean_FW_aspect_ratio, Total_Wing_area (mm^2)

- Data quality and handling
  - Missing data indicated by empty cells.
  - Data collected under controlled climate room conditions; results reflect experimental manipulations rather than field conditions.
  - Each individual has a unique ID, aiding traceability across datasets.

- Potential GIS applications
  - Map population origins and landscape contexts to visualize spatial patterns by population and treatment.
  - Link individual-level data to geospatial layers (e.g., habitat type, climate surfaces) via Population/ID.
  - Create map-based summaries: mean adult_mass, development time, fecundity, and wing traits by landscape and treatment.
  - Integrate with other spatial datasets to assess environmental influences on life-history and morphometrics.

- Practical notes for use
  - Ensure alignment of Population IDs across all three CSVs when merging datasets for GIS analyses.
  - Consider handling missing values appropriately (as indicated) during spatial analyses.
  - The headers include explicit descriptions to facilitate metadata generation and data lineage tracking.