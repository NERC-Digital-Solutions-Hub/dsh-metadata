# Em and Ex PARAFAC loadings

- Overview
  - The document presents PARAFAC loadings for two modes: Emission (Em) and Excitation (Ex), likely stemming from a fluorescence EEM (excitation-emission matrix) decomposition used to characterize environmental samples.
  - The data appear to be a raw dump of loading values across many components, with numerous entries organized by index and loading values.

- Em PARAFAC loadings
  - The Em section lists a large set of emission-mode loadings, indexed by numbers (e.g., 282, 284, 286, 288, etc.), each followed by one or more loading values.
  - Values range from very small (on the order of 1e-5) to larger values (tens to hundreds in the given units, though most are fractions like 0.0x–0.1x, with some entries showing small decimals).
  - The formatting is highly inconsistent and includes irregular line breaks and partial entries, indicating a garbled or export-only portion of the data.
  - Some rows show multi-column patterns (e.g., sequences like “312.0299988 0.001240727 314.0599976 0.001229063”), suggesting multiple loading entries per component or multi-dimensional representations that require cleaning.

- Ex PARAFAC loadings
  - The Ex section provides excitation-mode loadings for components labeled by indices (e.g., 245, 250, 255, 260, 265, etc.), with sub-values labeled 1 through 7, indicating a 7-factor loading structure per component.
  - Example entries show:
    - 245, 1 = 0.404503245; 245, 2 = 0.300941748; 245, 3 = 0.226102695 0.186140736; 245, 4 = 0.333530111; 245, 5 = 0.333530111; 245, 6 = 0.216483065; 245, 7 = .
    - Similar patterns continue for subsequent components (250, 255, 260, 265, 270, 275, 280, 285, 290, 295, 300, 305, 310, 315, 320, 325, 330, 335, 340, 345, 350, 355, 360, 365, 370, 375, 380, 385, 390, 395, 400, etc.).
  - The values are typically in the 0.0x to ~0.4 range, with some higher values indicating stronger loadings for certain excitation bands.
  - The data appear to be more regularly structured than the Em section, but there are still signs of formatting inconsistencies and truncations (e.g., lines ending with incomplete entries or missing final component values).

- Data quality and formatting notes
  - The EmPARAFAC and ExPARAFAC sections contain numerous formatting irregularities, truncated lines, and inconsistent separators, which would require careful cleaning and validation before downstream analysis.
  - Cross-referencing Em and Ex components is necessary to ensure correct pairing of latent factors; current formatting may hinder straightforward alignment.
  - Several entries show placeholders (e.g., blanks or periods) or mixed numeric formats that suggest extraction from a larger table or export artifact.

- Environmental interpretation and use
  - PARAFAC loadings for Em and Ex are typically used to decompose fluorescence data into identifiable fluorophore components (e.g., humic-like, fulvic-like, protein-like, marine-derived, terrestrial, etc.).
  - Once cleaned, these loadings can be used to:
    - Identify and quantify underlying fluorophore groups in environmental samples.
    - Track changes in dissolved organic matter sources and processing over time (seasonal trends, contamination events, watershed influences).
    - Compare samples or datasets by comparing corresponding latent factors and their excitation/emission profiles.
  - The document’s format suggests it is part of a standardised dataset or repository intended for consistent environmental health monitoring and policy performance assessment.

- Next steps and recommendations for analysts
  - Data cleaning: rectify formatting issues, remove garbled lines, and ensure consistent indexing for Em and Ex components.
  - Alignment and validation: verify that Em and Ex loadings correspond to the same PARAFAC model components; check for any missing values and impute or annotate as needed.
  - Annotation: map latent factors to putative fluorophore types (e.g., protein-like, humic-like) based on known excitation/emission patterns and cross-reference with reference spectra.
  - Documentation and storage: store the cleaned loadings in the appropriate environmental data portal or repository with metadata, versioning, and access to underlying raw data to facilitate reuse.
  - Quality assurance: perform sensitivity analyses (e.g., reconstructing EEMs from the loadings, validating with supplemental measurements) to confirm the robustness of identified components.