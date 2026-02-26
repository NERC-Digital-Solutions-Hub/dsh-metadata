# Soil Core Dataset Metadata Fields

## Overview
- A metadata-rich dataset for soil core samples across field sites, capturing treatment conditions (biochar amendment, wetted treatment), sampling context (site, depth, replicate, timesample), and a range of chemical and physical soil measurements taken before and during incubation.
- Includes both measured values (e.g., pH, carbon and nitrogen contents, extractable nutrients) and physical properties (bulk density, particle density, porosity, weight).

## Key fields and meanings

- Identification and sampling context
  - soilcorenumber: Unique identifier for each soil sample/core.
  - site: Field site where the sample was collected.
  - depth: Depth of the soil sample from the soil surface.
  - replicate: Replicate number for samples from the same treatment.
  - timesample: Time at which the sample was taken.
  - biocharamendment: Indicates if the sample was amended with biochar (yes/no or category).
  - wettedtreatment: Indicates if the sample was periodically wetted to a high water content (yes/no or category).

- Chemical properties
  - pH.water: Soil pH measured in water at a 1:2.5 ratio.
  - total.C.percent: Total carbon content as a percentage.
  - total.N.percent: Total nitrogen content as a percentage.
  - CN ratio: Ratio of total carbon to total nitrogen (C/N).
  - extract.nh4-n.mgkg: Extractable ammonium (mg per kg of soil).
  - extract.no3-n.mgkg: Extractable nitrate (mg per kg of soil) after the start of incubation.

- Physical properties and mass
  - drysoilweightg: Dry soil weight in grams for the soil core.
  - gravwatercontproportion.before: Gravimetric water content as a proportion before incubation.
  - bulkdensitygcm3.before: Bulk density before the start of incubation (g/cm3).
  - particledensitygcm3: Particle density of the soil (g/cm3).
  - totalporosityproportionbefore: Total porosity before incubation, computed as 1 - (bulk density / particle density).
  - wfpsproportionbefore: Water-filled pore space before incubation, calculated as gravimetric water content * (bulk density / total porosity).

## Derived calculations and validation
- totalporosityproportionbefore is derived from bulkdensitygcm3.before and particledensitygcm3.
- wfpsproportionbefore is derived from gravwatercontproportion.before, bulkdensitygcm3.before, and totalporosityproportionbefore, using the provided formula gravwatercontproportion.before * (bulkdensitygcm3.before / totalporosityproportionbefore).

## Metadata, quality, and governance considerations
- Standards and consistency
  - Enforce uniform units across records (percent, mg/kg, g, g/cm3, dimensionless proportions).
  - Use consistent field naming and definitions to support interoperability.

- Data provenance and documentation
  - Document sampling times, incubation status, and any transformations or processing applied to the data.
  - Track data contributors and versioning of the dataset.

- Sharing and lifecycle management
  - Assess data availability and potential restrictions (embargoes, proprietary concerns).
  - Plan and execute data uploads to relevant data portals; maintain catalog entries for discoverability.
  - Consider documenting work performed on datasets to support reproducibility.

- Data quality and support
  - Provide guidance and tools to data creators to meet metadata and format standards.
  - Perform quality assurance on received data, including unit checks and plausible value ranges.
  - Address incomplete or delayed data submissions by engaging with data creators.

## Particular Challenges (context for stewardship)
- Aligning user needs with the dataset structure and ensuring complete metadata.
- Timely receipt of data from multiple creators and systems.
- Standardizing metadata across diverse formats and older databases.
- Handling large datasets and integrating data from outdated or bespoke systems.