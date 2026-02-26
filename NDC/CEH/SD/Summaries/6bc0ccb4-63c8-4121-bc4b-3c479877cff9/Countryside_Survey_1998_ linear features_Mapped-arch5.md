# Dataset Documentation

- Overview
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - National estimates of landscape linear feature stock for 1998 calculated using the 2007 ITE Land Classification (Bunce et al., 2007; Scott, 2007).
  - Estimates are total lengths (metres) per 1 km square per Land Class.
  - Note: some LC2007 values may be negative due to the statistical model; treat negative values as zero.

- Data Model and Schema
  - Key fields:
    - FID: Object ID; Description: Feature ID (autonumber).
    - Shape: Geometry (Spatial data).
    - LC2007: Land Class (numeric).
    - LC2007_COD: Land Class (text code).
    - CSYEAR: Year of survey.
    - LCAREA: Total area of relevant Land Class (00s hectares).
    - LF_1 to LF_7: Lengths for linear features (metres per 1 km square per land class); each feature type:
      - LF_1: Hedges
      - LF_3: Wall
      - LF_4: Line of trees/shrubs/relict hedge/fence
      - LF_5: Line of trees/shrubs/relict hedge
      - LF_6: Bank/grass strip
      - LF_7: Fence
    - LFTOTAL: Total length of linear features.
    - Shape_Length, Shape_Area: Geometry metrics.
  - Descriptions of linear feature types and their ecological/geographic interpretations:
    - _1 = Hedges
    - _3 = Wall
    - _4 = Line of trees/shrubs/relict hedge/fence
    - _5 = Line of trees/shrubs/relict hedge
    - _6 = Bank/grass strip
    - _7 = Fence
    - TOTAL = Total length of linear features
  - Reporting design:
    - Six major feature classes; no double counting of multi-element features.
    - Hedges take precedence in reporting when co-occurring with walls or fences; hedge element is included in hedge counts and not double-counted in walls/fences.

- Data Lineage and Classification
  - National estimates for 1998 derived from the 1 km survey squares using the ITE Land Classification (2007 update).
  - Reporting framework ensures consistent aggregation and avoids double counting across feature types.
  - Classification and methodology referenced in key documents:
    - ITE Land Classification 2007
    - CS Technical Report No. 4/07 (Scott, 2007) on converting 1 km survey data to national estimates
    - Foundational background documents (Bunce et al., 1996; 2007; Haines-Young et al., 2000; Barr et al., 1998)

- Usage, Acknowledgement, and Rights
  - Use must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Full acknowledgement statement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©; Database Right/Copyright NERC-CEH. All rights reserved.
  - Data licensing and rights are explicitly reserved; ensure proper attribution in copies, publications, and presentations.

- Access and Documentation
  - Countryside Survey Website provides general overview and links to methodology and relevant documents.
  - Key outputs include: Countryside Survey: UK Results from 2007 (Carey et al., 2008) and various methodological background papers.
  - Primary metadata and technical reports are publicly referenced (e.g., Scott 2007; Bunce et al. 2007; Bunce et al. 1996).

- References and Methodologies
  - Core references for dataset context and methods:
    - Scott, W.A. (2007). CS Technical Report No.4/07: Statistical methodology for national estimates from 1 km squares.
    - Bunce, R.G.H. et al. (2007). ITE Land Classification 2007 dataset.
    - Bunce, R.G.H. et al. (1996/1981) foundational land classification frameworks.
    - Haines-Young, R.H. et al. (2000). Accounting for nature: habitat assessment in the UK.
  - Additional background materials and links available via the Countryside Survey website.

- Governance Considerations for Data Stewards
  - Ensure metadata quality and consistency with the described schema (FID, Shape, LC2007, CSYEAR, LCAREA, LF_1–LF_7, LFTOTAL).
  - Maintain data provenance: link national estimates to the 1998 field survey and the 2007 ITE Land Classification methodology.
  - Enforce the reporting rule of no double counting and hedges-prioritization when co-occurring with walls/fences.
  - Manage data access, updates, and embargoes as appropriate; provide guidance on how to handle potential negative LC2007 values (treat as zero).
  - Coordinate with data creators/sharers to ensure adherence to metadata standards and to facilitate timely data sharing.
  - Ensure proper dissemination channels (portals and catalogues) and thorough documentation of transformations and quality checks.

- Practical Challenges (as noted)
  - Incomplete understanding of user needs and priorities.
  - Timely receipt of data from creators and consistent metadata completion.
  - Interoperability across multiple systems and diverse formats.
  - Handling large datasets and potential transfer/storage constraints.
  - Legacy/up-to-date database integration requiring bespoke or non-interoperable solutions.