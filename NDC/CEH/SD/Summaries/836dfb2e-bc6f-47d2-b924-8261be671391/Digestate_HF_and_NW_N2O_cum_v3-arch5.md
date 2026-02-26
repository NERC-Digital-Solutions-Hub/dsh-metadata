# Details of data structure to ' Digestate_HF_and_NW_N2O_cum.csv '

- Dataset scope and provenance
  - Supplement to supporting documentation for data series in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
  - Data from digestate wheat trial 2017 conducted at Henfaes Research Center (HF) and North Wyke (NW) research stations
  - Focus: N2O fluxes across treatments: C (control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP)

- Dataset structure
  - 7 columns, 40 rows
  - Columns detail: Site, Treatment, Block, Plot, Date, N2O_qa1, N2O_qa2, N2O_qa3
  - Sites: HF and NW
  - Treatments: C, D, AD, DNI, ADNI
  - Block: 1–5 (randomised block design)
  - Plot: plot identifier; note that plots 1, 19, 25, 31 and 47 were used for monthly samplings for the 150 kg N ha-1 treatment
  - Date: date of measurement
  - N2O flux processing columns:
    - N2O_qa1: all N2O flux data for each chamber/plot across the entire experimental period (used for deriving cumulative values)
    - N2O_qa2: cumulative N2O flux data with data fits where R^2 < 0.6 removed and replaced with zero flux
    - N2O_qa3: cumulative N2O flux data with data fits where R^2 < 0.6 removed and all negative flux values replaced with zero
  - Note on data adjustments: R^2 thresholds are adjustable for qa2 and qa3; negative values are set to zero in qa3

- Measurement context and plot details
  - Plot sizes and harvest areas:
    - HF: 1.2 m × 6.5 m (harvest area) for nitrogen addition rate experiments; 1.2 m × 14 m for C, D, AD, DNI, ADNI
    - NW: 2 m × 4.5 m (harvest area) for nitrogen addition rate experiments; 2 m × 9 m for C, D, AD, DNI, ADNI
  - Data represent N2O fluxes collected per plot/chamber over the experimental period; cumulative values derived from qa1 data after quality filtering

- Data quality and processing notes
  - qa1 provides the complete flux measurements
  - qa2 and qa3 apply quality filters to derive reliable cumulative flux values
  - Filters involve removing poor fits (R^2 < 0.6) and handling negative flux values as zero
  - The R^2 threshold is acknowledged as adjustable to suit analysis needs
  - These processing steps aim to produce robust cumulative N2O flux estimates for comparison across treatments and sites

- Governance and sharing considerations for Data Stewards
  - Align with the broader CINAg supporting documentation and data governance practices
  - Ensure metadata completeness and consistency with data dictionaries
  - Document all data transformations (qa1, qa2, qa3) and rationale for thresholds
  - Maintain traceability of data sources, processing steps, and decisions (e.g., when adjusting R^2 thresholds)
  - Upload and catalogue the dataset in relevant portals and data holdings
  - Be mindful of data availability and sharing limitations, and clearly note any embargoes or access constraints
  - Track updates and maintain versioning; document any changes to structure or processing rules

- Practical considerations and caveats
  - Dataset represents a specific 2017 field trial; ensure users understand the experimental design (site, block, plot, treatment)
  - Interpret cumulative N2O flux values in light of the quality filters applied (qa2/qa3)
  - Metadata should clearly reflect measurement dates, units, and processing steps to enable reuse by data consumers and other systems

- Relation to broader documentation
  - This dataset’s structure and processing are described as part of the supplementary documentation to the main supporting CinAg experiment materials (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf)