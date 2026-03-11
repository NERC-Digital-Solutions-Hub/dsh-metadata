### Availability of superfast broadband (Z-Score)

**Description:**
This field (which is identified as `ZLackSuperfastBroadband` or "Lack of superfast broadband (Z-Score)" in the spatial dataset) represents the standardized Z-score for the percentage of premises lacking access to superfast broadband within a given Lower Super Output Area (LSOA). It measures how the local concentration of poor high-speed internet connectivity in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric is a core indicator within the "Internet" domain, which is utilized to evaluate a community's "(In)ability to Prepare," "(In)ability to Respond," and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher proportions of premises without high-speed internet access indicate a higher level of social vulnerability. Poor digital connectivity restricts a community's capacity to quickly access vital online information, receive early hazard warnings, and navigate digital services and support networks required during the recovery phase.

**Interpretation:**
Because this metric is standardized as a Z-score and typically reversed to reflect a *lack* of access, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher lack of superfast broadband (poorer availability) than the national average, indicating a higher level of social vulnerability.
*   **Values around 0** indicate that the availability is approximately average for England.
*   **Negative values** signify better availability than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from Ofcom (2018), specifically measuring superfast broadband (SFBB) availability in January 2018 (% premises). It carries a weight of 0.500 within the broader "Internet" domain, sharing this domain equally with the indicator for sub-standard broadband. 

*Dataset Note:* The methodology explicitly advises that this indicator should be used with caution because it does not take account of the availability of *ultrafast* broadband, and users are recommended to refer to the latest data from Ofcom for the most current picture.