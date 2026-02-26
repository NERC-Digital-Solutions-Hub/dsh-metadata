# Radiological Environmental Sample Data Schema

- Purpose and scope
  - Defines a structured data schema for recording environmental sample analyses related to radiological measurements.
  - Supports tracking of sample metadata, species attribution, and quantitative concentration ratios across numerous elements with associated variability metrics.
  - Facilitates data quality assurance, standardised analysis outputs, and publication/portal workflows.

- Core sample metadata
  - Sample_Code: unique sample identifier
  - Species: Latin name of the sampled species
  - RAP: International Commission on Radiological Protection (ICRP) Reference Animals and Plants (RAP) attribution for the species
  - Sample_Description: portion of the sample that was analysed
  - Mean_Value: indicates whether the reported mean is geometric or arithmetic
  - Standard_Deviation_I-127 and Standard_Deviation_[Element]: (per element) standard deviation terms corresponding to the mean

- Element-specific data structure (pattern)
  - For each element (e.g., I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cs, Tl, Pb, U, etc.):
    - [Element]: denotes the mean concentration ratio
      - 1 = Mean concentration ratio
      - 2 = unitless
      - 3 = Geometric or arithmetic mean as identified by Mean_Value
    - Standard_Deviation_[Element]: accompanying variability metric
      - 1 = Standard deviation
      - 2 = unitless
      - 3 = Geometric or arithmetic standard deviation as identified by Mean_Value
  - Note: Some entries show a consistent unitless and geometric/arithmetic interpretation across elements; for several elements, the exact fields are represented with placeholders or extended formatting in the source, but the intended pattern is a per-element mean, unit, and mean-type specification plus a corresponding standard deviation set.

- Data handling and usage for Analysts Monitoring the Environment
  - Data verification, quality assurance, cleaning, and transformation of the collected sample information.
  - Analysis using standardised methods to produce outputs such as comparative concentration ratios and associated uncertainty.
  - Presentation of results in clear formats (reports, maps, charts) and storage/upload to appropriate data portals to support monitoring over time.

- Key challenges and opportunities highlighted
  - Increasing the value of the created datasets by linking them with additional relevant data (beyond single-use analysis).
  - Ensuring accessibility to the underlying data used to produce final outputs, enabling broader scrutiny and reuse.