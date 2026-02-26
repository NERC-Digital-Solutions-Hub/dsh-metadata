# Amazon Fertilization Experiment (AFEX)

- Study context: Conducted within the Biological Dynamics of Forest Fragments Project (BDFFP) area, KM41 reserve, ~100 km from Manaus, Brazil. Site features Ferralsols soils, 1900–2500 mm annual rainfall with a pronounced dry season (June–October). Forest structure metrics include above-ground biomass (AGB) ~322 ± 54 Mg ha-1 (≥ 10 cm DBH) and mean wood density ~0.67 g cm-3; estimated species richness ~280 species per hectare (≥ 10 cm DBH).

- Experimental design (AFEX 1): Full factorial fertilization with eight treatments, four replicates per treatment, totaling 32 plots organized in four independent blocks spaced at least 200 m apart. Treatments comprise combinations of:
  - N (125 kg N ha-1 year-1 as urea)
  - P (50 kg P ha-1 year-1 as triple superphosphate)
  - Cations: K (50 kg K ha-1 year-1 as KCl), Ca (160 kg Ca ha-1 year-1 as dolomitic limestone), Mg (160 kg Mg ha-1 year-1 as dolomitic limestone)
  - Combinations: Control; N; P; cations; N+P; N+cations; P+cations; N+P+cations
  Plot size: 50 x 50 m, with a minimum 50 m separation between plots. Fertilization is annual and delivered in three applications by hand during systemic walks to reduce nutrient loss.

- AFEX 2.0: Plot delineation and layout documented with location maps showing all fertilized blocks and plots within the KM41 reserve.

- Data collection methods (LAI measurements): 
  - Instrument: LAI-2200 C
  - Sampling: 36 points per plot
  - Timing: 6:00–17:00 h (avoid 12:00–14:00 h to minimize solar interference)
  - Method: Above-canopy reference readings; sensor placed in a clearing; directionally oriented (west in the morning, east in the afternoon); 45° view cap to exclude operator from field of view; sensors matched prior to collection
  - Analysis: LAI computed with 5, 4, and 3 rings; data processed in FV2200 software
  - Campaigns: October 2017, March 2018, August 2018, October 2018 in Central Amazon (Manaus region)

- Data spreadsheet and structure:
  - Columns and meaning (example mapping):
    - CENSO: Plot sampling number
    - PlotID: Block and plot code
    - B_Obs: The 36 sampling points
    - Time: Time of observation (hours, minutes, seconds)
    - LAI_5_rings: LAI computed with 5 rings
    - Time: Time of corresponding LAI_5_rings measurement
    - LAI_4_rings: LAI computed with 4 rings
    - H: Time of LAI_4_rings
    - LAI_3_rings: LAI computed with 3 rings
    - Date: Campaign date (year_month)
    - coord x: Horizontal grid position in plot (0, 10, 20, 30, 40, 50 m)
    - coord y: Vertical grid position in plot (0, 10, 20, 30, 40, 50 m)
  - Data deposition: Leaf Area Index data deposited in the EIDC system (Figure 4)
  - Data granularity: 36 points per plot across four campaigns, enabling self-serve analysis of LAI patterns across treatments and time

- Key outputs and potential data products:
  - LAI measurements (LAI_5_rings, LAI_4_rings, LAI_3_rings) by plot, time, and location within plot
  - Spatially explicit LAI data (coord x, coord y) for 36 sampling points per plot
  - Time-series LAI data across four campaigns to assess fertilization effects on canopy structure

- References (contextual sources for methods and background):
  - Duque et al. 2017; Insights into regional forest structure and dominance from terra firme plots
  - De Oliveira & Mori 1999; High tree species richness on poor soils in central Amazonia
  - Quesada et al. 2011; Soils of Amazonia focusing on RAINFOR sites
  - Rankin de Merona et al. 1992; Preliminary large-scale inventory results in Central Amazonia