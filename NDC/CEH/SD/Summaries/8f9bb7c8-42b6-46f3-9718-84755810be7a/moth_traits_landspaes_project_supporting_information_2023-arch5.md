# A traits database for the species of macro-moth and micro-moth recorded by the Landscape-scale species monitoring of agri-environment schemes project: 2017-2021

- Overview
  - Dataset from LandSpAES project addressing how mobile taxa respond to local and landscape agri-environment schemes (AES) gradients across arable, grassland, and upland systems in England (2017–2021).
  - Multi-year baseline survey across 54 survey squares in six National Character Areas; moths sampled with six light traps per square, twice per year, on nights meeting weather requirements; specimens euthanized and identified in the lab.
  - Focuses on macro- and micro-moth traits for broad farmland-relevant species, including many micro-moths not typically covered in farmland ecology.

- Data assets
  - Three repository items:
    - Macromoth_traits_LandSpAES_2023.csv (macro-moth traits, 410 rows, 85 KB)
    - Micromoth_traits_LandSpAES_2023.csv (micro-moth traits, 605 rows, 180 KB)
    - Moth traits_LandSpAES project_supporting information_2023.rtf (metadata, data derivation, and references; 330 KB)
  - Supporting information explains how each column was derived and how headers map to data values.

- Content and variables
  - Trait categories included in both macro- and micro-moth files:
    - Life cycle ecology and phenology; conservation status and distribution; adult and larval feeding (host plants; host plant types and parts); breeding habitats; morphological characteristics (e.g., forewing length); abundance indicators.
  - Data structure details:
    - Broader categories are subdivided into sub-categories for finer resolution (e.g., habitat, host plant types/parts).
    - Forewing lengths provided as min/max/average; multiple columns capture monthly timing data for life stages (Egg, Larva, Pupa, Adult) across 12 months (monthly presence indicators).
    - Voltinism categories (univoltine, multivoltine, variable) with north/south distinctions.
    - Host plant data include Main_HP_spp_1/2/3 and HPT_XXX/HPP_XXX mappings, plus Hab_XX_XXXX breeding habitats.
  - Documentation of data lineage and source references is embedded in the supporting information.

- Provenance and data sources
  - Core sources informing trait values and categorizations:
    - Waring & Townsend (2017)
    - Sterling & Parsons (2012)
    - Emmet & Heath (1991, 1992)
    - UKMoths (online resource)
  - Additional references in the dataset include Agassiz et al. (2013), Davis (2012), Manley (2021), and project-specific reports (LandSpAES final report; Staley et al. 2021, 2022).

- Data quality, completeness, and scope
  - Not all moth species in England are covered; emphasis on common farmland moths given the LandSpAES sampling frame and spatial design.
  - Micro-moth data draw from multiple sources to fill gaps (incomplete coverage for some taxa); documentation clarifies data derivation and column meanings.
  - Header explanations exist to aid interpretation (Table 2 for macro-moths; Table 3 for micro-moths), including examples of merged headers and multi-month columns.

- Access, documentation, and support
  - Primary contact for queries: AESspeciesmonitoring@ceh.ac.uk
  - Project website: https://www.ceh.ac.uk/our-science/projects/landspaes
  - Final project report: https://randd.defra.gov.uk/ProjectDetails?ProjectId=20012
  - The accompanying project_supporting information provides detailed metadata, column derivations, and references to ensure reproducibility.

- Usage notes and governance considerations
  - Data are stored as CSVs with a separate metadata document (RTF) to support interoperability and reproducibility.
  - Documentation outlines data derivation rules, including how many-month columns map to life stages and how host plant and habitat categories are defined.
  - Users should note the dataset’s targeted scope (common farmland species) and the reliance on multiple literature sources for micro-moth traits.
  - For updates or inquiries about data provenance, refer to the project support information and LandSpAES documentation.