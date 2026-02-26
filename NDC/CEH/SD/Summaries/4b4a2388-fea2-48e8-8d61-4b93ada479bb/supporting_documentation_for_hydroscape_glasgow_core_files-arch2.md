# Headings used to record the stratigraphic data collected for each core

- Purpose and scope
  - Defines the standardized set of headings (determinands) used to record stratigraphic data for sediment cores.
  - Data blanks indicate no measurement; the matrix is organized as columns (determinands) and rows of contiguous core-depth intervals.
  - Files are associated with lake bodies via WBID and project codes.

- Data structure and identifiers
  - Sub_ID: Internal UCL Amphora database unique core-slice ID.
  - Top_Depth_cm, Bottom_Depth_cm: Distances to the top and bottom of each sliced core section from the sediment/water interface.
  - The dataset is designed to be stored and uploaded to appropriate portals.

- Core slice fields (examples of determinands)
  - Mass of sediment after drying at 105°C for 24 hours (DW)
  - Percentage of dry weight lost after combustion at 550°C for 2 hours (LOI 550)
  - Carbonate content (%) estimated by combustion at 950°C for 2 hours (LOI 950)

- Sediment physical properties
  - wetd: Mass (g) of 1 cm³ of wet sediment

- Radioisotopes and dating
  - Pb210_Total, Pb210_Total_err: Total Pb-210 activity and its measurement error
  - Pb210_Supported, Pb210_Supported_err: Supported Pb-210 activity and error
  - Pb210_Unsupported, Pb210_Unsupported_err: Unsupported Pb-210 activity and error
  - Cum_Unsupported_Pb210, Cum_Unsupported_Pb210_er r: Cumulative unsupported Pb-210 and its error
  - Cs137, Cs137_err: 137Cs activity and error
  - Am241, Am241_err: 241Am activity and error
  - Date_AD: Calculated year date (AD)
  - Age_yr, Age_yr_err: Sediment age (years) using Constant Rate of Supply model and its error
  - SAR: Sediment accumulation rate (g cm^-2 yr^-1)
  - SR, SR_err: Sedimentation rate (cm^-2 yr^-1) and its error

- Geochemical and elemental measurements
  - Hg µg/g: Total mercury concentration (dry sediment)
  - Elements measured by XRF (percent dry mass or µg/g as specified): Na%, Mg%, Al%, Si%, P%, S%, Cl%, K%, Ca%, Ti%, V µg/g, Cr µg/g, Mn%, Fe%, Co µg/g, Ni µg/g, Cu µg/g, Zn µg/g, Ga µg/g, As µg/g, Br µg/g, Rb µg/g, Sr µg/g, Y µg/g, Nb µg/g, Ba µg/g, Pb µg/g

- Data quality, format, and methods
  - Descriptions accompany each determinand to specify units and measurement context.
  - References for methods:
    - LOI methodology: Heiri, Lotter, & Lemcke (2001) for organic and carbonate content via loss on ignition.
    - Pb-210 dating: Appleby & Oldfield (1978) for calculating dates with constant rate of supply.

- Data storage and accessibility
  - Data are captured in the internal Amphora (UCL) database and are intended for storage and portal upload.
  - The document emphasizes enabling access to underlying data and combining datasets for enhanced value.

- Associated files
  - 25855_doug_deep.csv, 25866_bard_deep.csv, 25866_bard_litt.csv, 26001_possi_lit.csv, 26145_hogg_deep.csv, 26163_bish_deep.csv, 26167_wode_deep.csv, 26392_semp_deep.csv, 26392_semp_int.csv, 26392_semp_litt.csv, 26535_libo_deep.csv
  - Filenames encode water body identification number (WBID) and lake/project location, linking data to specific cores.

- How this supports environmental monitoring
  - Provides a consistent, exportable framework to document stratigraphic and geochemical data across cores and projects.
  - Facilitates temporal reconstruction of environmental conditions, comparison across sites, and integration with other datasets for monitoring environmental health and policy performance over time.

- Key considerations and challenges
  - Balancing depth of measurement with standardized reporting across datasets.
  - Increasing value by integrating these stratigraphic datasets with complementary environmental data and ensuring broad data accessibility.