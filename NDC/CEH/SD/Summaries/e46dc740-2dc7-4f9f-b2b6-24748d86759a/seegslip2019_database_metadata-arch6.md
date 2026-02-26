# pasture fed livestock farms across Great Britain, 2019

- A data collection by the UK Centre of Ecology & Hydrology (with BBSRC funding) to evidence the impacts of pasture-fed livestock practices on grassland ecology, sward composition, and soil quality in Great Britain.
- Focuses on grassland significance for biodiversity, water filtration, nutrient cycling, and carbon storage; includes context on the Pasture Fed Livestock Association (PFLA) certification standards.

## Overall aims and scope

- Document patterns in vegetation, soil properties, and farm management across pasture-based farms.
- Compare mob grazing versus set-stocking practices and, where applicable, species-rich versus traditional leys.
- Produce data products to enable analysis and public exploration of grassland ecology under pasture-based systems.
- Data originate from 17 farms (PFLA members) surveyed in 2019; anonymised farm identifiers included.

## Experimental design and sampling

- Farms: 17 across Great Britain; 10 fully certified by PFLA, 7 with intentions to certify.
- Field sampling: two paired fields per farm when possible (mob-grazed vs set-stocking, or species-rich ley vs traditional ley); occasionally more field pairs were sampled.
- Timing: field visits between May and September 2019; on-site farmer interviews about management practices.
- Anonymisation: farms and fields anonymised; landowner confidentiality preserved.

## Data collected and key variables

- Vegetation data (plots and species): 3 randomly placed 2 x 2 m quadrats per field; records include species name, cover (%), flowering status, canopy/shrub/ground heights, wormcasts, soil surface condition, and biomass in a sub-sample.
- Biomass: dried weights by plant groups (grass, dicot, cereal) and total biomass per sample.
- Soils and chemistry: multi-depth soil sampling along a W-shaped transect; cores and bulked samples analyzed for chemistry, moisture, bulk density, and other physical/chemical properties.
- Field/farm management: on-site questionnaire covering sward longevity, grazing type and stocking densities, inputs, and other management practices.
- Additional data: soil eDNA sub-samples deposited in the European Nucleotide Archive (ENA) under accession PRJEB46195.
- Data files (CSV) and contents:
  - SEEGSLIP_PLOTS_2019.csv — vegetation plot attributes and field/plot metadata.
  - SEEGSLIP_SPECIES_2019.csv — species-level data per plot, including cover and flowering.
  - SEEGSLIP_BIOMASS_2019.csv — dried biomass weights by plant group.
  - SEEGSLIP_SOIL_2019.csv — soil chemistry and physical properties by field/depth.
  - SEEGSLIP_FARMDATA_2019.csv — farm-level management information from farmer questionnaires.
  - SEEGSLIP_FIELDS_2019.csv — field-level management details and field characteristics.
  - SEEGSLIP_STOCK_2019.csv — stocking and supplementary feeding information.
- Data access and identifiers:
  - Farms anonymised with ID numbers/sites; data joinable by FARM_NO and FIELD_ID.
  - Soil and vegetation data aligned with field sampling dates (SURVEY_START/SURVEY_END).

## Data structure and quality

- Data structure: seven CSV tables capturing plot-level vegetation, species, biomass, soil chemistry, farm-level management, field-level management, and stock information.
- Soil analyses and quality controls:
  - LOI, SOC, total N, P, Olsen P, pH (in water and CaCl2), electrical conductivity, bulk density, particle size distribution, aggregate stability, CaCO3 content, and total C/N/P metrics.
  - Quality control includes internal standards, duplicate checks, and calibration procedures (e.g., LOI QC, pH QC, conductivity QC).
  - DNA sub-sampling for eDNA analyses reported separately in ENA data.
- Data notes:
  - Some data values use -999 to denote missing data.
  - Fields include multiple descriptive codes (e.g., SLOPE, SHADE, CANOPY_HEIGHT) with predefined categories.
  - Anonymisation ensures landowner confidentiality while preserving analytical usefulness.

## Data management and potential uses

- Primary data products enable self-serve analyses of:
  - Relationships between grazing regime (mob vs set-stock) and vegetation structure, diversity, and biomass.
  - Soil health indicators (SOC, N, P, pH, bulk density, moisture) across field types and depths.
  - Impacts of management practices (rest periods, fertilizer use, ley types) on soil and plant parameters.
- Potential applications:
  - Comparative studies of mob grazing versus traditional practices on grassland ecology.
  - Development of dashboards or reports for farmers, policy makers, and researchers.
  - Cross-table analyses by FARM_NO/FIELD_ID to link management with ecological outcomes.
- Considerations for data reuse:
  - Join SEEGSLIP_PLOTS_2019.csv, SEEGSLIP_SPECIES_2019.csv, and SEEGSLIP_BIOMASS_2019.csv for plot-level vegetation insights.
  - Use SEEGSLIP_SOIL_2019.csv and SEEGSLIP_FARMDATA_2019.csv to explore soil properties alongside farm management.
  - Leverage SEEGSLIP_FIELDS_2019.csv and SEEGSLIP_STOCK_2019.csv for field-level and stocking information.
  - Integrate eDNA data from ENA PRJEB46195 for microbial/soil biological context.

## References and related materials

- Background literature and methodological references provided in the dataset documentation (CS soil manuals, Bunce et al. land classification, and related emissions/soil analysis standards).
- Further Reading:
  - Seaton et al. 2023: soil microbial communities and field heterogeneity.
  - Wagner et al. 2023: mob grazing as a nature-based solution in British farms.