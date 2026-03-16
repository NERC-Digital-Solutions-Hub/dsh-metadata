The field **'Heat Disadvantage, recent past 30 year mean 1990 - 2019'** (internal name `zheatdisadvantagerecentpast`) represents the final heat disadvantage score for the baseline period.

### Description

**Heat Disadvantage** maps where high social vulnerability and heat hazard-exposure coincide. This metric combines the Socio-Spatial Heat Vulnerability Index (SSHVI) with historical temperature data to identify communities that were most at risk during the 1990-2019 period.

* **Assumption:** Disadvantage occurs when populations with high biological sensitivity and low adaptive capacity live in areas with high extreme heat exposure. High positive scores identify neighbourhoods where the severity of potential impacts is greatest.
* **Vulnerability Dimension:** This is the primary output of the **Heat Exposure and Disadvantage** assessment.
* **Caveat:** An area with high social vulnerability but low hazard-exposure is not considered "disadvantaged" in this specific framework.
* **Data Source:** Calculated as the standardized sum of the **SSHVI** and the **ztmaxp95recentpast** score.
