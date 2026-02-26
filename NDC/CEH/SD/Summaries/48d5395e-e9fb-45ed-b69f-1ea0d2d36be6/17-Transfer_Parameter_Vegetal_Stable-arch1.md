# Supporting documentation for 17-Transfer_Parameter_Vegetal_Stable.csv

- Purpose and scope
  - Provides metadata and definitions for a CSV containing transfer parameters (Fv) for stable Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th in vegetal matrices.
  - Indicates the focus on olive oil and wine contexts for certain Fv values, with units described accordingly.
  - Aims to support analysts in understanding sample information, measurement values, uncertainties, and detection limits to enable data-driven analysis of transfer patterns.

- Data structure and key fields
  - Sample metadata
    - Sample_Code: Unique sample identifier.
    - Sample_Type: General description of the sample’s foodstuff group.
    - Location: Location where the sample was collected.
    - Sample_Description: Part of the plant analyzed (e.g., specific tissue or fraction).
    - Collection_Date: Date of sample collection (dd-mm-yyyy).
  - Transfer parameter values (Fv) and related metrics
    - Cs_Fv, Sr_Fv, K_Fv, Na_Fv, Ca_Fv, Mg_Fv, P_Fv, Pb_Fv, U_Fv, Th_Fv: Fv values representing transfer parameters for each element.
    - Unc_Cs_Fv, Unc_Sr_Fv, Unc_K_Fv, Unc_Na_Fv, Unc_Ca_Fv, Unc_Mg_Fv, Unc_P_Fv, Unc_Pb_Fv, Unc_U_Fv, Unc_Th_Fv: Uncertainty associated with the respective Fv value.
    - Detection_Limit_Cs_Fv, Detection_Limit_Sr_Fv, Detection_Limit_K_Fv, Detection_Limit_Na_Fv, Detection_Limit_Ca_Fv, Detection_Limit_Mg_Fv, Detection_Limit_P_Fv, Detection_Limit_Pb_Fv, Detection_Limit_U_Fv, Detection_Limit_Th_Fv: Detection limits for the respective Fv value.
  - Notes on multiple subfields
    - P_Fv, Pb_Fv, U_Fv, Th_Fv include numbered subfields (e.g., 1, 2, 3) indicating multiple contexts or representations within the dataset.
    - Several fields include values described as “Where blank, then below detection limit,” indicating censored data.

- Units and interpretation
  - Fv units are generally unitless or expressed as kg dry matter per L, depending on the element and the olive oil/wine matrix.
  - For Cs_Fv, Sr_Fv, Na_Fv, Ca_Fv, Mg_Fv, and others, explicit unit guidance is provided, with some fields allowing alternative units (e.g., unitless).
  - The documentation notes that some entries may be below detection limits when blank values are present.

- Data quality considerations
  - Some header descriptions contain formatting inconsistencies or truncations (e.g., misplaced notes and repeated phrases), which may require careful parsing.
  - The presence of blanks indicates values below detection limits; handling these censored values is necessary for analyses.
  - Variability in units across elements and matrices requires attention when aggregating or comparing Fv values.

- How this supports analysis
  - Enables identification of correlations between sample metadata (e.g., location, collection date, sample type) and transfer parameters.
  - Provides uncertainty and detection-limit information to inform model confidence and handling of censored data.
  - Facilitates reproducible modeling of transfer behavior across elements (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) in vegetal products, particularly olive oil and wine.