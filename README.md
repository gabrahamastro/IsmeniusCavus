# Influence of Ice in North-West Ismenius Cavus, Mars
## Introduction
Contained here are the files which relate to a project undertaken at l'Università degli Studi Gabriele d'Annunzio in Pescara in 2026, as part of the [Planetary Mapping and Data Processing](https://unich.coursecatalogue.cineca.it/corsi/2025/9553/insegnamenti/2025/33240_0902R-2525_45800_504425/2025/33240) course. The project was undertaken to understand the processes leading to the formation of an alcove in northwest Ismenius Cavus, located at [34.62, 16.80](https://mars.quickmap.io/layers?prjExtent=988964.0118263%2C2047438.5653706%2C1003443.9501214%2C2056663.5188444&earthShadowEnabled=true&proj=3&stack=3468%2C3569%2C277%2C3467&defs=N4IgTA7BIFyg9gBwIYGMCWAXAnrAjAL4A0IAzACwBs0cISaWuMhJFlAHLAihjrAAwA6AJzEyAVkrCudHowGCIBAkA).

## Data Sets Used
Data used are not contained here (owing to size constrains). Please find them at:
- **HiRISE**: [`ESP_049187_2150_RED`](https://ode.rsl.wustl.edu/mars/productDetail.aspx?product_id=ESP_049187_2150_RED&product_idGeo=25972314)
- [**CTX**](https://doi.org/10.17189/1520266): [`B03_010696_2144_XN_34N343W`](https://ode.rsl.wustl.edu/mars/productDetail.aspx?product_id=B03_010696_2144_XN_34N343W&product_idGeo=12806632) and [`V23_089052_2140_XN_34N343W`](https://ode.rsl.wustl.edu/mars/productDetail.aspx?product_id=V23_089052_2140_XN_34N343W&product_idGeo=49393373)
- HRSC: [`H5267_0000_DA4`](https://ode.rsl.wustl.edu/mars/indexproductpage.aspx?product_idgeo=18491941&product_id=H5267_0000_DA4.IMG)

### Processing of Data Sets
- **HiRISE**: Imported using the black-and-white `.JP2` file and associated `.LBL` file (after importing level 2 CTX `.cub` files).
- **CTX**: Processed from unprocessed CTX `.IMG` files to level 2 `.cub` files (radiometric corrections and map projection to [Mars Equirectangular](MapTemplateCTX.map)) using [ISIS](https://isis.astrogeology.usgs.gov/).
- **HRSC**: No further processing was performed, with pre-processed digital terrain model (DTM) data used. 

### Software Used
- **ISIS**: [Version `8.0.1`](https://doi.org/10.5066/P987T9CH)
- **QGIS**: [Version 3.40.3-Bratislava](https://github.com/qgis/QGIS/tree/release-3_40)
- **conda**: Version [`25.11.1`](https://github.com/conda/conda/releases/tag/25.11.1) for Apple ARM
- **GDAL**: [Version `3.13.1` Iowa City](https://github.com/OSGeo/gdal/releases/tag/v3.13.1)
- **YOLOLens**: [Version `0.1`](https://github.com/riccardolagrassa/YOLOLens_QGIS_Plugin)
- **Profile Tool**: [Version `4.3.4`](https://github.com/PANOimagen/profiletool/releases/tag/4.3.4)
- **mappy**: [Version `0.3.2`](https://github.com/europlanet-gmap/mappy/releases/tag/v0.3.2)
- **Corel Draw 2026**: Version `27.0.0.121` (to draw cross-sections)
### Symbology Used
- **gysymb**: [Version `1.1.0`](https://github.com/afrigeri/geologic-symbols-qgis/releases/tag/v1.1.0)

## File Structure
- [`LaTeX`](LaTeX): Contains all the source files for building [`Presentation.pdf`](Presentation.pdf). Note that files within [`Diagrams`](LaTeX/Figures/Diagrams/) are missing because they are released under different licence terms.
- [`QGIS`](QGIS): Contains all files related to the QGIS project (apart from basemaps, due to file-size constrains)
- [`MapTemplateCTX.map`](MapTemplateCTX.map): The map template used to map-project CTX `.IMG` files. 
- [`Presentation.pdf`](Presentation.pdf): The presentation delivered, explaining the basics about the project ([recording available here](https://youtu.be/OtV0qp5-GEE)).
    - *N.B. Contextual information (location, geological history) are not included since this was delivered alongside an introductory presentation.*
## Acknowledgements 
I would like to thank [Monica Pondrelli](https://orcid.org/0000-0002-2103-2939) for her continued and invaluable help, guidance and insights provided throughout the project. I also thank the other members of the group I was in as part of this project (Enora Toublanc, [Nicole Jimeno](https://orcid.org/0009-0002-8041-1805) and Hamda Amjad). Discussions with them helped with data processing and in developing insights into what the data may indicate.
## References
For literature used during this project, please refer to the references located at the end of [`Presentation.pdf`](Presentation.pdf).

## Licence
The main work is licenced under the Creative Commons CC BY-SA 4.0. Note, however, that this work uses images, licenced under the terms they were originally published under (details of sources available in the presentation) and the presentation uses the $\LaTeX$ [`.bst` file](LaTeX/elsarticle-harv.bst) is provided by Elsevier through Overleaf. 