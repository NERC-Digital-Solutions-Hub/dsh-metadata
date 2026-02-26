# Leaf functional traits from three common garden sites along an elevation/temperature gradient in the Colombian Andes

- Purpose: A dataset of leaf functional traits to assess thermal acclimation potential and inform environmental health monitoring and policy decisions regarding climate adaptation and ecosystem function.

- Data scope:
  - Collected June–August 2019 at three elevations in the Colombian Andes (high ~2516 m, MAT ~14°C; mid ~1357 m, MAT ~22°C; low ~736 m, MAT ~26°C).
  - Eight midsuccessional Andean tropical montane forest species grown from nursery plants transplanted to common soils.
  - Data include two CSV files: absolute values and scaled values.

- Datasets and key variables:
  - Absolute values file:
    - Structural traits: LMA (g m^-2), LT (mm), LDMC (mg g^-1), LA (cm^2), LW (mm).
    - Nutrient traits: Nm (g g^-1), Na (g m^-2), Pm (g g^-1), Pa (g m^-2).
    - Water-use trait: d13C (‰), g1 (kPa^0.5).
    - Metadata: Site (1 high, 2 mid, 3 low), Species (genus and species).
  - Scaled values file:
    - Includes: Site, Climatic.origin, Species, Tmean (mean home temperature of species distribution), Site_temp (mean annual temperature at site), Stdev_of_Tmean, TDI (thermal displacement index).
    - Trait values scaled to a home reference; TDI is used to indicate displacement distance from home temperature.
  - Units and descriptions for each column are provided in Table 1 (with notes on Site_temp, Tmean, and scaling).

- Experimental design:
  - Three sites with different altitudes and mean annual temperatures.
  - Plot layout: 6 blocks per plot; 15 plants per block; 4 plots per site; total ~90 plants per site.
  - Fertilized versus unfertilized blocks (Block 6 highlighted in blue in the figure).
  - Common soil used across sites (400 kg per tree); irrigation to maintain constant soil moisture.
  - Seedlings grown for two years in a mid-elevation nursery before transplanting in late 2018.
  - Data extracted from eight species present at the sites.

- Trait measurement methods (absolute values):
  - LT: Measured with precise calipers at three leaf areas away from the midrib; average reported.
  - LA: LeafScan images processed with LeafArea (R) and ImageJ for area calculation.
  - LW: Calculated from scanned images using LeafJ (ImageJ plugin).
  - LDMC: Wet weight measured, leaves dried at 70°C for ~48 hours, dry weight used to compute LDMC.
  - LMA: Dry weight divided by LA.

- Leaf nutrient trait methods:
  - Nm (mass-based N) and Na (area-based N): Leaf powder analyzed by IRMS; Na derived from Nm/LMA.
  - Pm (mass-based P) and Pa (area-based P): ICP-OES analysis; Pa derived from Pm/LMA.

- Leaf water-use efficiency measurements:
  - d13C from IRMS (as a carbon isotope proxy).
  - g1: Derived from diurnal measurements of A_n and g_s using a unified stomatal conductance model (Medlyn et al. 2012) fitted with the plant physiology R package (plantecophys). g1 reflects intrinsic water-use efficiency.

- Scaled values and interpretation:
  - TDI: (Site_temp − Tmean) / Stdev_of_Tmean; positive values indicate transplantation to warmer conditions than home.
  - Scaled trait values: Each trait value divided by the maximum home-elevation value; STV = 1 represents home temperature, >1 indicates an increase away from home, <1 a decrease.
  - STV computation uses WorldClim-derived species thermal ranges (Fick & Hijmans 2017).

- Data quality and gaps:
  - Some isolated values missing due to instrument error or post-processing quality control.

- Relevance for monitoring frameworks and policy:
  - Provides a structured, multi-trait data platform to monitor plant functional responses to temperature gradients, informing climate adaptation strategies and environmental health assessments.
  - Demonstrates data collection, processing, and governance considerations (metadata, data sharing, openness, transparency of methods).
  - Highlights potential barriers for monitoring programs: data gaps, access timing, organizational data silos, metadata inadequacy, data transformations, and governance requirements to ensure datasets meet standards.

- Key references and tools:
  - Measurement and analysis methods reference standard trait protocols and R packages (e.g., LeafArea, LeafJ, plantecophys, IRMS, ICP-OES, and WorldClim).
  - Foundational methodological papers: Medlyn et al. (2012), Pérez-Harguindeguy et al. (2016), Duursma (2015), Fick & Hijmans (2017), Lin et al. (2015), Maloof et al. (2013), and others.