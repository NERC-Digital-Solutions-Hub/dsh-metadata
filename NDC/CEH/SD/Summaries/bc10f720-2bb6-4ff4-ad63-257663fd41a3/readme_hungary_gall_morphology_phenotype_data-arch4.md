# Morphology phenotype data of 88 types of galls induced on oak trees by cynipid gallwasps from 6 sites in Hungary, 2000-2003: Supporting information

- Purpose and scope
  - Dataset of quantitative and categorical scores describing phenotypic attributes of 88 gall types induced on Quercus spp. by cynipid gallwasps.
  - Collected from 6 sites in Hungary during 2000–2003.
  - Includes separate phenotypes for sexual and asexual generations; 31 sexual-generation galls and 58 asexual-generation galls across 69 cynipid species.

- Data collection and sampling
  - Galls collected from six sites in Hungary (map referenced in the document).
  - For measurements, samples consisted of 10 galls per gall type, collected across sites 1–5.
  - Continuous measurements taken with digital calipers.
  - Mature galls were identified by mature larval/pupal chambers; maturity confirmed to validate data.

- Data types and structure
  - 17 data columns per gall type/generation, covering categorical, ordinal, and continuous variables.
  - Each row represents a single cynipid species and generation for the mature gall.
  - Continuous variables are in millimeters or cubic millimeters; all measurements are tied to gall structure.

- Variables included (definitions and data types)
  - Linnean species name (string)
  - Generation (Asexual or Sexual) (categorical)
  - Hair (binary: 1 = hairy, 0 = not hairy)
  - Dense_spines (binary)
  - Sparse_spines (binary)
  - Sticky (binary)
  - Space (binary)
  - Dummy (binary)
  - Peduncle (binary)
  - Nectar (binary)
  - Dehisce (binary)
  - Tough (ordinal, 1–4;  -999 for missing data)
  - Shape (categorical: cone, cylinder, sphere)
  - Radius (continuous, mm)
  - Height (continuous, mm; not provided for spherical galls)
  - Gall_Size (continuous, mm^3; volume based on Shape category)
  - Locularity (categorical: Unilocular or Multilocular)

- Data quality, verification, and quality control
  - Categorical variables are straightforward in mature galls; maturity confirmed via larval/pupal chambers.
  - Tough validated with continuous penetration scores (QTS-25) where available.
  - Gall identifications based on external diagnostic features by experienced field staff; DNA barcoding used when needed (mitochondrial cytochrome b and nuclear ITS2) for confirmation.
  - Data reported as carefully checked for errors.

- Metadata, units, and missing data
  - Continuous variables reported in millimeters or cubic millimeters (mm or mm^3).
  - Missing data flagged with -999 (including some species/generation combinations with no data).
  - Height not provided for spherical galls; some Tough values missing for certain gall types.
  - Data are organized with explicit variable definitions to support interoperability and reuse.

- Relevance and context
  - Data capture properties of the internal and external structure of mature galls; relevant to studies on host niches and defensive phenotypes, and broader parasitoid wasp community structure.
  - References linked to data interpretation and prior work:
    - Bailey et al. (2009)
    - Nicholls et al. (2012)
    - Roskam (2019)

- Practical considerations for data leaders
  - Clear, standardized variable definitions and units improve discoverability and reuse.
  - Explicit handling of missing data (-999) and documented measurement protocols support data quality and traceability.
  - DNA barcoding as a supplementary validation step demonstrates robust data governance.
  - Potential challenges include data gaps across generations and sites, heterogeneity in measurement completeness, and the need for careful interpretation when comparing across gall shapes (e.g., height not collected for spheres).