# Background

- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study of soil biodiversity at the Sourhope field site (Macaulay Land Use Research Institute, now James Hutton Institute) in the Scottish Borders. The site was monitored for above-ground biomass production, species composition, and relative abundance to understand soil biota diversity and their functional roles in ecological processes.
- 24 projects examined soil structure, soil processes (carbon and nitrogen cycles), and roles of micro-, meso-, and macro-fauna in soil ecosystems.
- The programme produced biomass and nutrient data from controlled field plots to assess treatment effects on productivity and soil chemistry.

## Data Coverage and Experimental Context

- Location: Sourhope field site, Sourhope Farm, Scottish Borders (grid reference NT8545019630).
- Timeframe: 1999–2002 growing seasons for above-ground biomass data; 1999 for baseline mineral analyses.
- Measurements:
  - Above-ground biomass: five sampling events per growing season (1999–2002) on 50 x 50 cm cells within main plots, including species sorting, drying at 80°C, and biomass weighing.
  - Mineral nutrient analyses: vegetation N, Ca, K, Mg, P, Al measured in 1999 on July cuttings; various laboratory methods cited.
- Treatments: various soil treatments including nitrogen and lime; effects analyzed relative to control plots (C1) to identify productivity responses.

## Data Files and Structure

- Biomass values, 1999-2001: P2109_VEG_BIOMASS_1999_2002.csv
  - Key fields: MEASID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, MEAS_DATE, BIOMASS (g per 50 x 50 cm cell)
- Mineral nutrient analysis, 1999: P2109_BASELINE_99_VEG_MIN_ANAL.csv
  - Key fields: VEG_ID, CUT_DATE, TREATMENT, BLOCK, MAIN_PLOT
  - Nutrients: NITROGEN, CALCIUM, POTASSIUM, MAGNESIUM, PHOSPHORUS, ALUMINIUM (units g/100g or % where indicated)
  - Includes measurement metadata and limits of detection for each analyte
- Data formatting and organization notes reference Scott et al. (2003) for dataset definitions and plotting (see accompanying documentation)

## Variables, Units, and Methods

- Biomass file:
  - BIOMASS: dry weight of grass per 50 x 50 cm cell (grams)
  - MEAS_DATE: approximate measurement date
  - CELL_X / CELL_Y: cell grid coordinates
  - TREATMENT: soil treatment applied
- Baseline nutrient file:
  - Nutrient concentrations: N, Ca, K, Mg, P, Al (percentage or g/100g as specified)
  - Measurement methods annotated (e.g., Acid Digest with specified test method numbers)
  - Detection limits provided for each element and year-specific notes
- References to methodological details, including the exact grid and plot definitions, are described in Scott et al., 2003

## Data Quality, Provenance, and Limitations

- Quality control:
  - Numeric range checks, formatting checks, and logical integrity checks
  - Laboratory analyses subjected to internal MLURI quality procedures
- Limitations and liability:
  - Data are subject to quality assurance, but NERC cannot warrant accuracy or fitness for a particular use
  - NERC disclaims liability for any loss or damage arising from data use
- Documentation:
  - Full description and context available in Sourhope Field Data Handbook (2003) and related Supporting Information via EIDC

## Usage and Implications for Data Support

- Data can be used to compare treatment effects on biomass productivity (notably nitrogen and lime) and to assess nutrient uptake in vegetation over time.
- Normalization against a control (C1) allows cross-year comparison of treatment effects.
- Suitable for data integration, cleaning, and transformation into dashboards or self-serve analyses, with attention to metadata, units, and detection limits.
- Important to reference and cite Scott et al. (2003) and the EIDC documentation when reusing the data.