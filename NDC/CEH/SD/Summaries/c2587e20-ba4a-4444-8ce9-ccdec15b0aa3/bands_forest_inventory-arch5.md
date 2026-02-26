# Amazon Fertilization Experiment (AFEX)

## Project context and study area
- Located within the Biological Dynamics of Forest Fragments Project (BDFFP) in the KM41 reserve, ~100 km from Manaus, Brazil.
- Local soils: clay-rich Ferrasols (~30% of the Amazon Basin); climate with 1900–2500 mm annual rainfall and a dry season (June–October).
- Forest structure: above-ground biomass (AGB) ~322 ± 54 Mg ha-1 (DBH ≥ 10 cm) and mean wood density ~0.67 g cm-3.
- Species richness: ~280 species per hectare ( ≥ 10 cm DBH).

## Experimental design
- Amazon Fertilization Experiment (AFEX) is a full factorial fertilization experiment with eight treatments.
- Experimental layout: 32 plots (four replicates per treatment) across four independent blocks, each block at least 200 m apart.
- Plot size and arrangement: 50 x 50 m plots, 50 m apart.
- Treatments: Control; nitrogen (N); phosphorus (P); cations; N+P; N+cations; P+cations; N+P+cations.
- Fertilization: annually applied in three doses to mitigate leaching/runoff.
  - N as urea: 125 kg ha-1 year-1
  - P as triple superphosphate: 50 kg ha-1 year-1
  - Cations (K, Ca, Mg): 50 kg ha-1 year-1 (Ca and Mg as dolomitic limestone)
- AFEX 2.0 includes updated plot delineation and maintenance.

## Data collection and measurement methods
- Forest inventories conducted annually from 2017 to 2019.
  - 2017 inventory longer due to botanical species identification; 2018 and 2019 inventories in May.
  - DBH measured at 1.3 m above ground with a diametric tape (adjusted for buttresses/deformations when necessary).
  - Training provided to staff; data entered in the field to minimize errors.
  - Recruitment (new individuals reaching DBH ≥ 10 cm) and mortality recorded.
- Dendrometric bands (growth monitoring) installed on 1,299 trees to obtain precise growth data.
  - Measurements taken as changes in circumference from a fixed window on the dendrometer bands.
  - Data collected in 2018–2020 (April, June, July, August, September, October, November in 2018; January, February, April, July, October in 2019; January in 2020).
  - Data collection avoided rainy periods to prevent instrument humidity effects.

## Data spreadsheets and data management
- Data are deposited in the EIDC system and composed of two primary spreadsheets:

1) Forest inventory data spreadsheet
- Key fields include:
  - TAG (unique tree ID), Block (B1–B4), Plot (P1–P8), PlotID (block+plot), DBH_2017, DBH_2018, DBH_2019
  - OBS (status: dead, not found, pendant, etc.), MH (height), CR (condition: alive, buttresses, vines, etc.), DN (damage type)
  - Family (botanical family), W (corrected scientific name), Date census (2017, 2018, 2019)
- Purpose: track individual trees across three inventories and annotate status and metadata.

2) Dendrometric bands data spreadsheet
- Key fields include:
  - Block, Plot, PlotID, subp_x, subp_Y, number, Family, Specie, date_band_install
  - DBH_2017, DBH_2018, DBH_2019
  - Window_Year_Month (circumference window measurements over time)
  - Date_Meas_Year_Month (dates of measurements)
  - Obs_Year_Month (observational notes, e.g., tape damage, band position change)
- Purpose: capture high-frequency growth data from dendrometric bands for selected trees.

- Both datasets note data quality practices: field training, in-field data entry, and structured metadata to support reuse.
- Accessibility: data are stored and shared via the EIDC system, facilitating discoverability within the AFEX project and related studies.

## Data governance considerations for stewardship
- Ensure consistent metadata: units (e.g., DBH in cm; circumference/diameter windows in mm), measurement protocols, plot/treatment mappings.
- Maintain data quality controls: standardize taxonomic naming (W field), clearly document OBS and CR codes, and record measurement dates with unambiguous formats.
- Support data interoperability: align fields with common ecological data standards where possible; document changes across inventories (2017–2019) and dendrometric measurements (2017–2020).
- Data updates and lifecycle: inventories occur annually; dendrometric data collected on a defined schedule; ongoing data deposition to EIDC.
- Access, licensing, and reuse: ensure clear licensing and data sharing agreements in EIDC; provide dataset-level summaries and provenance to aid discovery and replication.
- Potential data limitations to note:
  - Incomplete user needs may require additional metadata for broader reuse.
  - Some measurements are missing or marked as dead/lost; data may include NA values and status annotations.
  - Data formats originate from field records; consider converting to standardized schemas for interoperability.

## References (contextual)
- Duque A, Mulher Landare, HC, Valencia R, Cardenas D, Davies S, de Oliveira A, Perez AJ, Romero Santos H, Vicentini A. 2017. Insights into regional patterns of Amazonian forest structure and dominance from three large terra firme forest dynamics plots. Biodiversity and Conservation, 26:669-686.
- De Oliveira A, Mori SA. 1999. A central Amazonia terra firme forest. I. High tree species richness on poor soils. Biodiversity and Conservation, 8:1219-1244.
- Rankin de Merona JM, Prance JM, Hutchings RW, Silva RM, Rodrigues WA, Uehling MA. 1992. Preliminary results of a large-scale inventory of upland rainforest in the Central Amazon. Acta Amazonica 22:493-534.
- Quesada CA, Lloyd J, Anderson LO, et al. 2011. Soils of Amazonia with particular reference to the RAINFOR sites. Biogeosciences 8:1415-1440.