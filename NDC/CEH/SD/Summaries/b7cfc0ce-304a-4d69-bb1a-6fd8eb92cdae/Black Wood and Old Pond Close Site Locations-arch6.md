# Plot locations and notes for Black Wood and Old Pond Close studies

- The document is a dataset describing plot locations with metadata for two main sites: Black Wood (Hampshire) and Old Pond Close (Northamptonshire), plus numerous missing or placeholder fields.
- Each entry includes fields such as UK County, Start date (day, month, year), End date (day, month, year), grid reference, and Notes.
- Notes reference published works:
  - Neal et al., 2004 for plot locations at Black Wood.
  - Neal, C. 2002 for interception and attenuation study at Old Pond Close.
  - Neal, C. 1994 for interception of chemicals at a forest edge at Black Wood, Hampshire.
- The entries indicate study-related metadata about interception/atmospheric pollution research in lowland forested sites.

- Primary plotted sites:
  - Black Wood, Hampshire
    - Start: 23 May 1990
    - End: 12 December 1991
    - Grid reference: SU534428
    - Notes reference detailed plot locations in Neal et al., 2004; related interception study (Neal et al., 1994)
  - Old Pond Close, Northamptonshire
    - Start: 20 March 1991
    - End: 6 April 1992
    - Grid reference: SP877551
    - Notes reference plot location details in Neal, 2002; related interception study in Sci. Tot. Environ.

- Data structure and consistency
  - Fields present: UK County, Start date day/month/year, End date day/month/year, grid reference, Notes.
  - Many entries contain missing values (represented by dots) for several fields, indicating incomplete data.
  - Repeated entries include numerous placeholders (UK County = ., Start date = ., End date = ., grid reference = ., Notes = .), suggesting partial records or template rows.

- Data quality challenges relevant to Data Support
  - Understanding the ask: clarifying the scope to extract meaningful location-time data.
  - Patchy data across formats and systems (in this text, mainly a flat, inconsistent line-based format).
  - Extracting and validating data provenance from Notes (citations to Neal et al. and related papers).
  - Cleaning and transforming to a usable schema (standardizing date formats, resolving missing values, normalizing county names).

- Potential end-user outputs and data products
  - A clean, canonical dataset with standardized fields: site_name, UK_county, start_date, end_date, grid_reference, notes, and source_citations.
  - A geospatial view mapping Black Wood and Old Pond Close using the provided grid references.
  - A data provenance appendix listing the cited works (Neal 1994; Neal 2002; Neal et al. 2004) and their relevance to each plot.
  - Dashboards or pivot views to explore timeframes, plot coverage, and article references for the studies.

- Suggested data preparation steps (Data Support tasks)
  - Normalize field names and fill in missing values where possible (e.g., deducing UK County from context or leaving as missing if not determinable).
  - Convert Start/End date fields to standard ISO date format.
  - Validate and standardize grid references; optionally convert to geographic coordinates for mapping.
  - Link Notes to structured provenance fields (cite Neal references and associated years).
  - Create a summarized catalog of plots with key attributes (site_name, county, date range, grid_ref, notes) for reuse in dashboards and reports.