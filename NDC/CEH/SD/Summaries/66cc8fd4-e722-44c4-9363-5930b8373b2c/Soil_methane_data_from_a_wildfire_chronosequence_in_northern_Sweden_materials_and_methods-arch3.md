# Soil methane sink capacity response to a long-term wildfire chronosequence in northern Sweden

- Purpose and scope
  - Investigates how long-term wildfire frequency (a chronosequence) influences soil methane (CH4) sink capacity in boreal forest islands of northern Sweden.
  - Combines in situ and ex situ CH4 flux measurements with isotopic analyses to quantify CH4 oxidation and the factors shaping it.
  - Aims to inform environmental health monitoring by linking wildfire history with methane flux processes and soil properties.

- Study system and design
  - 30 freshwater islands in a boreal lake archipelago (Uddjaure and Hornaven), with uniform climate but varying wildfire frequency.
  - Islands range from 0.02 to 15 ha; age and retrogression characterized via 14C dating of buried charcoal and fire scar analysis.
  - Islands are otherwise climatically and physically similar (distance to shore, precipitation ~750 mm/yr, mean July temp around +13°C, winter -14°C) to isolate wildfire effects.
  - Chronosequence representing a wildfire-frequency gradient used to assess successional effects on CH4 dynamics.

- In situ CH4 flux measurements
  - One-week field campaign using static chambers (n=5 per island).
  - Chamber setup included base ring insertion into humus and headspace sampling at 0–30 minutes after sealing.
  - CH4 analyzed by gas chromatography with a flame ionization detector; detection limit ~0.05 ppm CH4.
  - Flux calculations follow standard regression approaches; all measurements retained even when below detection limit.

- Ex situ CH4 flux measurements
  - 2006: top 25 cm soil cores collected (four cores per island; n≈40 per island size class); measured with static chambers under controlled moisture.
  - 2007: full soil profile cores (humus to bedrock) collected and measured with adjusted chamber volumes.
  - Moisture and soil moisture content determined; samples stored and analyzed similarly to in situ methods.

- Isotopic approaches and oxidation determination
  - In situ sampling for δ13CH4 and CH4/CO2 concentrations across humus depth profiles (4 depths: 15, 35, 55, 75 cm) over four days.
  - Isotopic analyses conducted via isotope ratio mass spectrometry after CO2 and water removal; precision ≤ 0.2‰.
  - Top-to-bottom δ13C-CH4 approach used to determine the isotopic fractionation factor for methanotrophy (a_ox) for each island.
  - Fraction of CH4 oxidized (F_o) estimated with a mass-balance model incorporating a_trans (assumed diffusion-related value 1.0195) to account for transport as well as biological oxidation.
  - The model yields the percentage CH4 oxidized, enabling partitioning of CH4 sink strength into oxidation processes.

- Ecosystem properties and site characteristics
  - Measured soil pH, organic carbon (%C), and total nitrogen (%N) on 2006 cores.
  - Humus depth quantified via transect measurements across island centers in 2007.
  - Additional data on vegetation mass, shrub and tree productivity, and humus mass drawn from prior studies (1997–2011).

- Data analysis and statistical approach
  - Analyses performed in R.
  - Simple regressions relate CH4 response variables to successional age and humus development.
  - Differences among successional stages (Early, Mid, Late) tested with generalized linear models; non-normal data handled with quasi-likelihood and small data shifts to ensure non-negativity.
  - CH4 measures across depths and stages analyzed with linear mixed-effects models (island as random effect) to account for non-independence of measurements within cores.
  - Diagnostic checks performed to assess residuals and heteroscedasticity.

- Ethical and governance considerations
  - Fieldwork conducted on public islands; no permits required; no human or animal subjects involved.
  - No conflicts of interest; data collection and analysis followed applicable ethical guidelines.

- Practical implications for monitoring frameworks
  - Demonstrates a comprehensive, multi-method approach suitable for environmental health monitoring: combining in situ and ex situ flux measurements, stable isotope techniques, and isotopic/flux modeling to separate oxidation from transport processes.
  - Highlights the importance of long-term or chronosequence designs to capture ecosystem response to disturbance regimes (wildfire frequency) on greenhouse gas fluxes.
  - Emphasizes data quality and transparency through standardized protocols, calibration, and robust statistical treatment, with explicit handling of detection limits and model assumptions (e.g., transport fraction, a_ox, a_trans).
  - Provides methodological blueprint for policy-relevant monitoring of soil CH4 sinks under changing disturbance regimes, informing land management and climate mitigation strategies.