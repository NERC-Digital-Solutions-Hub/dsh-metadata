# Background

- The NERC Soil Biodiversity Thematic Programme was established in 1999, centered on an intensive field experiment at the Sourhope site (Macaulay Land Use Research Institute / James Hutton Institute) in the Scottish Borders (Grid reference NT8545019630).
- Primary aims: simultaneously understand the biological diversity of the soil biota and the functional roles of soil organisms in key ecological processes. 
- Scope: 24 separate research projects investigating soil structure, soil processes (including carbon and nitrogen cycles), and the roles of micro-fauna and flora (Bacteria, Nematoda, Protozoa, Fungi), microarthropods (e.g., Collembola, Acari), invertebrate root feeders (Tipulid, Bidionid, Scarabeid larvae), meso-fauna (e.g., Enchytraeidae) and macro-fauna (e.g., Megalodila, Mollusca, Coleoptera).
- Related monitoring: the site was also used to monitor aboveground biomass production (productivity), species composition, and relative abundance (diversity) alongside soil biodiversity research.

- Field monitoring and data flow:
  - Regular meteorological data collection from February 1999 to September 2002 via an on-site Automatic Weather Station (AWS) on the experimental plots.
  - Data were regularly downloaded and transmitted to the Soil Biodiversity Data Manager at the Centre for Ecology & Hydrology.
  - The dataset comprises hourly summaries from 5-second samplings, stored in a CSV file named CHA_Sourhope_AWS_1999_2002.csv, with fields covering date/time, rainfall, wind speed/direction, air and soil temperatures at various depths, and soil moisture.

- Dataset structure and contents:
  - Columns include EXPERIMENT_ID, AWS_DATE, AWS_TIME, RAINFALL (mm), WIND_SPEED (m/s), WIND_DIRECTION (degrees), AIR_TEMP (°C), SOIL_TEMP_2CM, SOIL_TEMP_MINUS_2CM, SOIL_TEMP_MINUS_5CM, SOIL_TEMP_MINUS_10CM, SOIL_TEMP_MINUS_30CM (°C), SOIL_MOISTURE (m3/m3).
  - Data quality checks: numeric range checks, formatting conformity, and logical integrity checks implemented as part of quality control.

- Data governance and limitations:
  - NERC performed quality assurance but does not warrant the accuracy of the data or determine fitness for a user’s specific purpose.
  - NERC cannot be held liable for any loss, damage, injury, or other occurrence arising from the use of these data.
  - Data management practice included storing and uploading the datasets to appropriate portals for accessibility.

- Weather context notes (2002):
  - Compared with previous years, 2002 saw low rainfall in April and September, with wetter periods in February, July, and the last three months of the year.
  - Winter 2001/02 was exceptionally mild, with average air temperatures around 3.88 °C (Dec–Feb) versus approximately 2.28–2.86 °C in prior years.