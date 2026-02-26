# Long-term vegetation monitoring data for the Moor House, exclosure and grazing plots, 1953-2016.

## Overview
- A long-term, map-relevant vegetation dataset from Moor House National Nature Reserve, tracking exclosure (ungrazed) versus grazed plots from 1953 to 2016.
- Nine plots across multiple sites, each with paired fenced (exclosure) and unfenced (grazed) areas, to assess grazing effects on upland vegetation.
- Data collected using a 1 m pin frame with 10 pins per frame, recording vegetation height strata and species touches or presence/absence.

## Experimental design
- Initiation in 1953 with nine plots added over time to study the effect of eliminating sheep grazing on typical upland vegetation.
- Each plot contains paired areas: a fenced exclosure adjacent to a grazed area.
- Permanent fences mark exclosures; smaller markers indicate the extent of nearby grazed plots.
- Plot locations vary by vegetation type; transects and frame locations differ between sites and over time.

## Sampling and data collection methods
- Irregular survey intervals since establishment; data collected with a 1 m frame, 10 pin positions at 10 cm intervals.
- At each pin, 2 mm vegetation is dropped to the soil surface; each pin is recorded by height strata for vascular plants and as unstratified for non-vascular plants and ground substrates.
- Height strata (strata): 1 = >30 cm, 2 = 20–30 cm, 3 = 10–20 cm, 4 = 0–10 cm; 99 = unstratified.
- For vascular plants, the number of touches within each strata is recorded (scores 1–13); for non-vascular plants, bryophytes/lichens, and ground substrates, presence/absence is recorded (score = 1 when present, 99 otherwise).
- Bryophytes/lichens and other non-vascular data are generally recorded only as unstratified presence/absence.
- Data quality controlled by experienced botanical surveyors working in pairs using consistent methods and equipment.
- Frame usage varies by site (frame used only at Bog Hill).

## Data structure and terminology
- Core fields: Site, Plot (enclosed or grazed), Year, Transect (numbers vary by site), Quadrat, Frame (Bog Hill only), Pin, Strata (1–4 or 99), Score (number of pin touches or presence indicator), Species number (VESPAN), Species name (updated to current nomenclature).
- Data include both absolute counts (touches per stratum) and presence/absence data (unstratified for bryophytes/lichens and others).
- Species coding aligns with Environmental Change Network (ECN) standards; names updated to current taxonomy.

## Site and temporal coverage
- Sites include Knock Fell, Trout Beck Head, Hard Hill, River Tees, Silver Band, Cottage Hill, Little Dun Fell, Moss Burn, and Bog Hill.
- Year ranges span from mid-1950s through 2016, with site-specific survey histories and varying numbers of points per treatment.
- Summary notes indicate variations in sampling schemes over time, including changes in the number of points, stratification, and bryophyte recording practices.

## Data quality, caveats, and gaps
- Some years exhibit data irregularities or missing elements (e.g., 1976 enclosed transect data lost; 1981 data gaps for enclosed frames; 1973 data sampled randomly in some plots).
- Moss Burn: 2013 survey noted that the enclosed plot was opened to grazing afterward, so an ungrazed plot no longer exists.
- Specific plots may have altered transect counts, frame positions, or bryophyte recording status across years.
- Documentation clarifies that data variations reflect methodological changes rather than solely data loss.

## Practical notes for GIS and data use
- Height strata and score interpretation are consistent within vascular plants; bryophytes/lichens and ground substrates are recorded as presence/absence (unstratified).
- Frame usage and transect orientations differ by site and year; when integrating data, account for site-specific methods and frame positions (e.g., Bog Hill frame relevance).
- Species codes (VESPAN) and updated species names enable cross-year harmonization; ensure taxonomy aligns with ECN conventions.
- Data quality relies on paired professional surveys; clear provenance exists through site, plot, year, and method documentation.

## Related documentation and sources
- Marrs, R.H., Rawes, M., Robinson, J., & Poppitt, S. (1986). Long-term studies of vegetation change at Moor House NNR: guide to recording methods and the database.
- Adamson, J.K. & Kahl, J. (2001). Changes in vegetation at Moor House within sheep exclosure plots established between 1953 and 1972.
- Environmental Change Network (ECN) database references and nomenclature.
- Additional notes and plot-specific method updates are documented in the accompanying data records and plot logs.