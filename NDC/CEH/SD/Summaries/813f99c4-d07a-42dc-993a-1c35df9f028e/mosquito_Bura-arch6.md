# Experimental Design/Sampling Regime

- Objective: Assess the effect of irrigation on the abundance of various mosquito species, focusing on vectors relevant to Rift Valley fever, and examine how irrigation effects vary by season (dry vs wet).

- Study design:
  - Analytical study comparing sites inside and outside the irrigation scheme.
  - Repeated sampling to cover wet and dry seasons and periods when irrigation is active vs inactive.
  - Trapping conducted for three consecutive days per site to reduce temporal variability.

- Field work and collection methods:
  - Adult mosquitoes collected with CO2-baited CDC light traps, set from 4:00 pm to 6:00 pm for 3 consecutive days.
  - Ten traps per night across homesteads and irrigated farms in ten villages; a control site at Murukani village and pastoral areas in Ijara, Garissa.
  - Daily collection, with specimens moved to a field laboratory in collection bags (CBG) or later via centrifuge tubes (CNT) and Eppendorf tubes (EPF) after sorting.
  - Traps placed in livestock night sheds, bushes, houses, farms, and forested areas.
  - Field data captured using a data collection tool.

- Sample processing and storage:
  - Mosquitoes immobilized with 99.5% triethylamine and preserved in liquid nitrogen; transported to KEMRI for identification and processing.
  - Sorting and pooling performed with up to 25 mosquitoes per pool.
  - Identified mosquitoes preserved at -70°C for future analyses.
  - All trapping and larval collection sites georeferenced for mapping.

- Species identification and pooling:
  - Identification to species using Edwards (1941), Gillies & de Meillon (1968), Jupp et al. (1986), Gillies & Coetzee (1987), Harbach (1988) keys.
  - Identification performed by expert taxonomists; accuracy confirmed by internationally certified mosquito taxonomists prior to pooling and preservation.

- Data management and dataset structure:
  - Dataset: a single CSV file named DDDAC_Kenya_entomology.csv.
  - Variables (9) and descriptions:
    - date: date of sampling
    - latitude: decimal degrees latitude
    - longitude: decimal degrees longitude
    - cbg: collection bag/trap identification number
    - cnt: centrifuge tube with unidentified mosquitoes linked to trap/CBG (empty if no sample; 'not_used' indicates direct transfer to EPF after sorting)
    - epf: Eppendorf tube/pool with identified mosquitoes
    - species: species of identified mosquitoes in the pool
    - sex: sex of the mosquitoes by species in the pool
    - Pool_size: number of mosquitoes in the pool
  - Data quality notes:
    - 'na' indicates no data for a field and corresponds to empty cnt.
    - Missing latitude/longitude values due to equipment failure.

- Quality control:
  - Mosquito identifications validated by expert taxonomists and internationally certified specialists prior to pooling and preservation.

- References for identification keys:
  - Edwards FW (1941)
  - Gillies MT & de Meillon (1968)
  - Jupp PG (1986)
  - Gillies & Coetzee (1987)
  - Harbach RE (1988)

- Data use implications for analysis and reporting:
  - Structured, georeferenced data enabling spatial analyses and mapping of mosquito distributions.
  - Clear provenance from field collection to laboratory processing supports reproducibility and potential data products (dashboards, summaries) for monitoring irrigation-related vector dynamics.