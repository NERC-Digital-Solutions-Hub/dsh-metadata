# Dissolved Si, Dissolved SO4, Dissolved Sr, Dissolved Th, Dissolved U, Dissolved Y, Dissolved Zn, Electrical conductivity, Temperature, Time, Date

- Overview
  - A comprehensive metadata record for dissolved chemical species measured in water samples, emphasizing data governance, provenance, metadata completeness, and interoperability.
  - Temporal span covered in the dataset runs from 15-Sep-92 to 04-Nov-94 with Wallingford as the primary laboratory.
  - Field and lab procedures (filtration, preservation, storage) are documented to support reproducibility and reuse.

- Scope and contents
  - Species and parameters include: Dissolved Silicon (Si), Dissolved Sulfate (SO4), Dissolved Strontium (Sr), Dissolved Thorium (Th), Dissolved Uranium (U), Dissolved Yttrium (Y), Dissolved Zinc (Zn), Electrical Conductivity, Temperature, Time, and Date.
  - Units vary by parameter (e.g., µg/l for most metals, mg/l for SO4, µS/cm for conductivity, Deg C for temperature, calendar for date).
  - Start/End dates are consistently Start = 15-Sep-92 and End = 04-Nov-94; Lab = Wallingford.
  - Filtration typically 47 mm, 0.45 µm membrane in field (with rain exclusions noted); Preservation commonly acidification to 1% HNO3; some parameters unfiltered or stored differently (e.g., unfiltered for certain measurements like temperature or pH-related analyses).

- Analytical methods and data quality
  - Methods used:
    - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES) for several metals (e.g., Al, Ca, Ba, Cu, Fe, Mg, Mn, Ni, Li, Na, K, Nd, Pb, Pr, Rb, Cs, Cd, Be).
    - Inductively Coupled Plasma Mass Spectrometry (ICP-MS) for elements such as Ce, La, Nd, Pr, Nd (repeat entries), U, etc.
    - Automated colorimetry for dissolved silica (Si) with unspecified details.
    - Specific instrument models referenced include PerkinElmer 3300 DV ICP-OES/MS and VG PlasmaQuad PQ1, among others.
  - Data quality indicators exist (Method quality control, Data qualifier), but many entries show missing values (dots), highlighting areas for stewardship review and standardization.
  - Some entries mention raw data with no laboratory data rounding or LQD (Quoted To) values, indicating provenance nuances that must be managed in data publishing.

- Data governance and sharing
  - The dataset is designed for reuse across organizations, with emphasis on:
    - Ensuring standards for accuracy, metadata completeness, and data formats.
    - Identifying data availability, embargoes, and proprietary constraints.
    - Uploading to portals and cataloguing data holdings, and maintaining update mechanisms while respecting sharing limitations.
  - Stewardship activities implied:
    - Providing guidance/tools to data creators/sharers to meet metadata and format standards.
    - Documenting work performed on datasets and ensuring traceability from field to final catalog entries.

- Particular challenges reflected
  - Incomplete understanding of user needs and priorities for this multi-element, multi-parameter dataset.
  - Timely acquisition of data from data creators and consistent metadata capture.
  - Interoperability across diverse systems and formats; handling large, multi-species datasets.
  - Legacy databases requiring bespoke handling and the need for standardized QC tagging across all species.

- Operational notes and pattern
  - The metadata is highly template-driven, enabling scalable governance, but also highlighting the need for consistent data quality tagging and full interoperability across all species.
  - Documentation covers locations (Wallingford), archival practices (storage conditions), and field/lab protocols critical for reproducibility and trustworthy data sharing.