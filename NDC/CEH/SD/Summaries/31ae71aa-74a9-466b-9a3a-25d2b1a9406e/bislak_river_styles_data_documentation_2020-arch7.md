# Section 1: Overview

- Purpose and scope
  - Data used in the Bislak River Styles Report and the paper “River Styles and stream power analysis reveal the diversity of fluvial morphology in a Philippine tropical catchment.”
  - Analyses conducted March–October 2020; methods detailed in Section 2; initial analyses by P. Tolentino, J.E. Perez, E. Guardian; full River Styles review by all authors.

- Segment-stream power shapefiles and spreadsheets
  - Tools and workflow
    - TopoToolbox V2 used to extract the stream network and delineate catchment areas.
    - Upstream area threshold set at 1 km² to separate debris-flow–dominated from alluvial channels; only alluvial channels (>1 km²) included.
    - Data cleaning via non-parametric quantile regression to remove artefacts; quantile carving along the central tendency (τ = 0.5) to enforce downstream decrease in elevation.
  - Segment processing
    - Channel slope averaged over 0.2 km segment lengths (1129 segments).
    - For each segment: mean elevation, mean slope, and median catchment area extracted and exported.
    - Validation against recent Google Earth imagery.
  - Stream power calculations
    - Relationship: Ω = 0.44 χ A S (with γ = density × gravity; γ ≈ 1 × 9.807 in the text context).
    - Outputs: shapefiles for segments with stream power attributes; CSV spreadsheets listing stream power by River Style.

- River Style identification shapefiles
  - Framework and classification
    - Used Stage One of the River Styles Framework (Brierley & Fryirs 2005; Fryirs & Brierley 2018) to identify River Styles.
    - Classification criteria: confinement (channel position in the valley), channel planform, geomorphic unit assemblage, and bed material texture.
    - Naming follows Fryirs & Brierley (2018); expert judgement plays a central role due to multiple criteria.
  - Data sources and verification
    - Interpretations aided by Google Earth imagery (scales ~1:75,000 to ~1:10,000) and field verification.
    - Longitudinal profiles interpreted with catchment/regional context to determine River Styles.
  - Outputs
    - Shapefiles: polygons for landscape units (lowland, upland, hills, catchment) and isohyet lines; polylines for River Styles.

- Supporting documentation for spreadsheets
  - Extensive list of CSVs linked to river style classifications (e.g., confined, laterally unconfined, braided, deltaic; etc.).
  - Typical column conventions and data descriptors
    - Identifiers, coordinates (x, y, z), Strahler and Shreve stream orders, upstream area, distance from outlet, slope, area_km2, and various stream power metrics.
    - Multiple formats and references for segments (e.g., Bislak_200 m_segment.csv; Bislak_50 m_segment.csv; Segment_River_Styles_Figure_6a.csv) with correspondingly named fields (FID, X, Y, Z, river style names, segment identifiers, and associated metrics).
  - Examples of attributes included
    - Stream power variables across scales and river style labels, river style names, and segment identifiers.
    - Derived metrics such as gradient_m, chi indices (chi_mn045, chi_mn079), normalised channel steepness (ksn_mn045, ksn_mn079), flow accumulation (flowacc_m), distance to outlet (distoutlet), and area proxies (area_km2_<insert river style>).

- References and framework context
  - Key frameworks and tools cited: River Styles framework (Brierley & Fryirs 2005; Fryirs & Brierley 2018), TopoToolbox 2 (Schwanghart & Scherler), hydrological and geomorphological methods (Schwanghart & Scherler 2017; Tadaki et al. 2014; Rhoads 2020; Khan & Fryirs 2020).