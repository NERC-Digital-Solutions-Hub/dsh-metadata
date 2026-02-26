# Biodiversity responses to vegetation height and diversity in perennial meadow plantings in two urban areas in the UK

## Overview and purpose
- Data from the Fragments, Functions and Flows in Urban Ecosystem Services (F3UES) project, part of the BESS programme, designed to quantify how meadow height and plant diversity affect plant, invertebrate, and soil microbial communities in urban greenspaces.
- Study sites: six plots across Bedford, Luton, and Cranfield University (UK).
- Objectives: assess relative roles of floristic diversity and height on biodiversity and provide data for interpretation of meadow management outcomes.

## Study design, sites and meadow establishment
- Experimental design: replicated, factorial field experiments with nine meadow treatments combining three height levels (short, medium, tall) and three diversity levels (low, medium, high).
- Plant material: perennial, native southern England species; seed mixes varied to achieve target height and floral cover per treatment.
- Plot sizes: 250 m2 per plot (50 m2 at Cranfield); one unmanipulated control area per site.
- Establishment: sown in May 2013; initial weed management and reseeding as needed to ensure establishment; some plots adjusted due to site constraints.
- Site details: Bedford (Chiltern Avenue, Jubilee Park, Goldington Green, Brickhill Heights), Luton (Bramingham Road), Cranfield University (smaller plots); some sites had incomplete treatment sets due to constraints or resident feedback.

## Treatments and mowing regimes
- Height treatments (H1–H3): Short (0.05 m, every 4–6 weeks), Medium (~0.50 m, twice yearly), Tall (up to ~1.5 m, once yearly).
- Diversity treatments (D1–D3): Low (3–4 spp, grasses only), Medium (9–13 spp, grass and forbs), High (16–21 spp, grass and forbs).
- Seed mix composition varied to meet height and diversity targets; plots separated from original sown grass by at least 5 m.

## Data collected and data structure
- Botanical surveys (2014–2015):
  - Quadrat surveys: 5 replicate 1 m2 quadrats per plot; species cover estimated using Domin scale; data include sown vs non-sown species.
  - Plot-level surveys: DAFOR-based abundance estimates and flowering cover categorized in eight percentage classes.
  - Files: Plant quadrat data, plot-level plant data, plus linking metadata.
- Invertebrates:
  - Sampling methods: sweep net, vacuum, and hand-search; summer and autumn seasons, with some winter sampling.
  - Visual surveys conducted (2014–2015) to capture observer-noticed diversity.
  - Winter overwintering assessment (Feb 2016) at several sites.
  - Data products include abundance by taxa (orders, with finer resolution for Coleoptera), biomass estimates, and visual observations.
  - Files cover sampling programmes, winter surveys, biomass data, and Coleoptera-focused data.
- Soil sampling and microbial communities:
  - Soil C, N, pH measured at two depths (0–10 cm, 11–20 cm) in select plots.
  - Microbial community structure assessed via PLFA (phospholipid fatty acids) and DNA-based methods (ITS and 16S rRNA sequencing).
  - DNA data processed to OTUs; fungal and bacterial communities analyzed separately; diversity metrics and Bray-Curtis dissimilarities calculated.
  - PLFA and DNA data included with detailed metabolomic and taxonomic indicators.
- Data structure and variables:
  - 11 CSV files provide samples, treatments, plant data, invertebrate data, soil chemistry, PLFA, and DNA data.
  - Key linking fields: PlotID, Site, PlotNo, OriginalTttmt, Ttmt, TtmtDiv, TtmtStruct, Year, and TtmtYear to connect samples across files.

## Specific data files and how they connect
- File 1: Treatments and plant-level metadata (linking site, plot, original treatments, year).
- File 2: Quadrat-level plant surveys (species, sown vs non-sown, Domin cover estimates).
- File 3: Plot-level plant surveys (DAFOR-based abundance and flowering cover).
- File 4: Invertebrate sampling program metadata (sampling methods and plot links).
- File 5: Winter invertebrate surveys (taxon placeholders and sampling notes).
- File 6: Invertebrates from visual surveys (taxonomic groupings and abundances).
- File 7: Invertebrate data from vacuum/sweep sampling (taxonomic classifications and abundances).
- File 8: Invertebrate biomass data (dry weights and sample counts).
- File 9: Coleoptera data (family-level abundances for Coleoptera from vacuum/sweep samples).
- File 10: Soils C, N, and pH data (per plot, depth, replication).
- File 11: Soil PLFA data (bacterial vs fungal indicators, PC1–PC3 coordinates and related metrics).
- DNA data: Deposited in NCBI BioProject PRJNA531648; sequencing and analysis workflow described (ITS for fungi, 16S for bacteria).

## Data processing and interpretation notes
- Plant data: Domin cover categories converted to approximate percent cover; distinction between seed-mix species and non-sown flora.
- Invertebrate data: multiple sampling methods to capture diversity, abundance, and potential visual observer biases; some taxa were analyzed at higher taxonomic resolution (e.g., Coleoptera family level).
- Soil and microbial data: standard soil chemistry analyses; PLFA used for microbial community structure; DNA data processed to OTUs with taxonomic assignment against standard databases.
- Data provenance: dataset description cites Norton et al. (2019) for background and methods; site maps are in supplementary documents.

## Access, references and related materials
- Primary publication: Norton BA et al. 2019, Urban meadows as an alternative to short mown grassland: effects of composition and height on biodiversity (Ecological Applications, in press).
- Site maps: supplementary document F3UES_meadows-expt_site-maps.pdf.
- Related methodological and stakeholder studies available in the linked literature.
- Raw DNA data available via NCBI BioProject PRJNA531648.

## Potential uses for data support and data products
- Create self-service dashboards to compare biodiversity responses across height and diversity treatments and sites.
- Cross-tabulate plant diversity, flowering, invertebrate diversity/biomass, and soil microbial indicators to identify drivers of biodiversity outcomes.
- Integrate plant, invertebrate, and soil microbial data for holistic biodiversity and ecosystem service assessments in urban meadows.
- Build reproducible data pipelines and data dictionaries to enable reuse by researchers, policy makers, and practitioners.