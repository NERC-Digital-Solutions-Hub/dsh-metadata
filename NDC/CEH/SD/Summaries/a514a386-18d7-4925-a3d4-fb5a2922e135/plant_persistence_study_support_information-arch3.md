# Survival and transfer potential of Salmonella Typhimurium and Vibrio cholerae colonising plastic mulch onto basil and spinach salad leaves

- Summary of findings
  - Salmonella Typhimurium and Vibrio cholerae can persist on plastic mulch adhered to basil and spinach leaves for up to 14 days.
  - Within 24 hours, both pathogens can dissociate from the plastic surface and transfer to the surface of basil and spinach leaves.
  - Removal of adhering plastics and washing of ready-to-eat crops would not completely remove these pathogens, posing a food safety risk.
  - As plastic mulch use increases in intensive production, there is an urgent need to understand co-pollutant pathogen risks to agricultural and food systems.

- Data and datasets
  - Seven CSV files provided:
    - Cholera_Endophytic_CFUs.csv, Cholera_epiphytic_CFUs.csv, Cholera_persistence_plastic_hay_CFUs.csv
    - Salmonella_Endophytic_CFUs.csv, Salmonella_Epiphytic_CFUs.csv, Salmonella_persistence_plastic_hay_CFUs.csv
    - STyphimurium_R_squared_Gradient_K_value_D_value.csv
  - Data types include:
    - Endophytic CFUs (bacteria recovered inside leaves)
    - Epiphytic CFUs (bacteria on leaf surfaces)
    - Persistence CFUs on plastic, hay, or culture
    - CFU counts, dilutions, CFU_per_leaf, CFU_per_ml, CFU_per_mm2
    - Modeling metrics for S. Typhimurium (R^2, Gradient, K, D-value)
  - Temporal coverage: sampling on days 0, 1, 2, 3, 4, 7, 10, 14
  - Plant material: basil and spinach; surfaces: adaxial and abaxial
  - Materials tested: plastic mulch, hay, and culture (for contamination sources)
  - Data processing: CFU counts converted to concentrations per ml or per leaf; no missing data reported; replicates 1–4

- Methods overview
  - Experimental setup
    - Basil and spinach leaves placed in petri dishes with wet cotton pads
    - Materials (plastic mulch, hay, or culture) applied to leaf surfaces
    - Sampling performed on specified days; four replicates per timepoint
  - Sample processing
    - Material samples: PBS suspension, serial dilutions, plated on LB agar with chloramphenicol
    - Epiphytic samples: leaf surface wash with PBS, then plated
    - Endophytic samples: ethanol wash to remove surface bacteria, leaves crushed and resuspended, then plated
    - Incubation: 24 hours at 37°C
  - Data reporting
    - All data reported as CFU counts
    - Quality control: no data gaps; zeros indicate no colonies recovered

- Experimental design details
  - Leaves were tested with adaxial or abaxial orientation
  - Timepoints included 0, 1, 2, 3, 4, 7, 10, and 14 days
  - Negative controls included; all datasets reported; four replicates per condition

- Context and implications for monitoring frameworks
  - Demonstrates a clear link between plastisphere-associated pathogens and exposure risk to edible crops
  - Highlights data types and metadata useful for monitoring: longitudinal CFU data by plant type, surface, and material
  - Underlines data governance considerations (data sharing, metadata quality, standardization) relevant to environmental health monitoring
  - Supports integration of plastisphere pathogen transfer data into risk assessments and policy development for agricultural practices and plastic pollution management

- Publication reference
  - Data and findings published in: Woodford L, Fellows R, White HL, Ormsby MJ, Quilliam RS (2024) Salmonella Typhimurium and Vibrio cholerae can be transferred from plastic mulch to basil and spinach salad leaves. Heliyon 10:e31343. https://doi.org/10.1016/j.heliyon.2024.e31343