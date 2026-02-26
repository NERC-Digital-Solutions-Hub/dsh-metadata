# The Sampling Strategy for Countryside Survey (up to 2007)

- Overview
  - Documents the evolution of the ITE Land Classification and its use as the sampling frame for Countryside Survey fieldwork from 1978 to 2007.
  - Emphasises the need for a stratified, representative sample to enable national, regional, and country-specific estimates of habitats and land use.
  - Highlights how data collection, classification, and sampling have been refined over time, including adaptations for Wales and Scotland, and upland habitat assessment.

- Core concepts for GIS and data products
  - Stratified, random sampling to ensure representative coverage across environmental strata.
  - Land Classification as the backbone for sampling design and later national estimates.
  - Historical linkage between sample squares (1 km) and land-class areas to estimate habitat extents.
  - Use of the centre squares of a larger grid (and surrounding squares) to build the classified dataset.
  - Geographic specificity of country-unit estimates (England & Wales together vs. Scotland separately) and implications for policy-relevant reporting.
  - Notes on cross-year comparability: changing classifications affect consistency of national estimates; guidance on using latest vs. original classifications for consistency.

- Key historical developments and how they informed sampling
  - The Beginning (1970s)
    - Developed a stratified sampling approach to avoid bias and improve representativeness.
    - Adopted a 1 km square sampling unit for GB with random selection within environmental strata.
    - ISA (Indicator Species Analysis) used to classify vegetation/land into climate and environmental classes, forming 32 ITE Land Classes.
  - The First Survey (CS1978)
    - Classified 6039 km squares (centre squares plus surrounding squares) and surveyed 256 1 km squares (8 per class).
    - Produced national estimates by combining mean habitat area per square with the land-class area.
  - The Second Survey (CS1984)
    - Expanded to 12 squares per land class (384 total), still using the 1978 classification for national estimates.
  - The All-Squares Classification (CS1990)
    - Began to classify every 1 km square in GB rather than a subset.
    - 508 squares surveyed; linked to first Land Cover Map of GB.
    - Resulted in a revised classification method; some squares reclassified, complicating direct cross-year comparability.
  - Developments for CS1990–CS2000
    - Need to improve regional and local estimates led to extending to classify all GB squares using surrogates for climatic/geological factors.
    - Several classification attempts yielded limited exact matches (62%), but most misclassifications fell into neighboring classes with similar characteristics.
  - Countryside Survey 2000 (CS2000)
    - Addressed representation imbalances and enabled separate country estimates (England & Wales vs Scotland).
    - Sub-divided Land Classes into country-unit versions (creating more strata, ~40).
    - Added 19 extra squares to better represent new classes; 11 more to balance between England and Wales.
    - Included upland habitat module to improve accuracy for upland areas.
  - Countryside Survey 2007 (CS2007)
    - Responded to devolution needs for Wales-only reporting; Wales gained more targeted representation.
    - Sub-divided existing classes into country-unit versions (5 new Welsh sub-classes: 5w, 6w, 7w, 15w, 18w).
    - Increased total strata to 45; added 43 Welsh squares; maintained representation in England with some classes still having as few as 4 squares.
    - Wales-specific sampling and Welsh-class representation prioritized for policy-relevant reporting.
    - Maps and tables illustrate revised land-class frameworks and country-specific sampling for CS2007.

- Sampling frame specifics by survey year
  - CS1978: 8 samples per Land Class; 256 total 1 km squares; 32 Land Classes.
  - CS1984: 12 squares per Land Class; 384 total; still using 32-class framework for national estimates.
  - CS1990: All GB 1 km squares classified; 508 squares surveyed; introduction of a unified, comprehensive Land Classification; national estimates recalculated from revised framework.
  - CS2000: Separate country estimates enabled; 40 strata; class subdivisions into country units; 19 additional Welsh squares; upland module added; Island of Man replaced for country estimates; updated land-class maps for England with Wales and for Scotland.
  - CS2007: Welsh-only reporting needs drove further subdivision and sampling expansion; total strata increased to 45; 43 additional Welsh squares; 6-square minimum per Welsh class; some English classes retained 4 squares; Wales gained dedicated country-unit sub-classes (5w, 6w, 7w, 15w, 18w).

- Country-specific and upland considerations
  - England & Wales combined vs Scotland reporting (and Isle of Man adjustments) to support policy and legislative needs.
  - Upland habitat module introduced to increase precision for upland areas in England and Wales.
  - Wales-specific refinements included additional Welsh squares and country-unit land classes to support Wales-only estimates.

- Data products and reporting implications for GIS
  - Land Class maps and sample-square distributions are central inputs for GIS-based habitat and land-use mapping.
  - Shifts in land classification over time affect comparability; for cross-year analyses, the note recommends using the latest classification for national estimates or retaining the original 1990 framework for consistency.
  - The documentation provides detailed class descriptions, maps, and tables that inform how to attribute each 1 km square to a Land Class in GIS workflows and how to aggregate by country units.
  - The approach supports generation of policy-relevant statistics at multiple geographic scales (GB, England & Wales, Scotland, and Wales).

- Practical takeaways for GIS specialists
  - When building map-based data products, align data with the ITE Land Classification version appropriate to the reporting year (e.g., use CS2007 sub-classes for Wales-only reporting in 2007 onward).
  - Be mindful of country-unit definitions and the corresponding sampling frames when aggregating to England & Wales vs Scotland.
  - For longitudinal analyses, document which land-class framework is used and consider running analyses with both the latest framework and the original 1990 framework to assess consistency.
  - Consider incorporating upland module data for England and Wales to improve habitat estimates in highland areas.
  - Use the provided class descriptions and maps to ensure consistent classification of squares in GIS projects and to reproduce national estimates accurately.

- Acknowledgements and references (highlights)
  - Acknowledges statistical guidance, data synthesis, and graphical support from CEH, ITE, and DETR contributors.
  - References cover foundational development of the ITE Land Classification, landscape change studies, and Countryside Survey reports across years.

- Timeline of key changes (summary)
  - 1978: First ITE Land Classification; 32 classes; stratified 1 km square sampling; 256 total samples.
  - 1984: Land use-focused survey; same framework; increased samples per class.
  - 1990: All GB 1 km squares classified; CS1990 field survey of 508 squares; updated classification with regional implications.
  - 1998–2000: CS2000 introduces country-unit estimates; extended classification to ~40 classes; upland module added.
  - 2007: CS2007 introduces Wales-focused reporting; adds Welsh sub-classes and increases strata to 45; expanded Welsh sampling to support country-specific estimates.

- Note on data structure and definitions
  - The document provides detailed tables and figures (e.g., class maps, sample-square distributions) that underpin GIS implementations.
  - It also discusses the trade-offs in classification consistency vs. historical comparability for national-scale estimates.