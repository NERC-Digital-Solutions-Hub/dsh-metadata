# Sampling Rationale and Locations

- Purpose and scope
  - Post-fire water quality assessment in Flow Country peatlands (north Scotland) following a wildfire in May 2019.
  - Monthly sampling from 52 rivers/streams over just over a year (Sept 2019 onward); objective to understand fire effects on dissolved organic matter and other physico-chemical parameters.
  - Some sampling gaps: November 2019 missed due to shooting activities; Apr–Jun 2020 missed due to Covid-19.

- Site selection and sampling design
  - 42 of 52 sites had pre-fire data from FREEDOM and LOCATE projects, enabling reference comparisons.
  - Pre-fire reference sets:
    - FREEDOM: 30 sites representing undrained, drained, and near-forest peatland catchments.
    - LOCATE: 12 sites along the Halladale River.
  - Direct wildfire effect measurement: remaining sites chosen after field visits to burned areas, selected for accessibility, channel characteristics, flow, stratification, and peat type; included degraded (n=5) and near-natural (n=5) peatland catchments.
  - Burned-site labeling included Burnt-Degraded, Burnt-Near-Natural; additional LOCATE and FREEDOM site groups.

- Field methods and equipment
  - Manual sampling with a plastic bucket; in situ measurement of pH, electrical conductivity (EC), and temperature using a calibrated Hanna HI-991300 multiparameter probe.
  - Sample collection near the center of stream flow; field filtration (0.45 µm) for cDOM/fDOM, DOC, nutrients, and metals.
  - Containers and preservation prepared per analyte:
    - 30 mL amber glass, 50 mL/15 mL polypropylene tubes, 250 mL Nalgene bottles.
    - Tripled-rinsed containers; pre-conditioned filters and syringes to minimize artifacts.
  - Field documentation included site coordinates, sampling date/time, physico-chemical readings, and environmental notes via field forms.
  - Field equipment list included GPS, site maps, sampling bottles, syringe with 0.45 µm filter, and a multiparameter probe.

- Sample handling, storage, and transport
  - Samples kept cold in a cold box during fieldwork; refrigerated and light-protected upon return to ERI.
  - Storage specifics:
    - Nutrients and total organic carbon analyzed within 2–5 days.
    - Macro and trace metals preserved by acidification (0.5 mL HNO3 per 10 mL sample) and stored at 4°C in the dark.
  - Transport to NOC and UKCEH for absorbance analysis in insulated boxes with ice packs.

- Laboratory analyses and instrumentation
  - Nutrients (NH4+, SRP, TON): SEAL AQ2 Discrete Analyser; ISO-standard methods; calibration with certified standards and CRMs; colourimetric detection with specific reagent schemes.
  - Dissolved organic carbon (DOC): Shimadzu TOC-L with non-purgeable organic carbon method; 680°C catalytic oxidation; internal standards and TOC CRM used for QA.
  - Absorbance (UV-Vis) for cDOM; SUVA254 calculated to indicate DOC aromaticity; UKCEH and NOC performed inter-lab comparisons.
  - Dissolved metals (only New Burned and LOCATE sites): ICP-OES (Varian 720 ES); multi-element analysis including base cations, redox-sensitive elements, and potential toxicants (Cu, Zn, Ni); samples diluted to fit calibration range; river water CRM employed for QA.
  - Equipment and facilities included: SEAL AQ2, Shimadzu TOC-L, ICP-OES, UV-Vis spectrophotometers, Milli-Q water system, calibrated balances, and appropriate glassware.

- Data structure, formatting, and quality control
  - Dataset integrates three laboratory data streams (ERI, NOC, UKCEH) with site and sampling metadata.
  - Data columns include: sample ID, sampling date, conductivity, temperature, pH, NH4+, SRP, TON, NPOC, absorbance (Abs_254 and SUVA for NOC/UKCEH), and dissolved metals (for New Burnt and LOCATE).
  - Limits of detection (LOD) calculated per analysis per instrument using blank data; results reported as <LOD when applicable.
  - Missing information denoted with a dash (-) in dataset.
  - Absorbance inter-laboratory comparison conducted in July 2020 showed strong agreement (R^2 = 0.99) despite small absolute differences.

- Data management and outputs
  - Field data and analytical results organized into spreadsheets and stored on the ERI server; shared with project partners.
  - Summary Table (Table 4) defines code, description, and units for each data column (e.g., Cond µS/cm, Temp °C, pH, N-NH3 µg N/L, SRP µg P/L, TON µg N/L, NPOC mg/L, Abs_254, SUVA, and Dissolved metals with respective units).

- Timeline and scheduling notes
  - Initial plan split sampling across two weeks per month for New Burnt/LOCATE and FREEDOM sites; adjustments made due to site access, vehicle availability, and later Covid restrictions.
  - Sampling concentrated at end of weeks to facilitate timely shipping and subsequent analyses.

- Notable quality controls and comparability steps
  - Use of certified reference materials and standard solutions in nutrient analyses.
  - Regular instrument calibration and CRM checks for metals and TOC.
  - Inter-lab cross-check for absorbance measurements to ensure cross-lab data compatibility.

- References and context
  - FIRE Blanket project and related references used for study context.
  - Method references include Gaffney et al. (2017) for ICP-OES metals analysis and Sugimura & Suzuki (1988) for TOC methodology.