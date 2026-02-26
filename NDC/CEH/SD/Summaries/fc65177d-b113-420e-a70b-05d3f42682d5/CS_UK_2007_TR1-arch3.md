# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Overview
  - Guidance for field mapping of habitats and landscape features to support policy monitoring, reporting, and decision-making.
  - Produces time-series, country- and UK-level outputs for Broad Habitats (BH) and Priority Habitats (PH).
  - Shifts to digital data collection and integrated mapping within a 1 km square, building on prior CS surveys.

- Aims and scope
  - Identify environmental health measures to scrutinise policy and inform future decisions.
  - Enable monitoring of habitat change, distribution, and extent over time.
  - Ensure outputs support UK Biodiversity Action Plan reporting and policy evaluation.

- Data model and classification
  - Two-tier system: Broad Habitats (BH) and nested Priority Habitats (PH) where relevant.
  - BH categories cover major habitat types (e.g., woodland, grassland, aquatic, urban, etc.) with detailed subclassifications.
  - PHs are allocated within BHs when appropriate; GIS masks may constrain PH extents.
  - Emphasis on polygon-level BH/PH allocation and component-level attributes under defined themes (vegetation, forestry, physiography, agriculture/natural vegetation, etc.).

- Mapping units and rules
  - Mapping focuses on polygons (areas), lines, and points with a Minimum Mapping Unit (MMU) of 1/25 hectare (400 m²) for areas; lines/points capture narrower features.
  - Canopies and continuous belts inform BH/PH assignments; changes within the same habitat are noted as attributes unless a primary habitat change occurs.
  - Baselines: unenclosed habitats use 1990 CS data; enclosed habitats use 1998 data for baseline attributes.
  - Enclosed vs unenclosed habitat mapping considerations guide attribute detail and PH application.

- Field mapping workflow and digital tools
  - CS Surveyor: ArcMap extension enabling field data capture, change indication, and data governance within GIS.
  - Data capture focuses on recording genuine habitat change and correcting misallocations from previous surveys.
  - Data editing modules:
    - Area editing: polygon attributes, splitting/merging areas, boundary updates.
    - Line editing: management of lines (fences, walls, hedges) with events carrying length and condition.
    - Point editing: single features (trees, ponds, etc.) with multi-component attributes.
  - Operational rules:
    - Editing scales: points ≤ 1:5000, lines ≤ 1:5000; focus on habitat representation rather than pinpoint positioning.
    - Every edit must log a Reason for Change and Visit Status; defined change types include REAL change, ERROR correction, NEW BASELINE.
    - Save-workflow ensures changes are preserved.

- Change management, data quality and governance
  - Change types:
    - REAL change: genuine habitat/property change since last survey.
    - ERROR: correction of previous misallocation without real landscape change.
    - NEW BASELINE: introduction of a newly subclassed habitat or subdivision.
  - Data provenance relies on CS1998/CS2000 baselines for enclosed and unenclosed habitats, respectively.
  - Emphasis on significant ecological change thresholds and distinguishing ecological change from data errors.
  - Metadata completeness, attribute discipline, and provenance documentation are critical for data quality and governance.

- Pond mapping protocol
  - Ponds central to BH14/PH components; record all ponds in a square and designate one as the survey pond for detailed assessment.
  - Pond definition: standing water from 25 m² to 2 ha, typically water-filled for at least four months.
  - Delineation via vegetation transitions and water marks; selection process includes preselected or random pond choice with Appendix-driven randomization.
  - Distinguish ponds from ditches, streams, and dammed waters; capture area, water presence, and reasons for pond loss/creation.
  - Revisit or update CS2000 ponds as needed.

- Woody linear features (WLFs) and points/lines attributes
  - Points: include trees and small water bodies; multi-component attributes possible.
  - Woody linear features (WLFs): hedges, lines of trees, scrub; distinguish natural-shape lines vs managed hedges.
  - WLF events capture boundary features (fences, walls); attributes include length, margin widths, and topographic context.
  - Emphasis on natural shape indicators, modal diameter, canopy base height, vertical gappiness, species composition, and management signs (e.g., laying, coppicing, flailing).
  - Buffer zones around woody features may reflect landowner practices.

- Practical guidance for field staff
  - Use ArcMap with CS Surveyor for on-the-ground data capture and field edits.
  - Maintain metadata and data governance by documenting rationales and ensuring data lineage back to baselines CS1998/CS2000.
  - Vegetation: minimum two species per polygon (up to four) for descriptions; avoid over-specification in mosaics.
  - Record both primary and secondary attributes, ensure correct BH/PH allocation and qualifiers.
  - Field-specific attributes: woodland indicators, grassland indicators, bog/fen indicators; apply vegetation keys to classify habitats accurately.

- Outputs and reporting implications
  - Produces digitized, time-series maps and attribute data for BHs and PHs.
  - Supports monitoring and reporting for policy evaluation, UK biodiversity frameworks, and future decision-making.
  - Spatial accuracy is balanced with correct habitat attribution and extent to align with monitoring goals.

- End remarks, support and updates
  - CS Surveyor provides helpdesk support and methodology updates; surveyors should report issues and check latest guidance.
  - The handbook offers field-tested procedures to maintain consistency and comparability across squares and over time.

- Context and governance alignment
  - Addresses challenges common to monitoring frameworks: data gaps, data access, organizational silos, data-sharing barriers, metadata inadequacy, data format transformation, and governance needs.
  - Establishes data quality standards, clear provenance, and governance to enable transparent, repeatable habitat monitoring as part of a national policy framework.