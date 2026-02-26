# (Manual n°3) Period 2014 - 2016

## Overview
- Laboratory: Laboratoire des RadioIsotopes (LRI) - University of Antananarivo; national reference for soil and plant physico-chemical analyses.
- Scope: soil handling/preparation, soil physical and chemical analyses, soil biological activity; end products include datasets archived at a central data centre (EIDC) and linked publications.
- Purpose for Data Stewards: establish robust data governance practices around sample registration, analysis workflows, data provenance, and data publication.

## Data registration and metadata
- Sample registration and storage handled by LRI; field samples are received, registered, and tracked by the lab responsible.
- For each sample, a rich set of metadata is captured and recorded with a unique sample ID, including:
  - Person in charge (sampling lead)
  - Program or project name and ID
  - Sampling period
  - Sampling site
  - Sample type (soil, plant, etc.)
  - Sampling method
  - Sampling depth
  - Land cover or cropping system
  - Number of samples, and list of sample IDs (e.g., P01_001 to P01_090)
  - Analysis requirements (e.g., Olsen P, NO3/NH4, SOC, etc.)
- A concordance process links field IDs to lab IDs; a final electronic list documents this concordance for traceability.

## Data generation and processing
- Sample preparation and analyses:
  - Drying, grinding, sieving of soils as per analysis method.
  - SOC: Walkley and Black chemical method; subset analyzed chemically; full set scanned by Mid-Infrared Spectroscopy (MIRS) for model development.
  - Texture: chemical analyses plus MIRS for model development; fractionation via standard procedures (AFNOR 1999) and pipette method for silt/clay.
  - Bulk density: determined from dry soil weight after removing >2 mm fraction.
  - External analyses: natural 13C abundance (13δ) performed at specialized external labs on selected samples.
- Data modeling and prediction:
  - MIRS data used to develop prediction models for SOC, texture, and 13δ based on lab-measured properties.
  - Models trained on subsets (e.g., ~1/3 of samples for model development; remaining ~2/3 predicted).
- Documentation and procedures:
  - Methods and workflow documented to support reproducibility and data reuse.

## Data management, quality assurance, and provenance
- Data capture aligns with standardized laboratory procedures; meticulous sample tracking to maintain linkage between field and lab data.
- Quality assurance steps include:
  - Registration and storage of all samples by the lab responsible.
  - Regular checks to ensure all listed samples arrived in the laboratory.
  - Final electronic concordance between field IDs and lab IDs.
- Data storage and archiving:
  - All generated datasets archived at Environmental Information Data Centre (EIDC).
  - Datasets associated with published or in-process publications; datasets are traceable to the underlying analyses and models.

## Data publication and sharing
- Data publication status: datasets are published or in process of publication.
- Publications associated with the work (e.g., studies on land-use changes, soil organic carbon variability, and organic carbon stocks following land-cover changes in Madagascar) are listed as evidence of data use.
- Repository: Environmental Information Data Centre (EIDC) serves as the primary archival and sharing platform for datasets.

## Standards, interoperability, and governance implications
- Uses recognized standards and references to ensure comparability:
  - AFNOR (1999) quality standards for soil
  - Walkley-Black (1934) method for soil organic matter
- MIRS-based modeling supports scalable prediction across larger datasets while maintaining traceable methodology.
- Governance implications for Data Stewards:
  - Maintain clear, machine-readable metadata for all samples and analyses.
  - Ensure robust linkage between field and laboratory identifiers.
  - Enforce standardized procedures and documentation to support reproducibility and data reuse.
  - Ensure timely data archiving in a central repository (EIDC) and maintain records of data publication status.