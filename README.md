# 3D Wetlands App
<p>Google Earth Engine (GEE) Application to visualize and compare land cover changes and Digital Elevation Models (DEM) over the wetland areas of the Northern Gulf of Mexico and Florida at very high-resolutions.</p>

Link: https://lizcanosandoval.users.earthengine.app/view/hr-land-cover-gulf-of-mexico

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/gee-app.JPG" width="800">

## Introduction:
The 3D Wetlands App provide access to two large collections, (1) Landcover and (2) DEM, ingested to Earth Engine. The landcover product offer access to 12,929 processed and classified imagery at 2 m per pixel from WorldView-2 and WorldView-3 satellites, with temporal coverage from 2009 to 2018 (this is not consistent over time).

Satellite imagery coverage:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/wv-coverage.JPG" width="800">

The landcover analysis includes the following classes:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/classes.JPG" width="300">

The DEM product was built with 178 airborne topographic Lidar surveys (bare-earth) over the wetland and coastal areas of the Northern Gulf of Mexico and Florida. This product has horizontal resolution of 2-m per pixel and vertical accuracy of 0.2 m. 

DEM Coverage:

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/images/dem.png" width="800">

The 3D Wetlands App is open access through GEE. The users do not require a GEE account to use all the features available in the [app interface](https://lizcanosandoval.users.earthengine.app/view/hr-land-cover-gulf-of-mexico). If the user has a GEE account can have access to an [advanced version](https://code.earthengine.google.com/47c4f5bbc0182929f4273c24dd2315b6) which will allow to export data to the respective Google Drive account by clicking a button. To this point previous experience with GEE is **not required**. However, the access of the landcover and DEM collections for other specific uses through the code editor previous knowledge with GEE is required (See the [GEE Documentation](https://developers.google.com/earth-engine)).

## Features:
* Create, visualize and compare land cover mosaics of two user-defined periods in one or more selected Counties.
* Visualize the DEM associated to the selected Counties.
* Create mosaics including all or single landcover classes.
* See the number of images used to create a mosaic.
* Download the generated mosaics as .png (Basic Interface).
* Export the generated mosaics in as a GeoTiff image (Advanced Interface).
* Calculate the area (km2) of each class in the mosaic and export as a .csv file (Advanced Interface).
* Access to the whole landcover and DEM collections through the code editor (Advanced Interface).

## FAQ
**How are the landcover mosaics generated?**

The landcover mosaics are generated by calculating the maximum value of each pixel across the stack of all available images in the selected Counties. This prioritazes classes with higher pixel values such as Developed (pixel value 11) and minimize the presence of clouds (pixel value 1). If a single class is selected, then the final mosaic is just a stack of the respective pixel values.

**Do I need a Google Earth Engine account to use the app?**
No, everyone can use the 3D Wetlands app through the GEE App platform. But, a GEE account is required for exporting data and other advanced features.

**Can I have access to the landcover and DEM collections?**

Yes, full access to the collections is possible trough the GEE code editor (Advanced Interface).

**Can I download the generated mosaics and DEM trough the app?**

Yes, the mosaics can be downloaded as .png (Basic Interface) or .tiff (Advanced Interface).

## Disclaimer:
The 3D Wetlands App provide access to processed satellite imagery and LiDAR data as a tool for public and academic use. The raw satellite data is property of DigitalGlobe. The 3D Wetlands App is a product of the ongoing research project *Enhanced 3-D Mapping for Habitat, Biodiversity, and Flood Hazard Assessments of Coastal and Wetland Areas of the Southern US* granted by NSF to Frank Muller-Karger and Timothy Dixon at the University of South Florida, in collaboration with James Gibeaut at the Harte Research Institute, TAMU-CC.

## Credits:
The WorldView imagery was processed at the Institute for Marine Remote Sensing (IMARS) at the College of Marine Science, University of South Florida and the DEM was acquired by the Harte Research Institute for Gulf of Mexico Studies at Texas A&M University - Corpus Christi. Google Earth Engine is the platform where the data is stored and distributed. Special thanks to Noel Gorelick who helped to ingest the image collections in GEE.

<img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/USF-Logo2.png" width="300"> <img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/TAMUCC_block.png" width="200"> <img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/nsf-logo.jpg" width="300"> <img src="https://raw.github.com/luislizcano/3D-wetlands-app/main/logos/gee-logo.png" width="300">
