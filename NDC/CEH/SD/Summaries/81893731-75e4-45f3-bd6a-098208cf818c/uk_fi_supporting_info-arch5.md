# Collection of water samples

- Scope and timeline
  - Fieldwork conducted in autumn (September–November) 2018–2020.
  - Collaborative sampling with the Faroese Geological Survey (Jarðfeingi) in areas with high organic soil content in the Faroe Islands.
  - Study sites spanning England, Scotland, Wales, Northern Ireland, and the Faroe Islands.
  - Targeted water bodies include pools, headwaters, streams, inlets, reservoirs, lakes, and outlets within catchments; sampling sites chosen within access constraints.

- Sampling design and site characteristics
  - Water collected from diverse water body types with peat or organic soils.
  - Multiple locations within each catchment to capture spatial variability.
  - Site metadata cover type of surface water (e.g., lake, inlet, reservoir, stream), primary land use, vegetation cover, catchment area, and country.
  - Anonymity constraints: site locations not disclosed publicly for reservoirs water companies’ access, with sites identified by coded references.

- Field and laboratory methods
  - In situ measurements: pH, conductivity, dissolved oxygen, water temperature, plus air temperature, pressure, and humidity.
  - Grab water sampling: 50 mL per site, filtered on-site through 0.45 µm syringe filters, kept cold in field and transit, stored at 4 °C in the lab.
  - Laboratory analyses (water chemistry): dissolved inorganic and organic carbon, absorbance at eight wavelengths, dissolved nutrients, cations, metals, and anions.
  - Organic matter (OM) assessment: at roughly one-third of sites, large-volume samples filtered to isolate particulate organic matter (POM); concentration and evaporation steps to obtain a small volume for analysis; DOM and POM residues analyzed for elemental content.
  - DOM/POM elemental analysis: CHNO content determined with an Elementar Vario MICRO cube (C, H, N, O; inorganic carbon removed by acid treatment); derived metrics include oxidation state (Cox), oxidative ratio (OR), DBE/C, C/N, H/C, O/C, and proportion of organic carbon (prop C).

- Datasets and their variables
  - UK_FI_Water_Chemistry (N=448)
    - Site identifiers; environmental conditions at sampling (air temperature, humidity, pressure, bank soil temperature, water temperature).
    - Water chemistry: in-field pH, electrical conductivity (EC), dissolved oxygen (DO); lab-measured DOC, SUVA254, E4/E6, DON, Prop_DON, DOP, Prop_DOP; concentrations of Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li (mg/L or µS cm−1 as appropriate).
  - UK_FI_DOM_CHNO
    - DOM elemental content at sites: N, C, H, O, Org. C (as %).
    - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C; prop C (proportion of total C that is organic).
  - UK_FI_POM_CHNO
    - POM elemental content: N, C, H, O, Org. C; derived metrics similar to DOM (Cox, OR, DBE/C, C/N, H/C, O/C; prop C).
  - UK_FI_SITES
    - Site metadata: site code, water body type category (e.g., L1/L2/L3/L4 variants for lakes, inlets, reservoirs; STREAM, POOL), land use (e.g., cutting, felled forest, grazing, moorland, plantation, renewable, restored, shooting, woodland), vegetation cover categories (acid grassland, bog, broadleaf, coniferous woodland, heather, etc.), catchment area (km², calculated via DEM and GIS), country (ENG, SCO, WAL, NIR, FAROE).
    - Anonymity and data access notes: locations withheld to protect access agreements with water companies.

- Data quality assurance and controls
  - Laboratory QA: 10% of samples analyzed in replicate; instruments calibrated at start and checked throughout runs.
  - Data QA: replicate results compared; if replicates within 95% agreement, averaged; if not, re-analysis performed.
  - CHNO-derived restrictions: derived metrics constrained by physical-property limits.

- Data governance, availability, and stewardship considerations
  - Datasets are organized to facilitate discovery and reuse by data users, with careful attention to metadata and standardized variable naming.
  - Anonymized site codes and restricted location disclosure align with access conditions from water companies, balancing data sharing with privacy/permission constraints.
  - Documentation of methods and QA steps supports reproducibility and data integrity across users.
  - Data updates and ongoing stewardship implied by structured, well-documented datasets and clear file-level metadata.

- Key challenges relevant to data stewards
  - Incomplete understanding of user needs and priorities for the datasets.
  - Timeliness of data delivery from collaborators and across multiple sites.
  - Ensuring all data creators meet metadata and format standards.
  - Interoperability across diverse systems and formats from different laboratories and field teams.
  - Handling very large datasets and legacy databases requiring bespoke solutions.
  - Managing restrictions on data sharing and updating procedures due to confidentiality and access agreements.

- Takeaways for Data Stewards
  - Maintain clear, comprehensive metadata for each dataset and variable to support discoverability and reuse.
  - Ensure robust QA protocols are documented and reproducible, with transparent handling of replicates and outliers.
  - Preserve data provenance, including sampling context, field conditions, and lab methodologies.
  - Balance openness with access constraints by documenting anonymization practices and data-sharing permissions.
  - Plan for ongoing dataset maintenance, updates, and potential schema harmonization to improve interoperability across related UK-FI data resources.