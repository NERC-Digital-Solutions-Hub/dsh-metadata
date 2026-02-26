# Glastir Monitoring & Evaluation Programme

- Aims to monitor Glastir scheme effects on soil and environment in Wales, generate evidence on soil quality outcomes related to climate change, biodiversity, soil and water quality, and woodland expansion; quantify status and trends in soil quality independent of Glastir interventions.
- Operates under a four-year rolling survey (2013–2016 first cycle) with two components:
  - Wider Wales Component for baseline estimates, national trends, and national reporting.
  - Targeted Component linked to Glastir priority areas.
- Uses a common spatial unit (1 km squares) to enable integration across components and potential future linkage with other surveys (e.g., Countryside Survey GB).

- Sampling framework
  - Total of 300 1 km squares over the four-year cycle.
  - Half randomly sampled within Land Classification strata (to maximize environmental heterogeneity between strata and minimize within-stratum variability).
  - Half targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea are excluded.
  - Spatial distribution mapped at 10 km resolution to protect data confidentiality.

- Field sampling methods
  - Within each square, collect soil samples from 5 randomly dispersed locations where feasible.
  - Use a 15 cm soil core (C-core) coinciding with vegetation surveys.
  - Cores refrigerated and shipped within a few days to laboratories (Centre for Ecology & Hydrology, Bangor and Lancaster).

- Laboratory protocols and analytical methods
  - Soil organic matter and carbon metrics
    - Loss on Ignition (LOI) to estimate soil organic matter and derive soil carbon concentration (C_FE_LOI, C_FE_CARBO_CONC_GPERKG = LOI% × 5.5).
    - Total soil organic carbon (SOC) measured after inorganic carbon removal using an Elementar Vario-EL analyser; QA with in-house reference materials.
  - Nutrients and phosphorus
    - Total phosphorus (C_FE_PTOTAL) via acid digestion and colorimetric measurement.
    - Olsen phosphorus (C_FE_POLSEN) for arable/improved grassland; measured by molybdate blue chemistry.
    - QA with duplicates and blanks every ~25 samples.
  - Soil chemical properties
    - pH in deionised water (C_B_PH_DIW) and in CaCl2 (C_B_PH_CACL2); QA with internal standards.
    - Electrical conductivity (C_B_EC) of soil slurry; QA with internal standards.
  - Physical properties
    - Bulk density of fine earth (C_FE_BULK_DENSITYGPERCM3) via a 15 cm core.
    - Volumetric water content (C_FE_VWC) derived from bulk density and gravimetric water content.
    - Soil water repellency (C_FE_SWRMEDIAN) via Water Drop Penetration Time (WDPT) with video capture for timing.
  - Derived and associated data
    - Several derived units and QA/QC scripts produced (e.g., C_FE_CARBO_CONC_GPERKG, data QA scripts in R).

- Data quality control and QA/QC
  - Internal standards run in each batch; repeat analysis if LOI deviates >2 standard deviations from historical means.
  - Duplicates, blanks, and matrix-matched blanks included every ~25 samples for P and Olsen P; QA procedures documented for each metric.
  - Use of R scripts for calculation of derived variables and QA/QC checks.

- Data management, provenance, and sharing
  - Data collected and managed by CEH (Centre for Ecology & Hydrology) with designated QA and database management roles.
  - Archive and data management support including field coordination, laboratory analysis, data processing, and sample tracking.
  - Primary dataset described: GMEP_SOIL_METRICS_2013_16.csv, including site identifiers, coordinates, year, soil metrics (C, N, P, pH, EC, bulk density, VWC, SWR), and derived variables; dataset uses -9999.999 to denote missing values.
  - Map references and confidentiality: distribution plotted at 10 km resolution; detailed coordinates managed to protect confidentiality.

- Data model and example schema (GMEP_SOIL_METRICS_2013_16.csv)
  - Key fields include: SQ_ID, PLOT_TYPE, PLOTNUM, EASTING_10KM, NORTHING_10KM, LC (Land Classification), YEAR, C_FE_CTOTAL, C_FE_LOI, C_FE_NTOTAL, C_FE_PTOTAL, C_FE_POLSEN, C_B_PH_DIW, C_B_PH_CACL2, C_B_EC, C_FE_BULK_DENSITYGPERCM3, C_FE_VWC, C_FE_SWRMEDIAN, among others.
  - Descriptions provided for each metric (units and measurement context) and relationships to laboratory methods.
  - Data structure supports integration with national datasets and potential future analyses.

- Practical considerations and limitations
  - Some habitats have Olsen-P data limited to arable and improved grassland; other habitats have missing values.
  - The approach emphasizes interoperability by aligning with Countryside Survey methodologies to facilitate future data integration.
  - Emphasis on capturing multi-metric, ecosystem-scale data in a single visit where possible.

- References and acknowledgments
  - Methodological and technical references: Avery & Bascomb (Soil Survey Laboratory Methods), Bunce et al. (ITE Land Classification), Emmett et al. (Countryside Survey), Glastir Monitoring & Evaluation Programme (annual report), and Defra soil strategy references.
  - CEH and partner teams (including Bangor University) highlighted as responsible for QA, lab analyses, data management, and field operations.