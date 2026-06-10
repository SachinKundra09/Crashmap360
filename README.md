# Crashmap 360

This repository includes the code used for **Crashmap 360: A data-driven infrastructure recommendation system for Washington, D.C.**

The analysis was run in Google Colab, with public datasets downloaded from Open Data DC and stored in Google Drive. To reproduce the analysis, download the datasets from the links below and place them in the same Google Drive folder structure used in the notebook, or update the file paths in the code.

The project uses public Washington, D.C. crash and infrastructure data to identify locations that may need further traffic-safety review. The final analysis focuses on three crash categories: night crashes, speeding-involved crashes, and cyclist-involved crashes.

The code is organized into separate pipelines for each category:

- night: analyzes night crashes in relation to streetlights
- speeding: analyzes speeding-involved crashes in relation to speed cameras and speed humps
- cyclist: analyzes cyclist-involved crashes in relation to bike lanes
- logistic: analyzes predictors of high-severity crash hotspots

The category pipelines include the main distance calculations, clustering, severity rankings, exposure-normalized rankings, comparison tests, robustness checks, and maps used in the paper.

The project uses public datasets from Open Data DC and the District Department of Transportation, including crash records, streetlights, speed cameras, speed humps, bicycle lanes, roadway centerlines, traffic volume data, and the High Injury Network.

## Data Sources

- **Crash data** — Open Data DC, *Crashes in DC*  
  https://opendata.dc.gov/datasets/70392a096a8e431381f1f692aaa06afd_24

- **Streetlight locations** — Open Data DC, *Street Lights*  
  https://opendata.dc.gov/datasets/street-lights

- **Automated traffic enforcement camera locations** — District Department of Transportation, *Automated Traffic Enforcement Camera Locations*  
  https://ddot.dc.gov/publication/automated-traffic-enforcement-camera-locations

- **Speed hump locations** — Open Data DC, *Speed Humps*  
  https://opendata.dc.gov/datasets/DCGIS::speed-humps

- **Roadway centerlines / roadway segment data** — Open Data DC, *Roadway Centerlines*  
  https://opendata.dc.gov/pages/roadway-centerlines

- **Bicycle lane locations** — Open Data DC, *Bicycle Lanes*  
  https://opendata.dc.gov/datasets/bicycle-lanes

- **Traffic volume / AADT data** — Open Data DC, *2023 Traffic Volume*  
  https://opendata.dc.gov/datasets/DCGIS::2023-traffic-volume/about

- **High Injury Network comparison data** — Open Data DC, *High Injury Network*  
  https://opendata.dc.gov/datasets/DCGIS::high-injury-network-1

To run the Crashmap360 code, the above datasets must be installed and the paths must match the appropriate dataset.

This project identifies candidate locations for further review. It does not prove that missing infrastructure caused crashes, and final decisions would require field review and engineering judgment.

The assistance of large language models was used in developing parts of Crashmap 360's software. All design, algorithms, methodology decisions, and interpretations were made by the author.
