# Experimental Design/Sampling Regime

- Objective and design
  - Analytical study to assess how irrigation affects the abundance of mosquito species, particularly those involved in Rift Valley fever transmission.
  - Sampling sites identified inside and outside the irrigation scheme to enable comparison.
  - Seasonal variation considered: stronger irrigation effect expected during the dry season when water availability is limited to irrigated farms.
  - Repeated sampling across wet and dry seasons and active vs. inactive irrigation periods.
  - Each sampling visit involved three consecutive days at a given site to reduce variability.

- Field collection methods
  - Adult mosquitoes collected with CO2-baited CDC light traps, deployed 4:00 pm–6:00 pm for 3 consecutive days.
  - Ten traps per night at homesteads and irrigated farms within ten villages; control site included Murukani village and pastoral areas in Ijara, Garissa.
  - Mosquitoes collected each morning, then transported to field laboratory for sorting; immobilized with 99.5% triethylamine and preserved in liquid nitrogen for later lab processing.
  - Traps placed in livestock night sheds, bushes, houses, farms, and forested areas.
  - Sample handling evolved from direct transfer from collection bags to field lab (CBG) to later use of centrifuge tubes (CNT) to facilitate field-to-lab transport; later, samples were often moved to Eppendorf tubes (EPF) after sorting.
  - Identified mosquitoes stored at -70°C for future analysis; all trapping/larval sites georeferenced for mapping.

- Dataset and data structure
  - Single CSV file: DDDAC_Kenya_entomology.csv containing 9 variables.
  - Variables include: date (sampling date), latitude and longitude (decimal degrees), cbg (collection bag/trap ID), cnt (centrifuge tube with mosquitoes; empty if no sample), epf (identified mosquito pool), species (species in the pool), sex (sex of mosquitoes in the pool), Pool_size (number of mosquitoes per pool).
  - Data quality notes: some missing latitude/longitude due to equipment failure; missing data indicated as na; initial surveys had direct field-to-lab transfers, later standardized with CNTs.

- Quality control and validation
  - Mosquito identification performed by expert taxonomists and cross-validated by internationally certified taxonomists prior to pooling and preservation.
  - Identification and pooling practices aimed at ensuring accurate species-level data for downstream analyses.

- Data management and governance considerations
  - Field data captured with a data collection tool; locations and sampling activities are georeferenced for mapping and monitoring purposes.
  - Data organization (CBG/CNT/EPF) reflects chain-of-custody and sample processing steps; clear labeling supports reproducibility and auditing.
  - While explicit data-sharing policies are not described, the structure emphasizes transparency and traceability of specimens and their processing.