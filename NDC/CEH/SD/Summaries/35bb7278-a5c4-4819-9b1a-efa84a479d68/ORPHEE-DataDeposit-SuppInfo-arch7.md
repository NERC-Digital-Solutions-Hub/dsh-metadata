# Experimental design

## GIS-relevant overview
- Large tree diversity experiment (ORPHEE) in SW France, planted 2008, designed as eight blocks over 12 ha.
- Spatial structure: blocks nested within a site, each containing 32 treatment plots randomly distributed.
- Data collected at the tree level with spatially explicit identifiers to enable map-based analyses (Tree.ID, Block, Plot).

## Study design and sampling
- Experimental design: randomized blocked design with eight blocks; 32 treatments per block.
- Species palette: Quercus robur, Quercus pyrenaica, Quercus ilex, Betula pendula, Pinus pinaster.
- Treatments: fully factorial gradient of tree species richness from monocultures to five-species mixtures; an additional replication of the five-species mixture yields 32 plots per block.
- Irrigation: since 2015, half of the blocks receive irrigation (3 mm/night per plot) May–October; the other half rely on rainfall.
- Focus for survey: plots selected along a tree-diversity gradient focusing on Q. robur (excluding pine plots); eight treatments centered on Qr-containing mixtures (monoculture; three 2-species mixes with Qr; three 3-species mixes with Qr; 4-species mix including birch).
- Apparent oak dominance (apparency) varies with birch proportion, enabling comparisons of plots with identical richness but different oak apparency.
- Plot and tree sampling: blocks 1–6 surveyed (3 irrigated, 3 non-irrigated); four Quercus robur trees per plot were randomly chosen for damage assessment.

## Data collected and measurements
- Biotic responses recorded:
  - Insect herbivory on primary shoots.
  - Powdery mildew infection on lammas shoots.
- Sampling approach:
  - On each tree, eight shoots (varying height/angle) were assessed.
  - For primary shoots: five leaves per shoot; mines counted; data aggregated to shoot or tree level.
  - Damage classified for chewers (leaf miners grouped with chewers) into seven leaf-level classes (0–6).
  - For lammas shoots: five leaves per shoot; mildew classified into five classes (0–4); averages computed at shoot and tree levels.
- Covariates measured:
  - Primary and lammas shoot lengths (mm).
  - Tree height (cm).
- Additional focus: for 2018, height (H.2018) recorded for Q. robur trees.

## Data quality control
- Data entry: manual into Excel, followed by visual checks for outliers and missing values.
- Missing-value checks: df_status() function from the R package funModeling used to identify NAs.

## Data structure and units (key fields)
- Tree.ID: unique tree identifier; coordinates encoded in a bespoke x/y scale tied to the ORPHEE plan.
- Date.Surveyed: survey date (day/month/year).
- Block: experimental block (nested within site).
- Plot: plot within block (nested within block/site).
- Irrigation: Y/N irrigation treatment at block level.
- Plot.Composition: coding for species planted in the plot (e.g., Qr, Qp, Qi, Bp).
- Resource.Dilution: proportion of non-Qr species in the plot (0–0.75).
- Richness: number of tree species planted in the plot.
- PA.Birch: presence (Y) or absence (N) of birch in the plot.
- MeanChewerTree: average leaf-chewer damage across all leaves on a tree.
- MeanDefolTree: average total defoliation by chewers/miners across all leaves on a tree.
- SumMinersTree: total miners across all leaves on a tree.
- MeanMildewTree: average powdery mildew infection across leaves on a tree.
- MeanPShootLength: mean primary shoot length (mm) per tree (average across 10 shoots).
- MeanLShootLength: mean lammas shoot length (mm) per tree (average across 10 shoots; NA when lammas shoots absent).
- H.2018: Q. robur height in cm measured in 2018.

## Potential GIS applications and data products
- Spatial maps of damage indices (chewers, mildew) and shoot lengths across blocks and plots.
- Visualization of oak apparency gradients and their relation to herbivory and disease.
- Layered analyses combining Plot.Composition, Richness, Irrigation, and Resource.Dilution with damage metrics.
- Data suitable for integrating with plot shapefiles or site rasters to support spatial statistics and landscape-scale management insights.

## References
- Bert, D. et al. (2016). Powdery Mildew Decreases the Radial Growth of Oak Trees with Cumulative and Delayed Effects over Years. PLOS ONE.
- Castagneyrol, B. et al. (2017). Bottom-up and top-down effects of tree species diversity on leaf insect herbivory. Ecology and Evolution.
- Castagneyrol, B. et al. (2013). Plant apparency, an overlooked driver of associational resistance to insect herbivory. Journal of Ecology.
- Castagneyrol, B. et al. (2018). Anti-herbivore defences and insect herbivory: Interactive effects of drought and tree neighbours. Journal of Ecology.