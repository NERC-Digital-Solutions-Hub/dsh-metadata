# Long-term vegetation monitoring data for the Moor House, exclosure and grazing plots, 1953-2016

- Overview
  - Long-term dataset (1953–2016) assessing the effect of removing sheep grazing on upland vegetation at Moor House National Nature Reserve.
  - Nine plots with paired exclosure (ungrazed) and grazed areas; permanent fences mark exclosures and grazed plots are open to free-ranging grazing.
  - Data collected via pin-frame vegetation measurements and supplemented by presence/absence data for non-vascular taxa and substrates.
  - Sampling occurred at irregular intervals; the dataset spans multiple years and sites with varying methods and data densities.

- Experimental design
  - Nine plots established to compare vegetation changes under grazing vs. exclusion.
  - Each plot contains paired fenced (exclosed) and unfenced (grazed) areas.
  - Permanent fences delineate exclosures; adjacent grazed transects are accessible to sheep.

- Sampling and data collection methods
  - Pin-frame method: 1 m frame with 10 pins spaced 10 cm apart; pins extend through vegetation to the soil.
  - Vegetation height strata recorded (for vascular plants only):
    - 1: >30 cm
    - 2: 20–30 cm
    - 3: 10–20 cm
    - 4: 0–10 cm
  - Unstratified (value 99) used when height is not recorded or for bryophytes, lichens, and ground substrates (litter, bare soil, rock, etc.).
  - Two data recording approaches:
    - Absolute counts: number of pin touches per species within each height stratum (up to 13 touches).
    - Presence/absence: for some years/records, bryophytes, lichens, and non-vascular features recorded as presence/absence without height stratification.
  - Bryophytes, lichens, and physical features are typically recorded as unstratified presence/absence.
  - Fieldwork conducted by experienced botanists in pairs; consistent methods and equipment used for quality control.

- Data structure and recording units
  - Core fields include:
    - Site, Plot (enclosed vs grazed), Year (1955–2016)
    - Transect (1–10; Bog Hill uses 1A–7A and 1B–7B), Quadrat (1–10; Bog Hill 1–9, Moss Burn 1–6)
    - Frame (specific to Bog Hill; otherwise fixed)
    - Pin (position along the frame)
    - Strata (1–4; 99 for unstratified)
    - Score (number of pin touches per vascular species; 1–13; 1 for all non-vascular data)
    - Species number (VESPAN code) and species name
  - Data management notes:
    - Species names updated to align with current nomenclature
    - Data can be represented as either abundance-by-strata or presence/absence without stratification, depending on year/site

- Quality control and metadata
  - Each survey conducted by experienced botanical surveyors in pairs using standard methods.
  - Metadata and data processing notes exist to document methodological changes and site-specific variations.
  - Supporting documentation provides historical context and recording guidelines (e.g., Marrs et al. 1986; Adamson & Kahl 2001).

- Site and data coverage (nine Moor House sites)
  - Knock Fell, Trout Beck Head, Hard Hill, River Tees, Silver Band, Cottage Hill, Little Dun Fell, Moss Burn, Bog Hill
  - Data characteristics vary by site and year:
    - Some sites have long, continuous series with both exclosed and grazed treatments and consistent point counts (e.g., Knock Fell, Hard Hill, Cottage Hill).
    - Point counts per treatment range from about 400 to 1000, with stratified/unstratified configurations changing across years.
    - Bryophyte/lichen recording prevalence varies by site and year.
    - Frame usage and transect configurations not uniform across all sites (e.g., Bog Hill uses frame-specific data; other sites have fixed frames).
  - Notable data nuances:
    - Irregular sampling intervals and occasional methodological changes between survey years.
    - Some years include gaps or missing transects/frames (e.g., 1970s and 1980s for certain sites; 1976 data loss for Cottage Hill enclosed transect 1).
    - Moss Burn: 2013 enclosure opened to grazing to protect Saxifraga hirculus, resulting in no ungrazed plot after 2013.
    - Some years include special notes on strata usage (e.g., strata 99 treated as unstratified; bryophyte/lichen data recorded or not as per year).

- Data quality, limitations, and considerations for monitoring frameworks
  - Strengths:
    - Long temporal coverage across multiple sites with parallel exclosure/grazed treatments.
    - Rigorous field methods with clear stratification rules and documentation of data structure.
    - Availability of both abundance (pin touches) and presence/absence data, enabling various analytical approaches.
    - Metadata lineage and references to established recording guidelines; updating nomenclature enhances comparability.
  - Challenges to address in monitoring frameworks:
    - Data heterogeneity: varying numbers of data points, stratification schemes, and bryophyte recording practices across years and sites.
    - Access to complete metadata: historical changes in sampling design require careful harmonization for trend analysis.
    - Data gaps and losses: incomplete years and lost datasets (e.g., Cottage Hill 1976 enclosed transect 1) complicate longitudinal analyses.
    - Data governance and openness: ensuring underlying data and metadata are accessible and well-documented to facilitate reuse.
  - Practical implications:
    - When using this dataset for policy evaluation or decision-support, harmonization of stratification and treatment definitions over time is essential.
    - Analyses should account for site-specific methodological shifts and missing data to avoid biased inference about grazing impacts.

- Miscellaneous supporting materials and provenance
  - Key references:
    - Marrs, R.H., Rawes, M., Robinson, J., & Poppitt, S. (1986)
    - Adamson, J.K. & Kahl, J. (2001)
    - Environmental Change Network (ECN) database associations (VESPAN codes)
  - Supporting documents and project pages:
    - Summary of Moor House exclosure pin-frame data (detailed method notes)
    - Related project reports and web resources (e.g., www.ecn.ac.uk)

- Implications for monitoring framework authors
  - The Moor House dataset exemplifies a long-running environmental health monitoring program with:
    - Clear experimental design (exclosure vs. grazing) and defensible attribution of vegetation responses to grazing.
    - Robust, standardized field collection methods and a structured data model suitable for integration with broader environmental datasets.
    - Ongoing data governance needs, including metadata completeness, data sharing, and harmonization across years and sites.
  - Recommendations for similar frameworks:
    - Prioritize consistent metadata standards and documentation of methodological changes over time.
    - Maintain open data practices while balancing sensitive or provenance-related constraints.
    - Plan for data harmonization strategies to enable cross-site and cross-year synthesis.
    - Implement clear quality control procedures and provenance tracking to support policy-relevant analyses.