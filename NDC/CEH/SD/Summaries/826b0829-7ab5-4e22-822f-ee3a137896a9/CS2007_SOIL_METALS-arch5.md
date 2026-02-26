# Soil metals 2007 [Countryside Survey], Great Britain Version: 1: 02-6-2016

- Dataset scope
  - CS2007_SOIL_METALS.csv contains soil metal concentrations from 402 cores across up to 256 1km squares in Great Britain, surveyed in 2007.
  - Metals measured include Cd, Cr, Cu, Ni, Pb, Zn, Al, Ti, Mn, As, Se, Mo, Hg; additional fields include land class, location, and sample metadata.

- Data structure and columns
  - Spatial and sample identifiers: SQUARE (1km square code), PLOT (plot within square), YEAR (survey year).
  - Concentration measurements: CD, CR, CU, NI, PB, ZN, AL, TI, MN, AS, SE, MO, HG (all in ppm/mg/kg equivalents).
  - Secondary metadata: LC07, LC07_NUM (ITE Land Class 2007 and code), COUNTRY, COUNTY07, EZ_DESC_07 (environmental zone description) and related geographic descriptors.

- Provenance, ownership, and usage rights
  - Data owned by NERC - Centre for Ecology & Hydrology (CEH).
  - All CS data must be acknowledged in use; acknowledgement text specifies ownership and rights.
  - Copyright and database rights apply; use in publications, presentations, and reports should carry the required acknowledgement.

- Laboratory methods and analytes
  - Soil digests analyzed by ICP-OES (2000 survey methods); ICP-MS added in 2007 to expand detectable analytes (up to 27 analytes in CEH’s standard suite).
  - Analytical methods and references: Emmett et al. (2008) Countryside Survey: Soils Manual; additional method details in CS technical reports.

- Quality assurance and quality control (QA/QC)
  - Digestion method: Aqua Regia (as per The Standing Committee of Analysts, 1986) with CEH Lancaster as the analytical laboratory.
  - ISO 17025 accreditation for the laboratory (UKAS).
  - QC targets: total analytical error target of 20% (10% precision, 10% bias); action and warning limits govern rejection of data batches or CRM results when exceeded.
  - Reanalysis: batches with issues may be reanalyzed; persistent QC issues may lead to data rejection or reinstatement after review.
  - Cross-checks and re-analyses ensure consistency across methods and across samples (loss-on-ignition, etc.).

- Sampling design and representativeness
  - Sampling rooted in the Countryside Survey’s rigorous, stratified design based on Land Classes to capture environmental gradients.
  - 591 sample squares surveyed in 2007 (England, Scotland, Wales distribution specified).
  - Soil sampling: 0-15 cm layer collected from specific corners of plots, with consistent relocation across survey years to maintain comparability.
  - Power analyses guided sample size for major measurements; metals analyses used reduced sampling while maintaining confidence in reporting.

- Data processing, documentation, and archiving
  - Field protocols and lab processing guidelines provided to ensure standardized handling from logging to archive.
  - Data manipulation, cross-comparison testing, and power analyses documented in the 2008 CS Soils Manual.
  - Documentation and supporting materials are available via the Countryside Survey resources and referenced CEH/NERC reports.

- Limitations and considerations for data users
  - Potential gaps between user needs and dataset scope (e.g., metadata depth for all potential users).
  - Interoperability challenges due to legacy formats or differing systems across surveys; updates and maintenance are essential.
  - Some analytes rely on specific digestion/analytical methods; results are tied to the ICP-OES/ICP-MS workflow and QA standards described.

- How to use and cite
  - Use must acknowledge Countryside Survey data owned by NERC - CEH.
  - Refer to CS technical reports for detailed methods (Soils Manual; 2007 and 2008 CS documentation) and the Countryside Survey publications for contextual interpretation.

- References and further information
  - Emmett et al. 2008 Countryside Survey: Soils Manual; CS Technical Report No. 3/07.
  - Emmett et al. 2010 Countryside Survey: Soils Report from 2007.
  - Supporting literature on ITE Land Classification and Countryside Survey methodologies.
  - Countryside Survey website and NERC CEH publications for additional protocols and data access.