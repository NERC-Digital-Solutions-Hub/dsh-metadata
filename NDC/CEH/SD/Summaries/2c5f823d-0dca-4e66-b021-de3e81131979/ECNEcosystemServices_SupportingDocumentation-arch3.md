# Ecosystem services variables from the UK Environmental Change Network (ECN)

## Overview
- The Environmental Change Network (ECN) is the UK's long-term environmental monitoring and research programme, regularly measuring air, soil, water, and a range of fauna and flora at multiple sites to track changes in the natural environment.
- This dataset uses the Millennium Ecosystem Assessment (MA) as a conceptual framework to define and identify ecosystem services and associated variables.
- Purpose: to create a standardised set of ecosystem services variables across ECN sites, enabling consistent environmental and biodiversity measurements over time and space, and supporting policy scrutiny and decision-making.

## Site selection and boundaries
- Eleven ECN sites were selected for the ecosystem services dataset.
- Boundary definitions focused on land ownership, land management, and ECN site boundaries, with boundary choices reflecting human decision-making scales.
- Land ownership and management boundaries largely defined the data acquisition boundaries; at four sites, ECN site boundaries aligned with ownership/management boundaries. Some sites extended to whole farms or complete water basins.
- Boundaries incorporated both biogeophysical features and social discontinuities to align with MA’s combined social-ecological land-category framework.

## Data sources and variable selection
- Three data sources were used for ecosystem services variables at each site:
  - (i) Data collected according to the ECN standard protocol.
  - (ii) Data supplied by site managers from other sources.
  - (iii) Expert knowledge of site managers.
- A site managers’ workshop in January 2010 standardised variable definitions and ensured comparability.
- To minimise temporal variability, data for a single year (commonly 2009) or site-year averages were used; where appropriate, values were area-scaled to the site area.

## Variables and categorisation
- A comprehensive set of ecosystem services variables was defined (Table 2 in the source), covering provisioning, regulating, cultural, and supporting services.
- Categories include (examples):
  - Food: meat (tonnes per hectare), vegetables, fruit, eggs, cereals, and a count of provisioning categories per site.
  - Fibre: wool (sheep/goats), wood production (tonnes per hectare).
  - Fuel: timber for fuel, hydropower output.
  - Genetic resources: animal and plant species held as genetic stocks; national collections of species.
  - Biochemicals and pharmaceuticals: species/breeds used in industry/research; materials produced.
  - Ornamental resources.
  - Regulating services: air quality (N and S deposition per hectare), climate regulation (net CO2e flux), water regulation (dam/reservoir presence; flood events), erosion, and disease/pest regulation.
  - Pollination and biological control (e.g., pest presence).
  - Natural and other hazards (fire frequency; noise regulation).
  - Cultural and educational values: cultural diversity, spiritual/religious values, educational use and visitors, and ecotourism.
  - Aesthetic values: abundance of butterflies, carabid beetles, moths, bats, birds; landscape features and CVS types.
  - Social relations and heritage: local population proximity, access, and heritage features.
  - Ecotourism and education-related visitation.
- In total, the dataset includes a large suite of variables (over 60–70 in several categories), with each variable assigned a numeric or categorical unit (e.g., tonnes ha−1, yes/no, number per site).

## Format, structure, and metadata
- Original data were stored in Excel 2007 format and subsequently converted to comma-separated values (CSV) for long-term storage.
- Dataset structure uses site-specific columns (e.g., ALI for Alice Holt, CAI for Cairngorm, etc.) and a column for Service Type/Indicator Variable.
- Variable identifiers and numbers (Variable_ID, Variable_Number) link each site’s data to its definition (table-driven metadata).
- The data format and headings facilitate cross-site comparisons and time-series analyses when data are available for multiple years.

## Data availability and references
- Data sources and protocols are linked to the ECN:
  - ECN protocols ( site-specific data collection standards ).
  - ECN website: http://www.ecn.ac.uk/
- The dataset is publicly documented and has been analysed in peer-reviewed work:
  - Dick et al. (2011): A comparison of ecosystem services delivered by 11 long-term monitoring sites in the UK Environmental Change Network. Environmetrics 22(5), 639-648.
- Theoretical and reference framework:
  - Millennium Ecosystem Assessment (2005): Ecosystems and human well-being.
- The dataset is cited as: Ecosystem services variables from the UK Environmental Change Network (ECN), with a DOI for the data publication (Dick et al. 2011; NERC Environmental Information Data Centre).