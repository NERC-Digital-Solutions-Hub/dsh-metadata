# Amazon Fertilization Experiment (AFEX)

- Study area context
  - Located within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil (02o 24'S, 59o52'W).
  - Soils: clay-rich Ferralsols (~30% of the Amazon Basin).
  - Climate: 1900–2500 mm annual rainfall with a pronounced dry season (June–October).
  - Forest structure context: above-ground biomass (AGB) ≈ 322 ± 54 Mg ha-1 (trees ≥10 cm DBH); mean wood density ≈ 0.67 g cm-3.
  - Species richness: ~280 species per hectare (≥10 cm DBH).

- AFEX experimental design (2.0 and original)
  - AFEX is a full factorial fertilization experiment with eight treatments and four replicates per treatment, totaling 32 plots.
  - Experimental layout: four independent blocks with plots at least 200 m apart.
  - Plot size: 50 × 50 meters, with all plots in areas of similar soil, vegetation, and topography.
  - Treatments: Control; nitrogen (N); phosphorus (P); cations; N + P; N + cations; P + cations; N + P + cations.
  - Fertilization rates (per year): 125 kg ha-1 N (as urea), 50 kg ha-1 P (as triple superphosphate), 50 kg ha-1 K (as KCl), plus 50 kg ha-1 Ca and 20 kg ha-1 Mg (as dolomitic limestone).
  - AFEX 2.0 specifics: plot delineation and annual fertilization carried out in three applications to mitigate nutrient loss; fertilizer spread manually during systematic walks within plots.

- Data collection methods
  - Forest inventories conducted annually from 2017 to 2019.
  - 2017 survey spanned June–November to complete botanical identifications; 2018 and 2019 inventories conducted in May.
  - DBH measurements taken at 1.3 m above ground with a diametric tape (adjusted when buttresses or deformities required).
  - Quality control: trained staff and field data entered directly in the computer to reduce errors.
  - Recruitment and mortality: new individuals reaching >10 cm DBH are recorded; tree mortality tracked.
  - Dendrometric bands: installed on 1,299 trees to capture precise growth via window-notched circumference measurements.
  - Measurement cadence: 2018 (Apr, Jun, Jul, Aug, Sep, Oct, Nov); 2019 (Jan, Feb, Apr, Jul, Oct); 2020 (Jan); measurements avoided during rain to protect equipment.

- Data spreadsheets and structure
  - Primary forest inventory spreadsheet
    - Key columns: TAG (individual ID), Block, Plot, PlotID, DBH_2017, DBH_2018, DBH_2019, OBS (mortality/missing/pending), MH (height), CR (condition flags), DN (damage), Family (botanical family), W (corrected scientific name), Measurement dates (2017/2018/2019).
    - Data quality notes: includes status indicators for alive, buttresses, vines, damaged, missing, etc.
  - Dendrometric bands dataset
    - Columns cover Block, Plot, subplots (subp_x, subp_Y), Family, Species, date_band_install, DBH measurements across years, Window_Year_Month, Date_Meas_Year_Month, Obs_Year_Month.
    - Contains longitudinal band measurements with dates of installation and subsequent checks.
  - Data management and access
    - Datasets deposited in the EIDC data system.
    - References to standard taxonomic updates (corrected names) and multi-year census dates.

- Data context and references
  - Contextual references on regional forest structure and biodiversity patterns (Duque et al. 2017; De Oliveira & Mori 1999; Quesada et al. 2011; Rankin de Merona et al. 1992) supporting the ecological background and methodologies.

- Practical notes for GIS use
  - The AFEX plot layout (50 × 50 m plots across four blocks) provides a structured spatial framework for map-based visualization of treatment effects, biomass, and species distributions.
  - Dendrometric bands offer high-resolution temporal data to map growth responses over time at the tree level within the plots.
  - The combination of annual inventories and precise dendrometric measurements supports GIS-based analyses of spatial patterns in growth, mortality, recruitment, and nutrient treatment effects.