# Shapefiles with the outline of maximum water spread resulting from the catastrophic release of the Kakhovka Reservoir after the destruction of the Kakhovka Hydroelectric Power Plant by Russian occupying forces

# Authors:

### Moskalenko Yu. O.<sup>1</sup> strix@strix.ks.ua

### Pliushch S. O.<sup>1</sup>
<br>

*<sup>1</sup> Black Sea Biosphere Reserve of National Academy of Sciences of Ukraine*

*Lermontova St. 1, Hola Prystan, 75600 Ukraine, https://bsbr.in.ua*

<br>


The map is based on remote sensing data from Sentinel-2A (processing level L2A) dated June 8, 2023, and Landsat-9 (Collection 2 Level-2) dated June 9, 2023.

The following Sentinel-2 remote sensing data granules were used:<br>S2A_MSIL2A_20230608T084601_N0509_R107_T36TUS_20230608T132103.SAFE
S2A_MSIL2A_20230608T084601_N0509_R107_T36TVS_20230608T132103.SAFE<br>
S2A_MSIL2A_20230608T084601_N0509_R107_T36TWS_20230608T132103.SAFE<br>
S2A_MSIL2A_20230608T084601_N0509_R107_T36TVT_20230608T132103.SAFE

The following remote sensing data scenes from Landsat-9 were used:<br>
LC09_L2SP_179028_20230609_20230611_02_T1<br>
LC09_L2SP_179027_20230609_20230611_02_T1

The contour of the maximum water spread was constructed using a method of manual visual interpretation of remote sensing data, relying on knowledge of the local terrain. We consciously chose not to use automated methods with water indices such as the Normalized Difference Water Index (NDWI) or the Modified Normalized Difference Water Index (MNDWI), as these do not effectively distinguish water surfaces in areas covered with forest or dense reed thickets. Similarly, we did not use the SRTM digital elevation model due to significant artifacts in the study area, where the model shows the height of the forest canopy instead of the ground surface in forested areas.

For visual interpretation of Sentinel-2A remote sensing data, we used combinations of spectral bands NIR-Red-Green (8-4-3) and SWIR2-NIR-Green (12-8-3). For the visual interpretation of Landsat-9 remote sensing data, we used combinations of bands SWIR1-NIR-Red (6-5-4) and NIR-Red-Green (5-4-3). To better align the resolution of Sentinel-2A remote sensing data (10 m/pixel) with that of Landsat-9 (30 m/pixel), the latter's resolution was enhanced using the panchromatic channel (Band 8) through IHS-based pansharpening to 15 m/pixel. The pansharpening was performed using a custom bash script, utilizing command-line tools and utilities such as ImageMagick (https://imagemagick.org), listgeo, and geotifcp (https://github.com/OSGeo/libgeotiff). To expedite the pansharpening process, both Landsat scenes were cropped to the study region and merged by bands using the gdal_translate and gdal_merge.py utilities from the GDAL library (https://gdal.org/). For convenience, the Sentinel-2A data tiles T36TUS, T36TVS, and T36TWS were also cropped and merged by bands using custom scripts available at https://doi.org/10.5281/zenodo.13205058.

During visual interpretation, the above-mentioned remote sensing data were compared with satellite images acquired before the destruction of the Kakhovka Hydroelectric Power Plant. In particular, Landsat-9 remote sensing data were compared with Landsat-8 data from June 1, 2023, and Sentinel-2A data were compared with Sentinel-2B data from June 3, 2023.

Repository files:<br>
floodMax_UTM36N.zip — contains the shapefile in UTM36N projection (EPSG:32636);<br>
floodMax_WGS84.zip — contains the shapefile in geographic coordinates in WGS84 (EPSG:4326);<br>
floodMax_WGS84.geojson.zip — contains a GeoJSON file in WGS84 coordinates (EPSG:4326).

# Web version of the map

The web version of the maximum water spread map is available at:<br>https://yumoskalenko.github.io/floodmap_Kakhovka2023/

Embed code for the map on a webpage:

```
<iframe style="border: 1px solid black" src="https://yumoskalenko.github.io/floodmap_Kakhovka2023/index.html" marginwidth="0" marginheight="0" scrolling="no" width="100%" height="350" frameborder="0"></iframe>
```

---

***This scientific and technical product was created by the scientists of the Black Sea Biosphere Reserve of the National Academy of Sciences of Ukraine during the implementation of research on the topic "Monitoring the condition of natural complexes of the Black Sea Biosphere Reserve (‘Chronicle of Nature’)" (state registration number 0121U109174).***

---

## License agreement

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
