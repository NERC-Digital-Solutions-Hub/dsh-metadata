# SUMMARY

- Scope and aims
  - Four-year assessment of the NERC Soil Biodiversity Thematic Programme at the Sourhope site, focusing on above-ground productivity (biomass), plant species composition, and relative abundance (diversity) in relation to management treatments.
  - Emphasis on links between soil chemistry (pH), moisture, and plant community structure, including functional group dynamics (CSR framework).

- Site design and treatments (GIS-relevant geography)
  - Rigg Foot Experimental Site at Sourhope with 5 replicate blocks along a downslope environmental gradient.
  - Each block contains 6 main plots, subdivided into 10 sub-plots; treatments allocated within plots in a randomized design.
  - Full, plot- and cell-level mapping: 0.5 m2 sampling cells (S, T, U, V) used for data collection; site-level mowing and plot-level chemical and insecticide treatments.
  - Treatments include: Control 1, Control 2 (unmanipulated), Nitrogen, Lime, Nitrogen+Lime (N&L), Insecticide (Dursban 4).

- Data collected (temporal and spatial resolution)
  - Weather data from an on-site Automatic Weather Station (1999–2002); key variables include rainfall, radiation, and temperatures.
  - Above-ground biomass: monthly harvests (May–Sept) from random 0.5 m2 cells per plot; samples dried and weighed.
  - Point analysis surveys: baseline (1998) and annual surveys (2000–2002) using 0.5 m2 cells with a 25-point grid; identification extended to bryophytes in 2002.
  - Soil measurements: soil pH (5 cm depth) and soil moisture (theta probe in botanical cells) collected regularly; 2002 moisture measurements tied to vegetation sampling.
  - Bryophyte and vascular plant inventories complemented by descriptive notes and PCA/CSR-type analyses.

- Key results (2002 season and trends)
  - Biomass productivity
    - Overall increase in biomass across most treatments from 1999 to 2002, with the strongest production in plots receiving both nitrogen and lime (N&L).
    - 2002 saw a general decline in biomass compared with 2001 across several treatments; the Control 2 plots showed notable reductions.
    - Slope-position effect: Block 1 (lower on slope) tended to show larger proportional declines than Block 5 (upper slope) in 2002.
  - Effect of fertilization and lime on soil and productivity
    - Lime raised soil pH significantly (to near 7 in upper soil in 2002); nitrogen also raised pH but less strongly.
    - Higher pH generally associated with higher biomass when considering all treatments together; the relationship varied by treatment, being more positive for some plots and nonlinear for others (notably with N+L).
    - A strong negative correlation between soil moisture and pH; improved plots tended to be drier.
  - Insecticide effect
    - Bryophyte expansion and higher diversity indicators observed in several insecticide-treated plots; the link to reduced herbivory and plant diversity is discussed but not conclusively proven.
  - Mowing effect
    - Regular mowing (≈6 cm sward) markedly reduced Agrostis capillaris and Agrostis vinealis across treatments; Festuca rubra expanded, particularly in fertilized plots.
    - Bryophyte proliferation (mosses) appeared widespread under mowing and reduced disturbance from grazing.
  - Trampling effect
    - In 2002, C2 plots (insecticide/chemical-treatment area) showed sharp productivity drops plausibly linked to trampling during heavy sampling campaigns and 13CO2 pulse activities.
  - Vegetation composition and functional groups
    - Point analyses show increased dominance of Festuca rubra and Poa pratensis in fertilized plots; unimproved plots remain dominated by Festuca ovina and Anthoxanthum odoratum.
    - Bryophytes (e.g., Rhytidiadelphus squarrosus) increased across the site, especially in unimproved plots.
    - CSR-based functional groups shifted with treatments:
      - N&L plots favored competitive-stress tolerant (C-S-R) species due to higher pH and fertility.
      - Unimproved plots favored stress-tolerant (S) species as disturbance decreases and fertility declines.
      - SR/C-S-R groups diminished in lime- and insecticide-treated plots; SR/CSR components declined with higher disturbance/fertility regimes.
  - Diversity indices
    - Shannon diversity index increased in most treatments from baseline, with the notable exception of a 15% decline in N&L plots by 2002 relative to baseline; insecticide plots showed the largest relative gains (up to ~29% in some years).
  - Species-specific patterns (2002 point analysis)
    - Two grass species linked to improved pastures (Festuca rubra, Poa pratensis) accounted for a large share of hits in fertilized plots, while unimproved plots favored Festuca ovina and Anthoxanthum odoratum.
    - Mosses and bryophytes increased in frequency, notably Rhytidiadelphus squarrosus, with bryophytes more common in unimproved plots.
  - Multivariate patterns
    - Principal Components Analysis (PCA) of 2002 point data broadly separates improved vs unimproved plots; limed plots cluster distinctly; some nitrogen-treated samples align with limed plots, while others associate with controls or insecticide plots.
    - Dissimilarities among treatments reflected shifts in dominant functional groups and species composition.

- Implications for GIS and data products
  - The study provides a rich, spatially explicit dataset suitable for GIS-based visualization and analysis:
    - Spatial layers for: treatment type per plot, slope position (block), year, biomass density per 0.5 m2 cell, and species group abundances (vascular plants and bryophytes).
    - Additional layers for soil properties (pH, moisture) and temporal trends (1998–2002).
    - Functional-group maps (CSR-based) showing shifts in community strategy by treatment.
  - Potential map-based data products
    - Time-series maps of above-ground biomass by treatment and block across years.
    - Maps of dominant species and bryophyte distribution per plot/cell, with highlights of changes from 1999–2002.
    - pH vs biomass heatmaps, including non-linear relationships by treatment.
    - Spatial gradients along the downslope axis to explore block-level variability and trampling effects.
    - Layered dashboards combining productivity, diversity (Shannon), and CSR group composition for policy or outreach audiences.
  - Data considerations for GIS work
    - Data are distributed across multiple sources (plots, cells, surveys, weather stations, appendices); centralizing and harmonizing metadata will enhance interoperability.
    - Temporal alignment is important (annual biomass, seasonal mowing, annual point analyses); ensure consistent year- and treatment-labeled geospatial rasters/feature layers.
    - Visualizations should account for slope-related spatial heterogeneity and potential trampling effects in high-activity years.

- Limitations and cautions
  - Causal links between insecticide use and diversity require further investigation; interpretations are correlational.
  - Trampling effects may confound biomass patterns in certain plots during intensive sampling periods.
  - Complex interactions exist among pH, moisture, and nutrient status; relationships vary by treatment and year.

- Takeaway for GIS specialists
  - The Sourhope site demonstrates how spatially explicit, multi-year, multi-treatment plant and soil data can be transformed into informative map-based products that reveal how management actions shape productivity, diversity, and functional composition in grassland ecosystems.