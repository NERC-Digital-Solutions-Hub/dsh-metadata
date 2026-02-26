# Countryside Survey vegetation, recorded from plots in 2019

## Overview
- Countryside Survey (UK) is a long-running, Rolling program (since 2019) by UK Centre for Ecology & Hydrology Countryside Survey (UKCEH-CS) designed to monitor natural resources of the UK countryside.
- Integrates soil and vegetation metrics across multiple scales to detect spatial and temporal changes; aims to provide robust national and sub-national indicators.
- Observational data underpin policy-relevant insights and long-term trend analysis; time series extend back to 1978.

## Design and sampling
- Rolling survey: 500 x 1km squares sampled over a five-year cycle; 100 squares surveyed annually.
- Sample selection: stratified by Land Classification of Great Britain; includes 256 squares from 1978 carried forward to maximize time-series continuity; additional squares added based on early survey years (1990) to strengthen longitudinal coverage.
- Exclusion criteria: any square with >75% urban land or >90% sea excluded.
- Field approach: five sampling points per square (soil and vegetation data collected) to enable ecosystem-wide analyses.

## Data collection and quality assurance
- Data collection: conducted by trained botanical survey teams following standardized protocols (Smart et al., 2019); intensive pre-survey training ensures consistency.
- Quality control: on-site supervision during surveys; 10% of plots re-surveyed by a QA assessor; QA procedures have been consistent since 1990 to provide reliable measures of detection and location validation.
- Validation: independent validation of plot locations and alignment to the JNCC broad habitat classifications.

## Data products and metadata
- Data products (two CSV files) for 2019 vegetation surveys:
  - UKCEHCS_VEGETATION_PLOTS_2019.csv: plot-level information including YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, BAP Broad Habitat, BAP Priority Habitat, country, county, environmental zone, land classification (LC07) and related descriptors.
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2019.csv: species list per plot with species identifiers, names (BRC_NAMES), nest level data, and survey-year context.
- Data fields reference established nomenclature (e.g., Stace, 1997) and standardized habitat classifications (BAP, LC07, JNCC broad habitat).
- Documentation and data dictionaries are aligned with UK-SCAPE Field Survey Handbook (Smart et al., 2019) and related methodological sources.
- Files are designed to support integration with soil data and broader vegetation metrics for cross-scalar analyses.

## Data governance, access, and stewardship
- Governance: part of UKCEH-CS, with provenance linked to CEH/NERC data centers and the Countryside Survey program; designed for ongoing update and long-term accessibility.
- Metadata and provenance: explicit sample design, methods, QA history, and linkage to habitat classifications enable traceability and reproducibility.
- Access and publication: data and supporting materials are published through CEH and NERC Environmental Information Data Centre channels, with references and links provided in the accompanying documentation.
- Update and maintenance: rolling five-year cycle ensures continuous data addition; data stewardship responsibilities include updating datasets, maintaining compatibility with core classifications, and documenting methodological changes (e.g., field handbook 2019).

## Documentation, standards, and interoperability
- Methodology and field procedures: Smart et al., 2019 field handbook; standardized training, plot-level and species-level data collection.
- Classifications: Land Classification of Great Britain (ITE/Land Classification 2007), Biodiversity Broad Habitats, Priority Habitats (JNCC/Maddock 2008), and other habitat descriptors to enable comparability and interoperability.
- References provide depth on sampling design, statistical treatment, and policy-relevant interpretation (e.g., Scott 2008; Norton et al. 2012; Bunce et al. 2007).

## Practical considerations and challenges for Data Stewards
- Ensuring a complete picture of user needs and timely data delivery across multiple years and sites.
- Managing data from diverse systems and formats, including large, multi-file datasets with complex metadata.
- Maintaining data quality across an ongoing rolling program and ensuring consistent alignment with evolving classifications and standards.
- Handling updates and updates propagation to portals/catalogues while preserving time-series integrity and clear provenance.

## References and further reading
- Smart et al., 2019. UK-SCAPE Field Survey Field Handbook 2019 Vegetation Plots (UKCEH).
- Bunce et al., 2007; Bunce et al., 1996; Jackson, 2000; Maddock, 2008; Scott, 2008; Norton et al., 2012; Stace, 1997.
- Countryside Survey project documentation and related CEH/NERC data center resources.