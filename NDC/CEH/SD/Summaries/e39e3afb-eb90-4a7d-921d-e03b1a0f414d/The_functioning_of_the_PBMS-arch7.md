# THE FUNCTIONING OF THE PBMS - taken from Lee A. Walker, Richard F. Shore, Anthony Turk, M. Glo ´ria Pereira and Jennifer Best, The Predatory Bird Monitoring Scheme: Identifying Chemical Risks to Top Predators in Britain, 2008, Ambio Vol. 37, No. 6, 466-471.

## Overview
- Describes how the Predatory Bird Monitoring Scheme (PBMS) operates to monitor contaminant concentrations in predatory birds, using liver tissues and eggs as primary matrices.
- Choice of matrix depends on the contaminant and species; some toxins are best detected in liver, others in eggs.
- Uses sampling strategies that enable study of rare species (e.g., eggs for low-density species like golden eagles and merlins).
- Data collection relies on voluntary submissions from the public and other contributors, with extensive postmortem and biometric data recorded.

## Sampling, Collection, and Handling
- Submissions come from the public (via ads), taxidermists, and wildlife rehabilitation centers; only freeliving birds or those in captivity ≤7 days are used.
- Packaging standards and postal submission are defined; about 400 birds submitted yearly, with autumn and early spring being peak periods (about 60% of annual submissions).
- On receipt, carcasses are logged and stored at -20°C prior to examination.
- Postmortem examination records include age (EURING classification), sex, body weight, and putative cause of death; additional notes include fat reserves, moult, and organ hemorrhaging.
- When possible, organs and tissues are excised and archived at -20°C; eggs are similarly processed and archived.

## Core Monitoring Program and Matrices
- Liver and egg samples are analyzed for contaminants; specific sampling schemes include:
  - Livers from a stratified sample of sparrowhawks; livers of all herons; one egg from each merlin, golden eagle, and white-tailed sea eagle clutch.
  - Approximately 10 gannet eggs (Bass Rock and Ailsa Craig colonies) analyzed biennially.
  - Livers from a stratified sample of barn owls; livers of all kestrels and red kites.
- Analytes include PCBs (35 congeners, total PCBs, and PCB-TEQs), organochlorine insecticides, mercury; SGARs (difenacoum, bromadiolone, brodifacoum, flocoumafen) in specified species.
- Analyses are conducted by the Centre for Ecology and Hydrology; methods are described in other publications.

## Data Dissemination and Feedback
- Results are published in annual reports, scientific papers, and on the PBMS website.
- Collectors receive feedback in the form of postmortem reports or biometric data for eggs, plus summaries of contaminant levels for analyzed samples. This feedback supports ongoing engagement with volunteers.

## Archive and Data Resource
- The PBMS frozen archive spans back to 1968 and contains roughly:
  - 17,500 tissue samples from 6,000 individual birds
  - 9,000 egg contents
  - 82% of tissue samples date from 1980 onwards
- The archive supports: environmental toxicology studies beyond core PBMS, piloting/refining new monitoring, and projects addressing nonchemical threats (e.g., illegal trade, hunting) and fine-scale genetic studies (e.g., golden eagle populations).

## Data, Collaboration, and Funding
- The program is supported by multiple bodies: Centre for Ecology and Hydrology, Joint Nature Conservation Committee, Natural England, Environment Agency, and the Campaign for Responsible Rodenticide Use.
- Active collaboration with volunteers who submit specimens and receive feedback, maintaining strong engagement.

## GIS and Data-Product Implications for Spatial Analysts
- Data types suitable for GIS-based products:
  - Spatial provenance: collection sites and colony locations (e.g., Bass Rock, Ailsa Craig) and submission origins.
  - Temporal coverage: long-running time series with seasonal peaks (autumn, early spring) and year-to-year variation.
  - Biological metadata: species, age class, sex, and clutch information, enabling species- and age-specific mapping.
  - Contaminant data: concentrations of PCBs, OC insecticides, mercury, and SGAR residues by specimen or group, enabling hotspot analysis and trend mapping.
- Potential map-based outputs:
  - Contaminant concentration maps by species, tissue type, and geographic area.
  - Temporal heatmaps showing changes in contaminant levels across years and seasons.
  - Spatial layers of sampling effort and coverage to identify data gaps or resolve bias in the dataset.
  - Overlay analyses with land use, rodenticide usage, and other environmental layers to explore drivers of contamination.
- Data-management considerations for GIS:
  - Standardized metadata and georeferencing for all samples (collection site, habitat type, colony coordinates).
  - Integration of multi-matrix data (liver, eggs) across species for coherent spatial analyses.
  - Provenance tracking and data quality assurance to support reproducible mapping and analyses.
  - Linking archive records with current and historical data to enable retrospective spatial analyses.

## Key Takeaways for GIS Specialists
- PBMS provides rich, longitudinal, georeferenced data on contaminants in predatory birds, with explicit spatially-relevant collection sites and colonies.
- The scheme’s extensive archive and multi-species, multi-matrix design offer opportunities to build comprehensive map-based products illustrating spatial and temporal trends in environmental contaminants.
- Collaboration with volunteers and clear data-handling protocols are strengths, but demonstrated challenges (data held in multiple places, varying resolutions, and need for consistent standards) should be addressed in any GIS data model development.