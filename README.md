# StreetlightRepairEquity-To
An analysis of equity in streetlight repair response times across Calgary communities using 311 data.

# Project Overview
This project analyzes the equity of streetlight repair response times across Calgary communities using the City's 311 service request data for 2024. The goal is to identify neighborhoods that are systematically underserved in this critical public safety service by calculating a composite "Equity Score" for each community. This work supports the social sustainability goal of ensuring fair and timely access to municipal services for all residents.

# Folder Structure

# Data Sources and Methods
- **Primary Data:** [City of Calgary 311 Service Requests](https://data.calgary.ca/Services-and-Amenities/311-Service-Requests/iahh-g8bj/about_data). Filtered for streetlight-related requests in the 2024 calendar year.
- **Boundary Data:** [City of Calgary Community District Boundaries](https://data.calgary.ca/Base-Maps/Community-District-Boundaries/surr-xmvs/about_data).
- **Methods Summary:** Individual service requests were aggregated by community. For each community, a `fast_rate` (percentage resolved in 0-1 days) and a `slow_rate` (percentage taking over 2 weeks) were calculated. A composite `equity_score` was then derived, weighting the fast rate positively and penalizing the slow rate. The results were joined to community boundaries for spatial visualization. 

# Field Dictionary (for processed data)
| Field Name | Description | Data Type |
| :--- | :--- | :--- |
| `comm_code` | 3-letter community code | Text |
| `comm_name` | Full community name | Text |
| `total_requests` | Total number of streetlight requests in 2024 | Integer |
| `fast_rate` | Proportion of requests resolved in 0-1 days | Percentage |
| `slow_rate` | Proportion of requests taking >14 days | Percentage |
| `equity_score` | Composite score (0-100%) reflecting service equity | Percentage |

# Coordinate Reference System & Data Formats
- **Spatial Data CRS:** The community boundary data and resulting map use NAD83 / UTM zone 12N (EPSG:26912).
- **Data Formats:** Source and processed data are provided as `.csv` files. The final map is provided as a `.png` image.

# License and Citation
- **License:** This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/). See the `LICENSE` file for details.
- **How to Cite:**  
  To, Amber. (2024). Streetlight Repair Equity Analysis [Data set and code]. GitHub. https://github.com/amberto888/StreetlightRepairEquity-To
