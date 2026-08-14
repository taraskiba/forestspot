# forestspot


[![image](https://img.shields.io/pypi/v/forestspot.svg)](https://pypi.python.org/pypi/forestspot)


### A python package for foresters to query Google Earth Engine data
**Streamlining the process to bring remotely sensed data to foresters**

[![ForestSPOT](docs/files/logo.png)](https://github.com/taraskiba/forestspot)


-   Free software: MIT License
-   Documentation: https://taraskiba.github.io/forestspot/


## Walkthrough and Demonstration

[![](https://markdown-videos-api.jorgenkh.no/youtube/eaoYLEwzeQc?si=qXwAPfExQKgODc24)](https://youtu.be/eaoYLEwzeQc?si=qXwAPfExQKgODc24)


## Features

-   Access and retrieve pixel values from Google Earth Engine Images or ImageCollections and a desired time-period for a .CSV provided coordinates.
    -   Results can be exported averaged over matching plot IDs or individual points.
-   Buffer sensitive coordinates:
    -   Buffer to a singular point within a specified radius.
    -   Buffer to *n* points within a specified radius.
-   Create a map with provided coordinates and built-in basemaps and geojson overlays.
-   Please understand the limitations of Google's confidentiality policy before use.

## Installation
```python
pip install forestspot
```

Once installed, you need to authenticate your Google Earth Engine account. You can do this by running the following commands in Python:

```python
import ee
# Initialize Earth Engine
ee.Authenticate()
ee.Initialize(project="ee-forestplotvariables")
```

To load widget boxes, run the following command in Python:

```python
# For single point buffering
import forestspot.buffer_coordinates as sbc
single = sbc.BufferCoordinates().vbox
single

# For multiple point buffering
import forestspot.buffer_and_sample as sbs
multiple = sbs.Buffer().vbox
multiple

# For non-aggregated point extraction
import forestspot.point_extraction as spe
point = spe.PointExtraction().vbox
point

# For aggregated point extraction
import forestspot.aggregated_point_extraction as sape
agg = sape.AggregatedPointExtraction().vbox
agg

# For the mapping tool
import forestspot.interactive as map
m = map.Map()
m
```

## Web App

For a non-python user, you can access the Streamlit app here:
https://forestspot.streamlit.app/

## Publication
*pending*

### Logo Credit

-   Logo was designed by HiDream-I1-Dev (https://huggingface.co/spaces/HiDream-ai/HiDream-I1-Dev)