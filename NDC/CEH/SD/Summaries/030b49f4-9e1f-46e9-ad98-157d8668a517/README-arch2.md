# Package overview

- Purpose: R package with functions to examine the distribution of species records, understand sampling trends and potential biases, and build correlative presence-background species distribution models (SDMs) to predict species distribution across the landscape.
- Target data: Built to work with ERCCIS opportunistic species records (Environmental Record Centre for Cornwall and the Isles of Scilly).
- Data availability: Data are not included in the package; can be requested from ERCCIS (Cornwall Wildlife Trust) at https://erccis.org.uk/requestingdata.
- Data used and scope: Code analyses data held by ERCCIS and other species occurrence records; data structure supports standard R package workflows.
- Data organization: The package is structured as a standard R package; code for data processing and SDMs resides in R/; grids for analysis in data/.
- Data provenance: Species record data are not included in the package but can be obtained from ERCCIS or other sources.
- Installation and access: Install via install.packages(); functions documented in the package; run help(function_name) or ?function_name for usage.
- Outputs and use: Functions produce analyses of distribution, sampling trends, biases, and SDM-based predictions suitable for environmental monitoring and policy evaluation.
- Documentation: Each function has accompanying documentation accessible through standard R help mechanisms; additional guidance provided in the package vignette.