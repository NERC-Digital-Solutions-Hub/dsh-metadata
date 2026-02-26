# Experimental Design/Sampling Regime

- Objective and design
  - Analytical study to assess how irrigation affects abundances of mosquito species important for Rift Valley fever transmission.
  - Sampling sites chosen inside and outside the irrigation scheme to enable comparison.
  - Hypothesized that irrigation effects would be more evident in the dry season when water is limited to irrigated farms.
  - Repeated sampling across wet and dry seasons and during active vs. inactive irrigation.
  - Each sampling visit involved 3 consecutive days of trapping at a given site to minimize between-period variability.

- Field work and collection methods
  - Adult mosquitoes collected with CO2-baited CDC light traps, 4:00 pm to 6:00 pm for 3 consecutive days.
  - 10 traps per night in homesteads and irrigated farms across ten villages; control site in Murukani (15 km east) and pastoral areas in Ijara, Garissa.
  - Mosquitoes collected each morning, transported to field lab for sorting.
  - Specimens immobilized with 99.5% triethylamine and preserved in liquid nitrogen for transport to KEMRI lab.
  - Traps placed in livestock night sheds, bushes, houses, farms, and forested areas.
  - Mosquitoes transferred from collection bags to centrifuge tubes (CNT) and then to Eppendorf tubes (EPF) after sorting; initial surveys transferred directly to EPF in CBGs.
  - CNTs later introduced to improve field-to-lab transport.
  - All mosquitoes trapped and larval samples georeferenced.

- Processing and storage
  - Collected adults and emergent larvae identified to species; identification preserved on ice to support virus isolation in cell culture.
  - Identified mosquitoes pooled in groups of up to 25.
  - Identified specimens preserved at -70°C for future analysis.
  - All trapping and larval-sampling sites georeferenced for mapping.

- Data capture and dataset details
  - Field data recorded in a data collection tool.
  - Dataset filename: DDDAC_Kenya_entomology.csv
  - Dataset structure: 9 variables
    - date: sampling date
    - latitude: decimal degrees
    - longitude: decimal degrees
    - cbg: collection bag/trap ID
    - cnt: centrifuge tube with mosquitoes linked to trap/CBG (empty indicates no sample; "not_used" indicates direct EPF transfer after sorting)
    - epf: Eppendorf tube/pool with identified mosquitoes
    - species: species in the pool
    - sex: sex of mosquitoes by species in the pool
    - Pool_size: number of mosquitoes in the pool
  - Missing data notes: NA indicates no data; missing lat/long due to equipment failure
  - Quality control: mosquito identification conducted by expert taxonomists; accuracy confirmed by internationally certified taxonomists prior to pooling and preservation

- Data quality and governance considerations for data stewards
  - Standardized identification methods and pooling procedures support data consistency.
  - Georeferenced sampling sites enable accurate mapping and subsequent discovery.
  - Clear lineage of samples (CBG → CNT → EPF) with associated metadata supports traceability.
  - Cold-chain preservation (-70°C) and field-to-lab transport steps should be documented for reproducibility and future reuse.
  - Metadata definitions (variable meanings and coding) facilitate data discovery and interoperability for reuse in broader datasets.