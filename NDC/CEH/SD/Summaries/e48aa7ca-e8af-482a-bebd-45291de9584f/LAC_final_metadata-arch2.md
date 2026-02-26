# Name of datasets

- A set of seven CSV datasets from the LAC project: LAC_Ruppert_1cm_dataset.csv, LAC_Ruppert_2cm_dataset.csv, LAC_WBP_dataset.csv, LAC_Nor1_dataset.csv, LAC_Nor3_dataset.csv, LAC_AT2_1cm_dataset.csv, LAC_AT2_2cm_dataset.csv
- Datasets come from multiple study lakes across the Arctic/Northern regions (Alaska, Norway, Greenland) with cores analyzed at high vertical resolution (1 cm or 2 cm; XRF at 200–400 μm)

## Aim and context

- Demonstrate environmental condition through a consistent, monitorable data framework suitable for long-term environmental health and policy performance scrutiny
- Provide standardised, cross-site datasets to support comparisons over time and across monitoring responsibilities

## Authorship and affiliations

- International collaboration across UK (University of Southampton, UCL, University of Nottingham, University Park), Loughborough University, and Canadian partners (Limnology Laboratory, University of Regina), with Malaysian and Malaysian-campus affiliations represented
- Datasets list authors by dataset (multiple co-authors per dataset)

## Experimental design and sampling regime

- One sediment sequence collected per study lake, using overlapping drives to assemble continuous records
- Cores collected from:
  - Ruppert (Alaska) and Woody Bottom Pond (Alaska)
  - NOR1 (Camping Pond, Norway) and NOR3 (Dalmutladdo, Norway)
  - AT2 (Greenland)
- Core methods: 1 m Livingstone corer with larger-diameter adapters; Russian corers for some Norwegian cores
- Subsampling in the UK into contiguous 1 cm and 2 cm sections; analyses performed at 1 cm or 2 cm resolution; XRF at 200 μm (Ruppert) or 400 μm (others)
- LOI, diatoms, macroscopic fossils, chironomids, cladocerans, pigments, pollen, and isotopes collected across depth sequences; isotopes measured at specialized facilities

## Analytical methods (key approaches)

- LOI (Loss on Ignition)
  - Dry weight, bulk density, organic matter (550 °C), carbonate estimation (950 °C)
  - Used to create running depth profiles and percent dry weight
- Diatoms
  - Fossil diatoms counted from contiguous 1 cm samples; minimum ~200 valves per sample; identification to species when possible
  - Counts converted to % abundance; concentrations per g dry mass
- Biogenic silica (BSi)
  - Wet alkaline digestion with ICP-MS uSi quantification
  - Use of reference SCP standards to assess variability and ensure reproducibility
- Isotopes
  - δ13C and δ15N measured via EA-IRMS; reporting of δ values and % C and N
  - Instrument accuracy checked with standard references
- XRF scanning
  - Elemental counts per second, normalized by total counts; 1 cm bin averages for cross-dataset compatibility
- Macrofossils
  - Analysis of terrestrial and aquatic macrofossils; sieved fractions (>400 μm, >200 μm); counts per 100 ml and abundance scores
- Chironomids
  - Post-macrofossil residue processing; taxon-level counts and percentages; preparation and mounting following standard protocols
- Cladocera
  - Similar processing to chironomids with Lycopodium marker for concentration calculations
- Pigments
  - HPLC analysis for chlorophylls and carotenoids; pigments quantified as nmol per g organic matter
- Pollen
  - Standard pollen preparations; counts converted to % abundance by depth
- Data processing and normalization
  - Column definitions cover running depths, sample identifiers, LOI metrics, geochemistry, diatoms, biogenic silica, isotopes, XRF, macrofossils, chironomids, cladocerans, pigments, and pollen
  - Abundances, concentrations, and fluxes prepared for integration into final stratigraphic diagrams

## Format and units

- Data stored as comma-separated values (CSV)
- SI units used for concentrations; abundance values as percentages; sample depths in cm
- Column headers and units are documented in detail (e.g., Running_top_cm, Running_bot_cm, SubID, DW_%, LOI550_%dw, WetDensity_gcc, DryDensity_gcc, etc.)
- Abbreviations and taxonomic naming follow standard references (with notes on uncertain IDs)

## Quality control and data management

- Consistent checks for detection limits and calculation errors
- Cross-checks against previous cores and reference standards
- Isotope accuracy validated with standard reference materials
- Pigment identifications verified with retention-time controls; macrofossil and cladoceran identifications cross-checked
- Documentation includes extensive quality-control notes for each data type

## Data usage and outputs

- Data structured to enable integration into final stratigraphic diagrams and cross-core comparisons
- Outputs suitable for maps, charts, and standardized environmental health indicators over time
- Datasets are prepared for upload to data portals (EIDC) with defined column headings, units, and taxonomic nomenclature

## Format of data and data management notes

- Comprehensive tables of abbreviations and units accompany the CSV files
- Data are designed for interoperability across cores and analyses, supporting value-adding data linkages and broader accessibility

## Particular challenges for Analysts Monitoring the Environment

- Increasing the value of datasets by integrating with other relevant data sources to avoid “single use”
- Facilitating access to underlying data used to generate outputs, enabling broader scrutiny and reuse

## References and methodological context

- Documented references for diatom analysis, biogenic silica, pollen and macrofossil identification, isotopes, and core-scanning techniques underpin data provenance and methodological choices