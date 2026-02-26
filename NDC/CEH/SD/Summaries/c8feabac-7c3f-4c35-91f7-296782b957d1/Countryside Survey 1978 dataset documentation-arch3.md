# Broad Habitat Area Estimates by Land Class for Great Britain

- Purpose and scope
  - National estimates of Broad Habitat stock (Habitats 1–21, excluding 15 and 20) for 1978, calculated using the 1990 ITE Land Classification.
  - Derived from the Countryside Survey (CS) with a focus on estimations by Land Class to support habitat monitoring and change detection.
  - Data underpin: baseline for measuring habitat change over 30 years (1978 vs later years) and for informing habitat-related policy and management decisions.

- Data files and contents
  - CS1978_Estimates_by_LC.csv
    - Columns include: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha)
    - Provides national estimates of Broad Habitat area by Land Class, with 95% confidence intervals.
    - Notes: Broad Habitat codes exclude Land Classes 15 and 20; derived from the 1990 ITE Land Classification (Bunce et al., 1996; 1981 publications referenced).
  - CS78_BH1_17.tif
    - Raster at 1 km pixel resolution, representing Broad Habitat composition as a percentage of each Land Class area.
    - Each band corresponds to a Broad Habitat class (bands 1–17; excluding 15 in the mapping described).
    - Band-to-habitat mapping (examples):
      - Band 1 = Broadleaved Mixed and Yew Woodland
      - Band 2 = Coniferous Woodland
      - Band 3 = Boundary and Linear Features
      - Band 4 = Arable and Horticulture
      - Band 5 = Improved Grassland
      - Band 6 = Neutral Grassland
      - Band 7 = Calcareous Grassland
      - Band 8 = Acid Grassland
      - Band 9 = Bracken
      - Band 10 = Dwarf Shrub Heath
      - Band 11 = Fen, Marsh, Swamp
      - Band 12 = Bog
      - Band 13 = Standing Open Waters and Canals
      - Band 14 = Rivers and Streams
      - Band 16 = Urban
    - Pixel size: 1 km; Coordinate system: British National Grid; Projection: Transverse Mercator Great Britain (OSGB1936)

- Data provenance and usage rights
  - Data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©.
  - All use of Countryside Survey data requires formal acknowledgement.
  - Supporting publications and references provided to document methodology and context (linkages to CS project website and technical reports, Land Classification framework, and habitat guidance).

- How this supports monitoring frameworks
  - Provides a clear, auditable baseline of Broad Habitat area by Land Class for 1978, enabling trend analysis when combined with subsequent CS data.
  - Facilitates national-scale habitat monitoring, policy scrutiny, and evaluation of land-use/habitat management effects over time.
  - The raster (CS78_BH1_17.tif) enables spatial analyses and visualization (e.g., habitat distribution within Land Classes at 1 km resolution).

- Data quality, metadata, and governance considerations for monitoring authors
  - Metadata gaps can hinder reuse; linkage to originators and provenance is essential.
  - Public sharing of underlying data is mandated but can be a barrier; ensure clear data-sharing agreements and governance.
  - Data transformations required to align with Monitoring Frameworks (e.g., cross-walks between Land Classification schemes and current policy-relevant habitat definitions).
  - Potential challenges to apply: data gaps, access/availability delays, siloed datasets, and ensuring datasets remain up-to-date with ongoing monitoring.
  - Recommendations for frameworks: maintain rigorous data quality checks, document transformations, provide transparent lineage, and clearly acknowledge data sources.

- References and acknowledgements
  - Countryside Survey project materials and methodologies (CS website).
  - Wood et al. 2012: Countryside Survey – Measuring Habitat Change Over 30 Years; 1978 Data Rescue Final Report.
  - Scott 2007: CS Technical Report No.4/07 (Statistical methods for deriving national estimates from 1 km survey squares).
  - Bunce et al. 1996; Bunce et al. 1981: ITE Merlewood Land Classification and related user descriptions.
  - Jackson 2000: Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).