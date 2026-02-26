# Leaf functional trait data from three common garden sites along an elevation/temperature gradient in the Colombian Andes

## Overview
- A dataset of leaf functional traits collected at three altitudinal sites in the Colombian Andes during June–August 2019.
- Aims to assess the thermal acclimation potential of leaf traits across species and elevations.
- Eight midsuccessional Andean tropical montane forest species studied; data produced by the study’s lead author (AJFC).

## Data files included
- leaf_functional_traits_absolute_values.csv: absolute trait values.
- leaf_functional_traits_scaled_values.csv: scaled trait values.
- Both files come with a Table 1 detailing column names, units, and descriptions.
- Data support materials describe measurement methods and the experimental design (planting strategy, site temperatures, and soils).

## Traits measured (absolute values)
- Structural traits: LMA (g m⁻²), LT (mm), LDMC (mg g⁻¹), LA (cm²), LW (mm).
- Nutrient traits: Nm (g g⁻¹; mass-based leaf N), Na (g m⁻²; area-based N), Pm (g g⁻¹; mass-based P), Pa (g m⁻²; area-based P).
- Isotopic and water-use traits: d13C (‰), g1 (kPa⁰.⁵; intrinsic water-use efficiency).
- Data collected from eight key species; some values missing due to instrument error or post-processing quality assessment.

## Scaling and derived metrics (scaled values)
- Thermal Displacement Index (TDI) calculated as (Site mean temperature − Species mean temperature) divided by the species’ temperature standard deviation.
- Scaled trait values (STVs): each trait value divided by the maximum value observed at the home elevation/temperature.
- Scaling context:
  - Site temperatures: high elevation ~14°C MAT (2516 m), mid elevation ~22°C MAT (1357 m), low elevation ~26°C MAT (736 m).
  - Climatic origin and species information included to indicate cold- vs warm-affiliated tendencies.
  - Positive TDI indicates transplantation to a warmer site relative to a species’ home temperature; negative TDI indicates cooler than home.

## Experimental design
- Three experimental sites at different elevations with distinct mean annual temperatures (MAT).
- Each site contains multiple plots arranged in six blocks; each plot holds six trees, totaling 90 plants per site.
- Fertilized soil is present in Block 6 (highlighted in study figures) to assess nutrient influence.
- Trees were raised from seed in a nursery for two years before planting to common soils, with irrigation to maintain soil moisture.
- Planting occurred between November and December 2018.
- Data collected from eight species across sites.

## Data collection and methods (traits and analyses)
- Leaf structural traits:
  - LT: measured with high-precision digital calipers at three leaf locations (excluding the mid-vein); average taken.
  - LA: leaf scans analyzed with LeafArea (R) package and ImageJ workflow to compute leaf area.
  - LW: calculated from scanned leaf images using LeafJ (ImageJ plugin).
  - LDMC: dry mass after oven-drying leaves at 70°C for ~48 h, ratio of dry to wet mass.
  - LMA: dry mass divided by LA.
- Leaf nutrient traits:
  - Nm and Na: ground leaf tissue analyzed by IRMS; Na derived by dividing Nm by LMA.
  - Pm and Pa: ICP-OES analysis; Pa derived by dividing Pm by LMA.
- Leaf water-use efficiency:
  - d13C values from IRMS.
  - g1 derived from diurnal measurements of A and gs using a LI-6400XT (with the Medlyn et al. 2012 stomatal conductance framework) via the plantecophys R package.
  - Measurements replicated under consistent cuvette conditions (PAR, RH, temperature, CO2).

## Data quality and limitations
- Some trait values are absent due to instrument error or post-processing quality filtering.
- Absolute and scaled datasets provide complementary views, with scaling designed to facilitate cross-site comparisons and thermal acclimation assessment.

## Relevance for environmental monitoring and policy
- Standardized, systematically collected trait data across an elevational gradient support monitoring of plant functional responses to temperature shifts.
- The combined absolute and scaled datasets enable:
  - Cross-site comparisons of trait plasticity and thermal acclimation potential.
  - Integration with environmental indicators to assess ecosystem responses to warming.
  - Stakeholder access to underlying data via standardized formats and clear documentation.

## Data access and usage notes
- Data were collected and analyzed by AJFC; methods and citations provided for reproducibility (e.g., LeafArea, LeafJ, Medlyn stomatal model, WorldClim climate surfaces).
- Data are structured for use in trait-based ecological analyses and monitoring workflows; users should consult Table 1 in the data package for column definitions and units.

## References (key tools and sources)
- Duursma (2015): Plantecophys R package for leaf gas exchange analysis.
- Fick & Hijmans (2017): WorldClim 2 climate surfaces.
- Katabuchi (2015): LeafArea R package for leaf area analysis.
- Lin et al. (2015); Medlyn et al. (2012): Stomatal conductance modeling.
- Maloof et al. (2013): LeafJ ImageJ plugin for leaf shape measurements.
- Pérez-Harguindeguy et al. (2016): Standardized trait measurement handbook.
- R Core Team (2022): R statistical computing environment.