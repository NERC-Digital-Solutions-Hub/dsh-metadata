# Summary

- Overview
  - Dataset of key leaf functional trait data collected at three common garden sites along an elevation/temperature gradient in the Colombian Andes, June–August 2019.
  - Two CSV files: leaf_functional_traits_absolute_values.csv (absolute trait values) and leaf_functional_traits_scaled_values.csv (scaled trait values).

- Data files and columns
  - Absolute values:
    - Site, Species
    - LT (mm), LA (cm²), LW (mm), LMA (g m⁻²), LDMC (mg g⁻¹)
    - Nm (g g⁻¹), Na (g m⁻²), Pm (g g⁻¹), Pa (g m⁻²)
    - d13C (‰), g1 (kPa⁰·⁵)
  - Scaled values:
    - Site (1 = high, 2 = mid, 3 = low)
    - Climatic.origin, Species
    - Tmean (°C): mean temperature across species’ distribution
    - Site_temp (°C): mean annual temperature at each site
    - Stdev_of_Tmean
    - TDI (scaled thermal displacement index)
    - Trait values and STVs (scaled trait values)

- Experimental design and sampling
  - Three sites at different altitudes with distinct mean annual temperatures: high ~2516 m (MAT ~14°C), mid ~1357 m (MAT ~22°C), low ~736 m (MAT ~26°C).
  - Plot structure: six blocks per plot; 6×15 plants per plot; 4×90 plants per site; fertilised soil in block 6.
  - Plants grown from seed for two years in a nursery at mid-elevation, planted Nov–Dec 2018.
  - Data include eight tree species from the study.

- Measurements and methods (absolute values)
  - Structural traits:
    - LT: measured with high-precision calipers at three leaf areas; average treated as LT.
    - LA: scanned leaves; processed with LeafArea (R) and ImageJ.
    - LW: computed from scanned images using LeafJ (ImageJ plugin).
    - LDMC: (dry weight / wet weight) after oven-drying leaves.
    - LMA: dry weight / leaf area.
  - Nutrients:
    - Nm (mass-based N) and Na (area-based N) via IRMS.
    - Pm (mass-based P) and Pa (area-based P) via ICP-OES.
  - Water-use efficiency:
    - δ13C via IRMS.
    - g1 derived from diurnal A and gs measurements using LI-6400XT; fitted with plant ecophysiology models (Medlyn et al., 2012).

- Derived/Scaled variables
  - TDI (Thermal Displacement Index): TDI = (Site temperature – mean temperature) / standard deviation of mean temperature, based on WorldClim data; positive values indicate warmer-than-home conditions.
  - Scaled trait values (STVs): each trait value divided by the maximum home-elevation value; STV = 1 at home; STV > 1 indicates increase away from home temperature, STV < 1 indicates decrease.
  - Scaled values also include climate-related context: Climatic.origin, mean temperatures, and site-specific temperature metrics.

- Data context and potential GIS applications
  - Enables spatial analyses of leaf traits and physiological parameters across an elevation/climate gradient.
  - Suitable for creating map-based visualisations of trait variation, thermal acclimation tendencies, and species-specific responses.
  - Can be integrated with climate layers (e.g., WorldClim) and geospatial site metadata to explore spatial patterns of functional traits and water-use efficiency.

- Data quality and limitations
  - Some missing values due to instrument error or post-processing quality screening.
  - Data collection focused on eight species; measurements rely on standardised protocols and specific instrumentation (calipers, scanners, IRMS, ICP-OES, LI-6400XT).

- References and tools
  - R packages and methods referenced for trait processing (LeafArea, LeafJ), stomatal modelling (Medlyn et al., 2012), and standard trait measurements (Pérez-Harguindeguy et al., 2016).
  - WorldClim 2 used for environmental context.