# Predatory Bird Monitoring Scheme Egg Contaminant Data Description

- Purpose and context
  - Describes a dataset of contaminants in homogenised seabird eggs, generated for long-term temporal trend analyses as part of the Predatory Bird Monitoring Scheme (PBMS).
  - Reports and trend analyses are available on the PBMS website.

- Data structure and key fields
  - Ref, Description: Descriptive labels for variables (examples include contaminant names and site descriptors).
  - Year (4-digit): Year the egg was collected.
  - Site: Location of colony where eggs were collected. Sites include Ailsa Craig, Bass Rock, St Kilda, Grassholm, Scar Rocks, Hermness, Little Skellig (Ireland), and Great Saltee (Ireland), with exact coordinates provided for some sites.
  - Shell_index: Shell thickness indicator (based on Ratcliffe 1970). Units noted as mg/mm (typographical nuances present in the source).
  - Contaminants measured (in homogenised egg contents):
    - HEOD: Concentration of a complex hexachloro-naphthalene compound; Units: µg/g wet weight; Not analysed (NA) in some records; ND = None Detected.
    - DDE: Concentration of a DDT metabolite; Units: µg/g wet weight; NA/ND statuses as above.
    - Hg: Total mercury; Units: µg/g dry weight.
    - PCB: Total concentration of PCBs (excluding a subset of identified peaks) calculated relative to a reference Aroclor standard; Units: µg/g wet weight; NA/ND statuses as above.
    - PCB congener set (e.g., PCB008, PCB018, PCB029, PCB028, PCB031, PCB052, PCB077, PCB101, PCB105, PCB114, PCB118, PCB123, PCB126, PCB128, PCB138, PCB149, PCB153, PCB156, PCB157, PCB167, PCB169, PCB170, PCB180, PCB189, PCB194, PCB199, PCB201, PCB205, PCB206, PCB141, PCB163, PCB171, PCB183, PCB187, PCB194, PCB199, PCB201, PCB205, PCB206, etc.): Individual congener concentrations in homogenised egg contents; Units: µg/g wet weight; Not analysed (NA); None Detected (ND) statuses appear where applicable.
  - Additional Information: Text notes that the data support long-term temporal trend analyses and can be downloaded from the PBMS results page.

- Geographic and temporal coverage
  - Temporal span: Years collected (4-digit year field present for each record).
  - Spatial: Eight named sites (Ailsa Craig, Bass Rock, St Kilda, Grassholm, Scar Rocks, Hermness, Little Skellig, Great Saltee) with explicit coordinates for several sites.

- Data quality, metadata, and accessibility
  - Some records show ND (None Detected) or NA (Not Analysed) for certain contaminants or congeners.
  - Metadata completeness can vary; some fields require interpretation or external data sources (e.g., site coordinates, unit definitions).
  - Data governance considerations implicit: public sharing of underlying data is part of the PBMS framework, with associated data provenance requirements.

- Usage implications for monitoring frameworks
  - Enables long-term trend analyses of contaminant exposure in seabirds, supporting environmental health assessments.
  - The breadth of contaminants (shell quality indicators, organochlorines like DDE/HEOD, mercury, and a wide PCB congeners set) supports comprehensive risk profiling.
  - Public availability of reports facilitates transparency and stakeholder engagement, while highlighting the need for robust metadata and data governance to ensure reuse.