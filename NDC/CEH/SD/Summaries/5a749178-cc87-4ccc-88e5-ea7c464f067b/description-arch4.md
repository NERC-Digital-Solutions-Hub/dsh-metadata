# Data description Beech tree ring data from hot and dry European distribution edges, 2019

- Objective: Leverage the relationship between European Beech tree growth and environmental factors (climate) to monitor and forecast drought-related declines in forest growth across Europe; growth is measured as inter-annual ring widths (dendroecology).

- Sampling scope and sites: Added 12 new European Beech sites in Bulgaria, Albania, Kosovo, and Spain (late 2019) to better represent hot and dry edge conditions; sites mostly at lower elevational ends of Beech distributions.

- Site metadata: The file site_meta.csv contains metadata for the 12 sites, including latitude, longitude, elevation, and the nearest town or village.

- Tree and core sampling: At each site, at least 15 standard canopy-level trees sampled, with two cores per tree.

- Processing and imaging: Cores air-dried, mounted, and sanded through progressively finer grits (80, 120, 300, 600, 1200); scanned to 2400 PPI images for CDendro measurements with 0.01 mm precision.

- Cross-dating and quality control: All measurements cross-dated virtually and statistically; cross-dating quality controlled using COFECH.

- Data files and structure: 12 site-specific measurement files (named by site ID) containing ring width measurements for each core by year, in mm with 0.01 mm resolution.

- File layout details: First column is year; subsequent columns hold ring width measurements for each core; tree core IDs combine site ID and tree ID; two cores per tree labeled as 'a' and 'b'; missing values indicated as NA.