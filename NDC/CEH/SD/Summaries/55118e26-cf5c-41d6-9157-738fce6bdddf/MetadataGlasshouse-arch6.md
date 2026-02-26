# PhenotypeGlasshouse.txt

- A phenotypic dataset for pine species grown in a glasshouse, with accompanying genotype data. It includes geographic, familial, and temporal phenotypic measurements to support analysis of growth and development across individuals and populations.

## Data Files and Key Columns

- PhenotypeGlasshouse.txt
  - Core fields:
    - Species (MU = Pinus mugo; SY = Pinus sylvestris; UN = Pinus uncinata)
    - Country
    - Population, PopCode
    - PopCodeWachowiak2018 (reference to Wachowiak et al. 2018)
    - Family (shared maternal code)
    - Latitude, Longitude (decimal)
    - Block (1–25)
    - ID (unique tree identifier)
    - Genotyped (0 = no, 1 = yes)
  - Phenotypic measures (timing and size):
    - BS2010: Bud set in 2010 (days since a reference date)
    - BB2011: Budburst in 2011 (days since reference)
    - BB2012: Budburst in 2012 (days since reference)
    - H2011, H2012, H2013: Height in years 2011–2013 (cm)
    - I2012, I2013: Height increments (growth) for 2012 and 2013 (cm)
- GenotypeGlasshouse.txt
  - Columns:
    - snpid: Name of SNP marker
    - Additional columns: SNP genotype data (examples given as UN18_26_16)
    - ID linkage: Unique tree identifier matching Phenotype file

## Data Types and Units

- Numeric
  - Latitude/Longitude: decimal degrees
  - Height: centimeters (cm)
  - Days to events (BS2010, BB2011, BB2012): days
  - Height increments (I2012, I2013): cm
- Categorical/Codes
  - Species codes: MU, SY, UN
  - Genotyped: 0/1 indicator
- Identifiers
  - ID: unique per-tree
  - PopCode, PopCodeWachowiak2018: population identifiers and cross-reference

## Data Provenance and References

- PopCodeWachowiak2018 provides a standardized population code from Wachowiak et al. (2018).
- The dataset pairs phenotype measurements with genotype data (SNP markers) via the unique ID.

## Use Cases and Outputs

- Analytics and data products
  - Dashboards and pivot tables enabling self-serve exploration by population, family, and genotype status.
  - Time-series and growth analyses across 2011–2013.
  - Phenotype-genotype associations using SNP data from GenotypeGlasshouse.txt.
  - Spatial analyses leveraging latitude/longitude to compare populations.
- Data transformations
  - Cleaning and standardizing formats across multiple fields.
  - Merging phenotype and genotype data via ID.
  - Computing derived metrics (e.g., growth rates, timing distributions).

## Data Quality and Challenges

- Common issues
  - Patchy data across years or individuals
  - Diverse formats and data systems for integration
  - Communication of complex results to non-specialists
  - Ensuring outputs are shared and reused broadly
- Considerations for Data Support
  - Verify completeness and consistency of ID mappings between files
  - Validate units and ranges for timing and height data
  - Coordinate with domain experts to interpret phenotypic timing measures

## Next Steps for Data Support

- Data preparation
  - Clean and validate PhenotypeGlasshouse.txt and GenotypeGlasshouse.txt
  - Ensure robust join keys (ID) and consistency of population codes
- Tooling and outputs
  - Create example dashboards/pivot templates for end users
  - Provide guidance on using SNP data for association analyses
- Stakeholder engagement
  - Gather feedback on desired metrics and visualizations
  - Share early prototypes and iterate based on user input

## Key Definitions and Notes

- Species codes:
  - MU: Pinus mugo
  - SY: Pinus sylvestris
  - UN: Pinus uncinata
- Measurements:
  - BS2010, BB2011, BB2012: timing measures expressed as days since a start date
  - H2011–H2013: plant height in centimeters
  - I2012, I2013: height increments between years in centimeters
- Population references
  - PopCodeWachowiak2018 links populations to a published code for traceability
- Genotype data
  - Genotyped flag indicates inclusion in the SNP array
  - Genotype data organized as SNP columns with a per-tree ID linkage