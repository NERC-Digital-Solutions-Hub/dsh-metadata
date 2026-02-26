# Sampling Rationale and Locations

- Location and scope
  - Study area: Flow Country peatlands in the far north of Scotland (Caithness and Sutherland), affected by a wildfire in May 2019 that burned about 60 km2 of wet heath and blanket bog.
  - Spatial focus: 52 sampling sites across rivers and streams within Flow Country, including burned, pre-fire reference, and varied peatland catchments.

- Sampling design and site categories
  - Pre-fire reference sites (42 sites) from FREEDOM and LOCATE projects to understand post-fire changes.
  - Burned sites (newly established after site visits) representing degraded (n=5) and near-natural (n=5) peatland catchments post-fire.
  - Specific site groupings:
    - FREEDOM: 30 sites (undrained, drained, near-forest peatland catchments)
    - LOCATE: 12 sites along the Halladale River
    - Burned sites categorized as Degraded (B-D-1 to B-D-5) and Near-Natural (B-N-1 to B-N-5)
  - Each site documented with a unique code, stream name, and precise latitude/longitude coordinates (Table 1 references).

- Temporal coverage and schedule
  - Monthly water sampling commenced in September 2019, continuing for just over a year after the wildfire.
  - Sampling gaps: November 2019 (access limitations due to shooting) and April–June 2020 (COVID-19 restrictions).
  - Sampling and analysis cadence adjusted due to field access and vehicle constraints; campaigns occurred in weeks aligned with site access and lab processing.

- Parameters and sample processing (GIS-relevant variables)
  - In-field measurements: pH, electrical conductivity (EC), and temperature using a multiparameter probe.
  - Water chemistry analyses (laboratory): 
    - Dissolved nutrients: NH4+, soluble reactive phosphate (SRP/PO4 3-), total oxidised nitrogen (TON)
    - Dissolved organic carbon (DOC) and non-purgeable organic carbon (NPOC)
    - Dissolved metals (macro and trace elements) for New Burned and LOCATE sites
    - Absorbance measurements: UV-Vis absorbance in two laboratories, including SUVA254 calculations
  - Filtration and sample handling: field filtration (0.45 µm) for select analyses; multiple bottle types and preservations; extensive chain-of-custody and field notes.

- Field equipment and methods (GIS data capture)
  - Equipment list: GPS device with coordinates, site maps, protocol copies, sampling bottles, syringe and filters, multiparameter probe, and field forms.
  - In-field procedure: collect water near the center of flow, wash bottles, filter samples in the field where required, document conditions and environmental notes.

- Laboratory analyses and instrumentation
  - Nutrients: SEAL AQ2 Discrete Analyser for NH4+, SRP, TON; ISO-method alignment; CRMs used for QA.
  - DOC: Shimadzu TOC-L analyser (680°C combustion, NPOC method) with internal standards and CRMs.
  - Absorbance: Cary Eclipse UV-Vis (NOC) and PerkinElmer UV/Vis Lambda 365 (UKCEH) for absorbance spectra; SUVA254 calculations.
  - Dissolved metals (New Burned and LOCATE): ICP-OES (Varian 720 ES) for base cations, redox-sensitive elements, and potentially toxic elements; river water CRM used for QA.

- Data management and structure
  - Data flow: measurements from ERI (Thurso) and NOC/UKCEH laboratories; dataset includes field data and lab results with columns for sampling date, conductivity, temperature, pH, N-NH3, SRP, TON, NPOC, Abs_254, SUVA, and dissolved metals (for selected sites).
  - Data quality: limit of detection (LOD) calculated from Milli-Q blanks; results flagged as <LOD where appropriate.
  - Missing data: denoted by a dash (-).
  - Documentation: Table 4 defines column heads, units, sample IDs, and parameter descriptions; all field and analytical notes stored on the ERI server and shared with partners.

- Data workflow and accessibility
  - Field notes, sampling dates, site details, and parameter measurements compiled into spreadsheets and stored centrally.
  - Samples shipped to laboratories in insulated containers with ice packs; analyses conducted within specified timeframes to preserve integrity.
  - Data integration across multiple labs enables GIS-ready datasets for mapping water quality dynamics across burned, reference, and transitional peatland catchments.

- Practical notes and limitations
  - Access and safety considerations influenced site selection and sampling schedule.
  - Inter-lab absorbance comparisons conducted in July 2020 showed high correlation (R2 = 0.99) with minor systematic differences.
  - Some sites located in estuarine or ocean-influenced areas (e.g., L-13-R-ES) required special handling due to conductivity beyond instrument range.

- GIS-ready opportunities
  - Spatial dataset of 52 site locations with burn status, catchment category, and time-series sampling data.
  - Potential to overlay with peatland delineations, drainage/forestry history, wildfire extent, and land cover layers to analyze spatial patterns in water quality post-fire.
  - Availability of both parameter-specific layers (nutrients, DOC, metals, absorbance) and composite indicators (e.g., SUVA) for visualisation and analysis.