# Amazon Fertilization Experiment (AFEX)

## Overview
- Describes the AFEX factorial fertilization experiment within the Biological Dynamics of Forest Fragments Project (BDFFP) in the KM41 reserve.
- Aims to monitor how different nutrient additions affect forest structure, growth, and composition using standardized data collection and storage practices.
- Emphasizes data quality, dataset standardization, and making underlying data accessible for reuse and policy-relevant analysis.

## Study area
- Location: KM41 reserve within BDFFP, ~100 km from Manaus, Brazil (02o 24'S, 59o52'W).
- Soils: clay-rich Ferrasols covering ~30% of the Amazon Basin.
- Climate: 1900–2500 mm annual rainfall with a pronounced dry season (June–October).
- Forest characteristics (ind ≥ 10 cm DBH): above-ground biomass (AGB) ~322 ± 54 Mg ha-1; mean wood density ~0.67 g cm-3; species richness ~280 species per hectare.

## AFEX experimental design
- Start: March 2017.
- Structure: full factorial design with eight fertilization treatments and four replicates per treatment (32 plots in total).
- Plot layout: four independent blocks, each with 200 m separation between blocks; plots are 50 x 50 m and located within similar soil/vegetation/topography.
- Fertilization: annual applications divided into three events to reduce nutrient leaching and runoff.
  - Nutrients used: nitrogen (N, 125 kg ha-1 yr-1 as urea), phosphorus (P, 50 kg ha-1 yr-1 as triple superphosphate), and cations with 50 kg ha-1 yr-1 of Ca and 50 kg ha-1 yr-1 of Mg (as dolomitic limestone) plus potassium (K) at 50 kg ha-1 yr-1 as KCl.
- Treatments: Control; N; P; cations; N+P; N+cations; P+cations; N+P+cations.
- Plot delineation: AFEX 2.0 provides updated mapping of blocks and plots for consistent delineation and treatment assignment.

## Data collection methods
- Forest inventories: conducted annually from 2017 to 2019.
  - 2017 census window: June–November (longer due to botanical species identification).
  - 2018 and 2019 censuses: May.
  - DBH measured at 1.3 m above ground for trees with DBH > 10 cm; adjustments made for buttresses or deformities.
  - Quality control: trained staff; data entered in the field to minimize errors; recruitment of new individuals reaching 10 cm DBH; mortality recorded.
- High-precision growth measurements: dendrometric bands installed on 1,299 trees to capture cambial growth as circumference changes.
  - Measurements taken from a window on the bands with a digital caliper; data collection avoided during rain.
  - 2018: measurements in April, June, July, August, September, October, November.
  - 2019: measurements in January, February, April, July, October.
  - 2020: measurements in January.
- Data management: datasets structured to support longitudinal analyses of growth, mortality, recruitment, and treatment effects.

## Data spreadsheets and structure
- Inventory dataset (Figure 4):
  - Key columns: TAG (tree ID), Block, Plot, PlotID, DBH_2017, DBH_2018, DBH_2019, OBS (status: dead, lost, pendant), MH (tree height), CR (condition features: alive, buttress, vine, DAP, anchor tree, missing), DN (damage types), Family, W (corrected scientific name), Measurement dates (Measurement date.1/2/3).
  - Includes records of dead or missing trees and notes on measurement timing and precision.
- Dendrometric bands dataset (Figure 5):
  - Key columns: Block, PlotID, subp_x, subp_Y, number Family, specie, date_band_install.
  - DBH_2017, DBH_2018, DBH_2019 (diameter at breast height across inventories).
  - Window_Year_Month: circumference change measurements at multiple dates.
  - Date_Meas_Year_Month: date of each measurement event.
  - Obs_Year_Month: observations such as tape damage or band position changes.
- Data captured in the EIDC system (Electronic Information/Data Center) with detailed metadata to enable reuse and replication.
- Data standards emphasize corrected names, consistent identifiers (Block, Plot, PlotID, TAG), and explicit measurement dates.

## Data quality, access, and use
- Emphasis on standardized data collection protocols, field-trained personnel, and in-field data entry to ensure accuracy and consistency.
- Data are stored in centralized portals (EIDC system) to facilitate access and reuse by researchers, policymakers, and other stakeholders.
- Recognizes challenges and opportunities:
  - Increasing the value of datasets by integrating AFEX data with other environmental datasets (e.g., soil, climate, species traits).
  - Making underlying data accessible to external users to support transparency and broader analyses.

## References
- Duque A, Mulher Landare, HC, Valencia R, Cardenas D, Davies S, de Oliveira A, Perez AJ, Romero Santos H, Vicentini A. 2017. Insights into regional patterns of Amazonian forest structure and dominance from three large terra firme forest dynamics plots. Biodiversity and Conservation, 26:669-686.
- De Oliveira A, Mori SA. 1999. A central Amazonia terra firme forest. I. High tree species richness on poor soils. Biodiversity and Conservation, 8:1219-1244.
- Quesada, CA et al. 2011. Soils of Amazonia with particular reference to the RAINFOR sites. Biogeosciences, 8:1415-1440.
- Rankin de Merona, J.M. et al. 1992. Preliminary results of a large-scale inventory of upland rainforest in the Central Amazon. Acta Amazonica, 22:493-534.