# GOES-R ABI L2 Status Dashboard & Viewer

**Live View:** [https://coliveir-aer.github.io/goes-quickview/](https://coliveir-aer.github.io/goes-quickview/)  
**Repository:** [https://github.com/coliveir-aer/goes-quickview](https://github.com/coliveir-aer/goes-quickview)

## Overview
The GOES-R ABI L2 Status Dashboard & Viewer is a browser-based application designed for monitoring and visualizing Geostationary Operational Environmental Satellite (GOES-R) Advanced Baseline Imager (ABI) Level 2 products. The application combines a real-time data availability dashboard with a high-performance, purely client-side NetCDF sandbox environment.

## Core Features

### AWS S3 Availability Dashboard
* **Real-time Monitoring:** Queries NOAA's Open Data Registry via AWS S3 to track the availability of ABI L2 products.
* **Multi-Satellite Support:** Seamlessly switch between GOES-16, GOES-17, GOES-18, and GOES-19.
* **Domain Filtering:** View data availability across Full Disk (FD), CONUS (C), and Mesoscale (M1/M2) sectors.
* **Direct Access:** Instantly load available data into the viewer, download it locally, or copy the HTTPS/S3 URIs.

### Client-Side NetCDF Sandbox
* **In-Browser Parsing:** Utilizes `h5wasm` to parse and extract NetCDF (.nc) arrays directly within the client, eliminating the need for backend processing servers.
* **High-Performance Map Overlays:** Implements precise mathematical forward-projection to map TopoJSON vector boundaries directly into the satellite's native fixed-grid scan angles. This provides instant geographic context without the computational overhead of raster grid resampling.
* **Interactive Visualization:** * **1D Sequences:** Charting for single-dimension datasets.
    * **2D Rasters:** Interactive panning, zooming, custom colormaps, and a pixel inspector for precise latitude/longitude value extraction.
    * **3D Volumes:** Slice exploration using Three.js for multi-dimensional arrays.
