# Headings used to record the stratigraphic data collected for each core

## Overview
- Describes the headings (columns) used to record stratigraphic data for each sediment core.
- The data form a matrix: columns are determinands (measurements) and rows are contiguous core-depth intervals.
- Blanks indicate no measurement.
- Associated files are CSVs named with water body identification (WBID) and project code; Sub_ID links to an internal database (Amphora) unique ID for each core slice.

## Data structure and content
- Core and depth metadata
  - Sub_ID (internal Amphora ID for core slice)
  - Top_Depth_cm (distance to top of sliced section from sediment/water interface)
  - Bottom_Depth_cm (distance to bottom of sliced section from sediment/water interface)
- Sediment properties
  - DW (mass of sediment after drying at 105˚C for 24 h) as % wet weight
  - LOI_550 (loss on ignition at 550˚C)
  - LOI_950 (loss on ignition at 950˚C)
  - Wetd (mass of 1 cm3 of wet sediment)
- Radiometric dating and related values
  - Pb210_Total and Pb210_Total_err
  - Pb210_Supported and Pb210_Supported_err
  - Pb210_Unsupported and Pb210_Unsupported_err
  - Cum_Unsupported_Pb210 and Cum_Unsupported_Pb210_err
  - Cs137 and Cs137_err
  - Am241 and Am241_err
  - Date_AD (calculated year date)
  - Age_yr and Age_yr_err (SAR: Constant Rate of Supply model)
  - Sedimentation Rate (SR) and SR_err
- Mercury and trace elements (XRF)
  - Hg_µg/g
  - Na_%, Mg_%, Al_%, Si_%, P_%, S_%, Cl_%, K_%, Ca_%, Ti_%
  - V_µg/g, Cr_µg/g, Mn_%, Fe_%, Co_µg/g, Ni_µg/g, Cu_µg/g, Zn_µg/g, Ga_µg/g, As_µg/g, Br_µg/g, Rb_µg/g, Sr_µg/g, Y_µg/g, Nb_µg/g, Ba_µg/g, Pb_µg/g
- Notes
  - Units are provided for each measurement (e.g., % dry mass, µg/g, cm, years).
  - Anomalies in the list (e.g., a stray comma) reflect formatting; the intended fields are the elements and concentrations above.

## Determinands and categorisation
- Core metadata and depth measurements
- Physical and compositional properties (DW, LOI, Wetd)
- Chronology and sedimentation (Pb210, Cs137, Am241, Date_AD, Age_yr, SAR, SR)
- Mercury and trace elements (Hg_µg/g; XRF-derived elemental concentrations)
- Data quality indicators (measurement errors: _err fields)

## Data management and provenance
- Data are drawn from an internal UCL Amphora database (Sub_ID) and stored in core-specific CSVs.
- Associated files include eight CSVs named with WBID and project code:
  - 34827_FELB6.csv
  - 35179_WOLT1.csv
  - 35249_BLIC2.csv
  - 35738_MARS1.csv
  - 35852_BURF1.csv
  - 35977_HGB01.csv
  - 36043_SALG1.csv
  - 36202_UPTO3.csv
- Data are intended to be stored and uploaded to appropriate portals; standardised formats facilitate sharing and reuse.

## Measurement methods and references
- Loss on ignition (LOI) methodology reference
  - Heiri, O., Lotter, A. F., & Lemcke, G. (2001). Loss on ignition as a method for estimating organic and carbonate content in sediments.
- Lead-210 dating approach
  - Appleby, P. G., & Oldfield, F. (1978). The calculation of lead-210 dates assuming a constant rate of supply of unsupported 210Pb to the sediment.
- These references underpin the LOI and CRS dating interpretations used in the dataset.

## Relevance for Analysts Monitoring the Environment
- Provides a standardized, long-term record of sediment characteristics, dating, and elemental composition across lakes.
- Enables cross-site comparisons and trend analyses to assess environmental health and policy effectiveness over time.
- Highlights data-value and accessibility challenges: need to integrate with other datasets and ensure broad access to underlying data.
- Supports reproducible monitoring by documenting data structure, measurement methods, and provenance.