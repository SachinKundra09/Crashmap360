# Crashmap 360

This repository includes the code used for **Crashmap 360: A data-driven infrastructure recommendation system for Washington, D.C.**

The project uses public Washington, D.C. crash and infrastructure data to identify locations that may need further traffic-safety review. The final analysis focuses on three crash categories: night crashes, speeding-involved crashes, and cyclist-involved crashes.

The code is organized into separate pipelines for each category:

- night: analyzes night crashes in relation to streetlights
- speeding: analyzes speeding-involved crashes in relation to speed cameras and speed humps
- cyclist: analyzes cyclist-involved crashes in relation to bike lanes
- logistic: analyzes predictors of high-severity crash hotspots

The category pipelines include the main distance calculations, clustering, severity rankings, exposure-normalized rankings, comparison tests, robustness checks, and maps used in the paper.

The project uses public datasets from Open Data DC and the District Department of Transportation, including crash records, streetlights, speed cameras, speed humps, bicycle lanes, roadway centerlines, traffic volume data, and the High Injury Network.

To run the Crashmap360 code, the above datasets must be installed and the paths must match the appropriate dataset.

This project identifies candidate locations for further review. It does not prove that missing infrastructure caused crashes, and final decisions would require field review and engineering judgment.

The assistance of large language models was used in developing parts of Crashmap 360's software. All design, algorithms, methodology decisions, and interpretations were made by the author.
