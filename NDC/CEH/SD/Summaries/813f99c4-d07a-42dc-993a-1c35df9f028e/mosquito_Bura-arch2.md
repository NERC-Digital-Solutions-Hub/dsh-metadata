# Experimental Design/Sampling Regime

- Objective
  - Assess the effect of irrigation on the abundance of various mosquito species, particularly Rift Valley fever vectors.
  - Explore how the irrigation effect varies with season (more apparent during the dry season when water is limited to irrigated farms).
  - Employ a repeated sampling design across wet/dry seasons and across active vs inactive irrigation periods.

- Study design and sites
  - Sampling within and outside the irrigation scheme to enable comparison.
  - Control site: Murukani village (15 km east of irrigated farms) and pastoral areas in Ijara, Garissa.
  - Seasonal and irrigation activity dimensions built into the sampling plan.

- Field collection methods
  - Adult mosquitoes collected with CO2-baited CDC light traps from 4:00 pm to 6:00 pm for 3 consecutive days.
  - 10 traps deployed per night in homesteads and surrounding irrigated farms.
  - Traps placed in livestock night sheds, bushes, houses, farms, and forested areas.
  - Daily collection performed each morning; specimens preserved for downstream processing.
  - Early sampling used collection bags directly transferred to field lab; later, centrifuge tubes were introduced to facilitate field-to-lab transport.
  - All traps and larval sites were georeferenced.

- Laboratory processing and identification
  - Mosquitoes (adults and those emerging from larvae) immobilized and preserved for analysis.
  - Identification to species using established keys (Edwards 1941; Gillies & de Meillon 1968; Jupp 1986; Gillies & Coetzee 1987; Harbach 1988).
  - Specimens pooled up to 25 mosquitoes per pool; samples kept on ice to preserve material for virus isolation work in cell culture.
  - Identified mosquitoes preserved at -70°C for future analyses.
  - Trapping and larval sites retained for future mapping and analysis.

- Data management and dataset structure
  - One CSV file: DDDAC_Kenya_entomology.csv containing 9 variables.
  - Variables and descriptions:
    - date: date of sampling
    - latitude: decimal degrees
    - longitude: decimal degrees
    - cbg: collection bag/trap identification number
    - cnt: centrifuge tube with mosquitoes linked to trap/CBG (empty if no sample)
    - epf: Eppendorf tube/pool with identified mosquitoes
    - species: species in the pool
    - sex: sex of mosquitoes by species in the pool
    - Pool_size: number of mosquitoes in the pool
  - Notes: missing data (na) indicate empty cnt; missing latitude/longitude due to equipment failure.

- Quality control and data validation
  - Mosquito identification performed by expert taxonomists.
  - Species verification confirmed by internationally certified mosquito taxonomists prior to pooling and preservation.
  - All collection and processing locations georeferenced to support mapping and spatial analyses.

- Geospatial and storage considerations
  - Georeferenced sampling and larval sites to support mapping and spatial monitoring.
  - Samples preserved for downstream analyses, including potential virus isolation studies.