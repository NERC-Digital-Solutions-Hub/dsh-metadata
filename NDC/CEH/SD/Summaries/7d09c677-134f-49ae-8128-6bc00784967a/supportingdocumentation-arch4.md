# Brief Overview

- Objective and scope
  - Repeat electrical resistivity tomography (ERT) measurements conducted over four sites to capture how soil resistivity changes across the agricultural growing season.
  - Surveys planned for Spring, Summer, and Autumn 2021 to detect transitions between construction, production, and post-harvest stages.
  - Data collected to support the LANDWISE NFM (Land Management in Lowland Catchments for Integrated Flood Risk Reduction) research project.

- Field method and instrumentation
  - 19 m ERT transects with 96 electrodes spaced 20 cm apart, using a Campus Tigre system.
  - Wenner Array configuration to acquire subsurface resistivity data with adequate vertical and horizontal resolution.
  - Each transect yields approx. 660 apparent resistivity readings down to ~1 m below ground level (bgl).
  - Positioning accuracy of ~0.01 m using a Leica GNSS system to ensure repeatability.

- Sites and campaign details
  - Four survey locations: Lower Hampen Farm – Barn Ground; Lower Hampen Farm – Flat Ground; Manor Farm – Whittington Hill; Hendred Farm – Lockinge (Untraffic); Hendred Farm – East Hendred (Traffic A and B).
  - Start and end coordinates provided for each location, enabling precise localization and repeat surveys.
  - Campaign timeline: Spring (April/May 2021), Summer (June/July 2021), Autumn (September 2021, post-harvest).

- Data collection and processing workflow
  - Field data collected with ImagerPro2006; processing performed using Geotomo’s Res2DInv software.
  - Quality control includes checking electrode-ground contact and re-establishing poor contacts.
  - Noisy data points removed during processing prior to inversion to improve data reliability.

- Data format, structure, and accessibility
  - Data structured in the Res2DInv format (examples include Barnground_April.dat).
  - Each data file includes: survey name, unit spacing, array type (Wenner), number of data points, mid-point location, electrode spacing, and sequential data points (X-location, a-spacing, apparent resistivity).
  - Provides a detailed description of the data column layout and end-of-survey indicators.
  - External reference for the data format and tools: Res2DInv documentation (Geosoft/Geotomo) at https://www.geotomosoft.com/downloads.php.

- Data provenance, quality, and governance notes
  - Documentation captures survey names, locations, and precise coordinate data to support reproducibility and traceability.
  - Processing steps documented (ImagerPro2006 field collection; Res2DInv inversion with noise removal).
  - Emphasis on maintaining data quality through ground contact checks and data filtering, aligning with good data practices for spatial geophysical datasets.
  - Data intended to be integrable with broader LANDWISE and spatiotemporal analyses, potentially supporting cross-site comparisons and longitudinal studies.

- Relevance for data leadership and strategy
  - Demonstrates end-to-end data lifecycle: planning, collection, processing, and structured storage in a standardized format.
  - Highlights the importance of metadata, precise geolocation, and software toolchain for reproducibility and discoverability.
  - Provides a concrete example of aligning field data with a broader research program (LANDWISE), illustrating governance considerations for data sharing, documentation, and cross-team collaboration.