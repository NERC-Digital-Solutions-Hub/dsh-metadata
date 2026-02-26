# NERC Soil Biodiversity Thematic Programme: Sourhope Site Annual Report 2002

- Four years into the NERC Soil Biodiversity Thematic Programme, focusing on a large field experiment at Sourhope, Scottish Borders.
- Aims: understand soil biodiversity and its links to above-ground plant communities; monitor above-ground productivity, species composition, and diversity in relation to management treatments.

## Site, Treatments and Data Collection (Methods)

- Experimental design: Rigg Foot site with 5 replicate blocks on a downslope gradient; each block has 6 main plots, subdivided into 10 sub-plots; 0.5 m x 0.5 m cells used for different research groups.
- Treatments (plot-level): Control 1 (no treatment), Control 2 (no treatment), Nitrogen, Lime, Nitrogen & Lime, Insecticide.
- Site management: yearly mowing of the whole site to ~6 cm (May–Sept); insecticide (Dursban 4) applied to Insecticide plots after mowing; spring applications of N and/or lime on designated plots.
- Data collected (since 1998–1999 onward):
  - Weather: on-site Automatic Weather Station (temperature, rainfall, radiation, soil moisture).
  - Above-ground productivity: 0.5 m2 cell samples per sub-plot, clipped plots, dried and weighed.
  - Botanical surveys: baseline quadrat (25 points) and annual 0.5 m2 point analyses with a 100-hole grid using a pin to record species hits.
  - Soil data: soil pH (5 cm depth) and soil moisture (theta probe) in survey cells.
  - Additional small surveys: vegetation cover in small plots, biomass sorted by species, and bryophyte identification (2002 expanded bryophyte identifications).
- Analysis approaches: biomass comparisons, ANOVA (split-plot), correlations between pH, moisture, and productivity; Principal Components Analysis (PCA) of point-analysis data; Shannon diversity indices.

## Key Findings

- Mowing effect
  - Dominant shift away from Agrostis spp. toward Festuca spp., especially Festuca rubra, in fertilised plots.
  - Bryophytes (mosses) expanded across the site, facilitated by a ~6 cm sward height and reduced grazing disturbance.
  - Stress-tolerant species expanded broadly; ruderal species declined with disturbance reduction and nutrient changes.

- Fertilisation effect
  - Nitrogen and/or lime consistently increased above-ground biomass; plots with both nitrogen and lime showed the strongest productivity.
  - Lime raised soil pH toward ~7.0 in the upper soil profile; nitrogen had a smaller positive effect on pH.
  - Higher soil pH and lower moisture in fertilised plots linked to altered plant functional groups; concern that productivity could decline if pH continues to rise or moisture declines.
  - Functional shift: C-S-R (competitive-stress-ruderals) species expanded most in N+L plots; stress-tolerant species favored in unfertilised plots.

- Insecticide effect
  - Shannon diversity tended to be higher in insecticide-treated plots, though evidence for a direct causal link to reduced herbivory is not definitive.
  - Possible mechanism: reduced herbivory allowed more palatable species to persist, but without definitive causal data.

- Trampling effect
  - 2002 productivity decline in C2 plots attributed to trampling during intensive sampling periods (e.g., CO2 pulse experiments), rather than a treatment effect.

## Biomass Productivity Trends (1999–2002)

- Overall biomass increased across treatments from 1999 to 2002 when compared to the 1999 baseline, but 2002 saw a general reduction relative to 2001.
- Highest productivity consistently in plots receiving both nitrogen and lime; nitrogen and/or lime alone less productive; Control 2 plots showed notable declines in multiple years.
- A slope-position effect observed: block 1 (lower slope) sometimes showed larger relative declines than block 5 (upper slope).

## Biodiversity, Community Structure and Functional Groups

- Point analysis and PCA show clear separation between improved (fertilised/limed) plots and unimproved plots; nitrogen-treated samples share characteristics with limed plots.
- Bryophytes (mosses) increased in frequency across treatments, particularly in unimproved plots, contributing to higher bryophyte hits over time.
- Dominant vascular plant shifts:
  - Festuca rubra and Festuca ovina dynamics changed over time; Agrostis capillaris and Agrostis vinealis declined significantly since 2000.
  - 2002 point analysis shows increased relative abundance of Festuca rubra in fertilised plots and a reduction of Agrostis spp.
- Functional groups (CSR framework):
  - 69–95% of plant hits were accounted for by three groups: Stress Tolerators (S), Competitive-Stress-Ruderals (CSR), and Stress-Ruderal/CSR (SR/CSR).
  - By 2002, C-S-R species dominated in nitrogen+lime plots; stress-tolerant species increased in unimproved plots; SR/CSR groups declined in lime/insecticide plots.
- Diversity (Shannon Index)
  - 2000–2002: significant treatment differences emerged; 2002 showed notable declines in Shannon diversity in N+L plots relative to baseline, while other treatments showed increases (up to 29% in insecticide plots).
- Litter and bryophyte dynamics
  - Litter hits and bryophyte hits increased in several years; bryophytes became more common across treatments, reinforcing moss-dominated understory in some plots.

## Spatial and Data Product Considerations for GIS

- Spatial framework
  - Grid-based sampling: 5 blocks x 6 plots per block x 10 sub-plots per plot; within sub-plots, 0.5 m2 sampling cells (S, T, U, V) used for vegetation surveys and biomass collection.
  - Point analysis surveys conducted annually in July/August (2000–2002) with 25-point quadrats per sub-plot; 100-hole grid with a pin used to record species at precise vegetation levels.
- Data types to model
  - Plot-level treatments and year, block location, slope position.
  - Above-ground biomass (per plot, per year; multiple mowing events per summer).
  - Species hits by taxon (vascular plants and bryophytes), including detailed bryophyte/moss lists.
  - Functional group classifications (CSR, S, SR/CSR) by year and treatment.
  - Soil chemistry and physical context: pH (5 cm depth), soil moisture (theta), and their relationship to productivity.
  - Weather context: annual/seasonal rainfall, temperature, radiation, and anomalies (noting 2002 weather data gaps and data substitution).
- Implications for GIS data products
  - Enable per-plot and per-cell visualization of species composition changes over time.
  - Map- and grid-based analyses to track functional-group shifts in response to management, including CSR dynamics.
  - Integrate environmental covariates (pH, moisture, nitrate/nutrient status, lime application) with productivity and diversity indices.
  - Support spatially explicit analyses of moss/bryophyte expansion and its relation to mowing regime and disturbance reduction.

## Conclusions and Implications

- Management regimes strongly shape plant productivity, composition, and diversity. Fertilisation and liming increase productivity but drive functional shifts toward competitive species and reduce diversity in some treatments.
- Regular mowing elevates bryophyte abundance and can homogenize the sward, potentially altering competitive interactions among vascular plants.
- Insecticide treatment may support higher plant diversity under infertile conditions, but causal links require further study.
- Spatially explicit, grid-based, multi-year data enable GIS-enabled visualization of treatment effects, species dynamics, and functional-group transitions, supporting the development of map-based data products for policy colleagues, clients, and the public.