# Data

This directory contains the input data required to run the air route network optimization algorithm. The data is sourced from the original 2019 research project and is provided in CSV format.

## `airports.csv`

This file lists the 11 major French airports used in the study, along with their geographical coordinates.

* **`code`**: The IATA airport code (e.g., `CDG`).
* **`coordinate_x`**: The x-coordinate (Abscisse) in the projected coordinate system.
* **`coordinate_y`**: The y-coordinate (Ordonnée) in the projected coordinate system.

## `traffic_demand.csv`

This file contains the daily air traffic demand between the airports. The data is provided in a "tidy" or "long" format, where each row represents a single directed route.

* **`origin`**: The IATA code of the departure airport.
* **`destination`**: The IATA code of the arrival airport.
* **`traffic`**: The number of flights per day on that specific route.
