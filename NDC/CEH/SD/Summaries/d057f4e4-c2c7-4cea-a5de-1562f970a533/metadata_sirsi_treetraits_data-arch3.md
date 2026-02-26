# Western Ghats tree functional trait data

- Site and sampling
  - Farm near Sirsi, Karnataka, India (14.49 N, 74.75 E; 538 m a.s.l.)
  - Measurements conducted in summer 2021

- 1.1 Thermal traits
  - 1.1.1 CO2 assimilation temperature relationship (A-T curves)
    - Measurement of net photosynthesis (Anet) vs temperature using LICOR 6400 with a leaf chamber
    - In situ, sunlit terminal branches; irradiance ≈ 1000 μmol m−2 s−1; CO2 ≈ 400 μmol mol−1; RH ≈ 50–60%
    - Temperature range targeted: ~20–48 °C; typical leaf temperatures 21.4–45.0 °C (summer) and 23.2–41.1 °C (post-monsoon)
    - Data collection ensured leaf/chamber stabilization before logging; several temperature steps per leaf
    - Modelling: Anet = Aopt × exp[−((Tlieft − Topt)/Ω)²] (June et al. 2004)
    - Key parameters derived from curves: Topt, Aopt (Anet at Topt), Ω (temperature breadth), Tspan80% (80% of Aopt range), Tair_at_Topt, Tleaf_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt
  - 1.1.2 Temperature limits of Photosystem II (PSII) functioning (T50)
    - Based on heat response of dark-adapted Fv/Fm; temperature at which Fv/Fm is reduced by 50% of the upper asymptote (T50)
    - Protocol: leaf discs heated in a temperature-controlled water bath (25–50 °C) for 30 min, then Fv/Fm measured after 30 min dark recovery
    - Five discs per individual; 5–6 individuals per species
    - Curve fitting with a four-parameter logistic model (R drc package)

- 1.2 Hydraulic traits
  - 1.2.1 Water potential at 50% loss of hydraulic conductivity (P50)
    - Measured using pneumatic method with bench dehydration to generate air-discharge vs leaf water potential curves
    - Procedure: air discharged into a partial vacuum; leaf water potential measured with Scholander chamber
    - P50 defined as the leaf water potential when 50% of air has been discharged
  - 1.2. Leaf turgor loss point
    - Estimated via bench-dry/pressure-volume method
    - Relative water content vs leaf water potential plotted; Turgor Loss Point (TLP) identified at the transition from curved to linear segment

- 1.3 Leaf traits
  - Leaf area measured from scanned leaves (ImageJ)
  - Leaf mass per area (LMA) and leaf dry matter content (LDMC) following standard protocols
  - Additional trait conventions and units provided (e.g., LDMC, leaf area, etc.)

- Variables in the file (scope of data)
  - Species information: species, spcode, season, canopy position (cancat), leaf habit
  - Thermal traits: Aopt, Aopt.se, Topt, Topt.se, omega_June2004model_param, omega.se, Tspan80%, Tair_at_Topt, Tleaf_at_Topt, Tl_minus_Tair_at_Topt, VPD_at_Topt, Cond_at_Topt, Transp_at_Topt, wp, wpse
  - Temperature sensitivity and PSII metrics: P50, t50, t50.se, t5, t5.se, dw, dw.se, dwslope, dwslope.se, T50.com, T5.com, dw.com, dwslope.com, qymax.com
  - Xylem and leaf hydraulic/structural metrics: ldmc, ldmc.se
  - Leaf morphology and structure: Leafarea.se, leafperimeter, leafperimeter.se, leafwidth, leafwidth.se, lma, lma.se
  - Turgor and related metrics: Turgor_loss_point, TLP_stdev, TLP_std_error, number_of_samples_TLP

- Methods and data sources
  - Thermal traits data collected with portable IRGA (Li-6400 XT) and fluorescence measurements
  - PSII temperature limits derived from chlorophyll a fluorescence (Fv/Fm) with dark adaptation
  - Pneumatic method for hydraulic vulnerability (P50) combined with bench dehydration for leaf water potential
  - Bench-dry/pressure-volume approach for leaf turgor loss point
  - Leaf traits measured via digital imaging and standard chemical/physical protocols
  - Data interpretation and modelling rely on established literature:
    - June et al. 2004 for the A-T temperature response model
    - Sastry et al. 2018; Curtis et al. 2014 for thermal and recovery aspects
    - Ritz & Streibig 2005 for bioassay analysis in R
    - Hazir et al. 2022; Bartlett et al. 2012; Sperry et al. 1988; Bittencourt et al. 2018
    - Schneider et al. 2012; Wilson et al. 1999

- Author context and purpose
  - Presents a comprehensive suite of functional trait measurements for Western Ghats trees
  - Aims to support understanding of species’ thermal and hydraulic performance under climate stress
  - Provides data that can feed monitoring frameworks evaluating environmental health, resilience, and policy-relevant decision-making
  - Data are gathered with explicit protocols to enable comparability and potential integration into broader monitoring programs

- Relevance to monitoring frameworks
  - Covers thermal tolerance, hydraulic vulnerability, and leaf economics—key indicators of drought and heat resilience
  - Uses standardized methods enabling cross-site synthesis and policy-relevant reporting
  - Highlights data governance considerations such as metadata clarity and the need for data sharing and transparency (as reflected in the documentation and variable explanations) to support open, auditable monitoring outputs
  - Addresses common challenges: data gaps, access, silos, metadata quality, data transformation needs, and communicating complex trait results for decision-makers