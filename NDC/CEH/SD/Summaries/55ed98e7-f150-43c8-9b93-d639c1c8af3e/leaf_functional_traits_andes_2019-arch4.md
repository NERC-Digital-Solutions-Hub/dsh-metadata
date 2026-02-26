# Leaf functional traits from three common garden sites along an elevation/temperature gradient in the Colombian Andes

## Overview
- A dataset of key leaf functional trait data collected at three elevation sites along a temperature gradient in the Colombian Andes (June–August 2019).
- Contains two CSV files: leaf_functional_traits_absolute_values.csv (absolute trait values) and leaf_functional_traits_scaled_values.csv (scaled trait values).
- Focused on eight midsuccessional Andean tropical montane forest species; some values are missing due to instrument error or quality screening.

## Data contents
- Absolute values file includes:
  - Site (1 = High elevation, 2 = Mid elevation, 3 = Low elevation)
  - Species (genus and species, e.g., C. multiflora)
  - Structural traits: LMA (g m^-2), LT (mm), LDMC (mg g^-1), LA (cm^2), LW (mm)
  - Nutrient traits: Nm (g g^-1; mass-based N), Na (g m^-2; area-based N), Pm (g g^-1; mass-based P), Pa (g m^-2; area-based P)
  - Isotopic trait: d13C (‰)
  - Water-use trait: g1 (kPa^0.5)
- Scaled values file includes:
  - Site (coded as in absolute values)
  - Climatic.origin (2 indicates cold- or warm-affiliated)
  - Species (as above)
  - Tmean (mean temperature of species’ geographic distribution)
  - Site_temp (mean annual temperature at each experimental site)
  - Stdev_of_Tmean (standard deviation of species’ thermal mean)
  - TDI (Thermal Displacement Index; scaled relative to home temperature)
  - Trait values (scaled per trait where 1 = home temperature; >1 away from home temperature; ≤1 toward home temperature)
- Scaling details:
  - TDI = (Site - Tmean) / SD(Tmean)
  - STV = trait_value / maximum_home_value (maximum value observed at home elevation/temperature)
  - WorldClim-based species thermal ranges (Fick & Hijmans, 2017) used in calculations

## Experimental design
- Three experimental sites at different altitudes with distinct mean annual temperatures:
  - High elevation: ~2516 m, MAT ~14°C
  - Mid elevation: ~1357 m, MAT ~22°C
  - Low elevation: ~736 m, MAT ~26°C
- Plot structure: each site contains six blocks per plot; one individual from each of six blocks per species, across 15 species per plot (4 sites total). Block 6 at each plot used fertilized soil.
- Plant material and timing:
  - Trees grown in a nursery at mid-elevation for two years, then planted Nov–Dec 2018 in common soils (400 kg soil per tree) with irrigation to maintain soil moisture.
  - Data in this dataset come from eight species at the experimental sites.

## Measurement methods
- Leaf structural traits:
  - LT (mm): measured with high-precision electronic calipers at three leaf areas away from the central vein; average taken.
  - LA (cm^2): leaf scans via CanoScan LiDE 300; analyzed with the LeafArea package in R (ImageJ workflow via LeafArea/LeafJ).
  - LW (mm): calculated from scanned leaf images using ImageJ LeafJ plugin.
  - LDMC (mg g^-1): leaf dry mass content calculated as dry weight / fresh weight after 48 h drying at 70°C.
  - LMA (g m^-2): dry weight / leaf area.
- Leaf nutrient traits:
  - Nm (g g^-1): mass-based leaf N via IRMS (Callisto CF IRMS).
  - Na (g m^-2): area-based N calculated from Nm / LMA.
  - Pm (g g^-1): mass-based leaf P via ICP-OES.
  - Pa (g m^-2): area-based P calculated from Pm / LMA.
- Leaf water-use traits:
  - d13C (‰): measured via IRMS ( Leaf N pathway linked).
  - g1 (kPa^0.5): derived from diurnal measurements of A and gs using the Medlyn et al. (2012) stomatal conductance model; implemented with the plantecophys R package.
  - Model details: gs* = g0 + 1.6 [1 + g1/√D] (A/ Ca) with g0 ≈ 0; g1 linked to intrinsic water-use efficiency.
- Data provenance:
  - All data collected and analyzed by the study’s lead author (AJFC) to assess thermal acclimation potential of leaf traits.

## Scaled values and data transformation
- TDI (Scaled temperature displacement): calculated as (Site temperature - species’ mean temperature) divided by the species’ temperature standard deviation.
- STV (Scaled trait values): each trait value divided by the maximum value observed at home elevation/temperature.
- Interpretation:
  - STV = 1 indicates home temperature; >1 indicates an increase away from home temperature; <1 indicates a decrease.
- Scaling references:
  - T mean and distribution data drawn from WorldClim (Fick & Hijmans, 2017).

## Data quality and limitations
- Missing values: some data points missing due to instrument error or after quality screening during post-processing.
- Scope: eight species; results reflect midsuccessional Andean tropical montane forest species and may not generalize beyond this context.
- Methods and metadata are documented, with explicit units and column descriptions (Table 1 in the dataset documentation).

## Metadata and references
- Column-level metadata provided (Table 1): names, units, and trait descriptions for both absolute and scaled datasets.
- Key references for methods and tools:
  - Medlyn et al. (2012) for the stomatal conductance model
  - Plantecophys R package (Duursma 2015)
  - LeafArea and LeafJ tools for leaf area measurement
  - WorldClim 2 climate surfaces (Fick & Hijmans 2017)
  - Standard trait measurement protocols (Pérez-Harguindeguy et al. 2016)
  - R Core Team (2022) for statistical computing

## Implications for Data Leaders: governance and use
- Strong data governance demonstrated:
  - Clear file naming, documented units, and explicit trait definitions.
  - Separate absolute and scaled data with transparent transformation rules (TDI and STV).
  - Reproducible measurement methods and software references (R packages, libraries, and versions).
- Use cases for data strategy:
  - Cross-site trait comparisons to study thermal acclimation and climate adaptation in plants.
  - Meta-analyses or integration with broader trait datasets through standardized metadata.
  - Potential for data sharing and collaboration with partners studying data provenance, quality assurance, and harmonization across networks.
- Considerations for data leaders:
  - Maintain provenance and update metadata as methods or site conditions evolve.
  - Ensure discoverability and accessibility of both absolute and scaled datasets.
  - Map data fields to common ontologies and standards to enhance interoperability across datasets and networks.
  - Monitor and document any remaining gaps or future data collection to improve coverage and generalizability.