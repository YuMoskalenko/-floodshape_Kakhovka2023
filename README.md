# Shapefiles with the outline of maximum water spread resulting from the catastrophic release of the Kakhovka Reservoir after the destruction of the Kakhovka Hydroelectric Power Plant by Russian occupying forces

The map is based on remote sensing data from Sentinel-2A (processing level L2A) dated June 8, 2023, and Landsat-9 (Collection 2 Level-2) dated June 9, 2023.

The following Sentinel-2 remote sensing data granules were used: S2A_MSIL2A_20230608T084601_N0509_R107_T36TUS_20230608T132103.SAFE
S2A_MSIL2A_20230608T084601_N0509_R107_T36TVS_20230608T132103.SAFE
S2A_MSIL2A_20230608T084601_N0509_R107_T36TWS_20230608T132103.SAFE
S2A_MSIL2A_20230608T084601_N0509_R107_T36TVT_20230608T132103.SAFE

The following remote sensing data scenes from Landsat-9 were used:
LC09_L2SP_179028_20230609_20230611_02_T1
LC09_L2SP_179027_20230609_20230611_02_T1

The contour of the maximum water spread was constructed using a method of manual visual interpretation of remote sensing data, relying on knowledge of the local terrain. We consciously chose not to use automated methods with water indices such as the Normalized Difference Water Index (NDWI) or the Modified Normalized Difference Water Index (MNDWI), as these do not effectively distinguish water surfaces in areas covered with forest or dense reed thickets. Similarly, we did not use the SRTM digital elevation model due to significant artifacts in the study area, where the model shows the height of the forest canopy instead of the ground surface in forested areas.

For visual interpretation of Sentinel-2A remote sensing data, we used combinations of spectral bands NIR-Red-Green (8-4-3) and SWIR2-NIR-Green (12-8-3). For the visual interpretation of Landsat-9 remote sensing data, we used combinations of bands SWIR1-NIR-Red (6-5-4) and NIR-Red-Green (5-4-3). To better align the resolution of Sentinel-2A remote sensing data (10 m/pixel) with that of Landsat-9 (30 m/pixel), the latter's resolution was enhanced using the panchromatic channel (Band 8) through IHS-based pansharpening to 15 m/pixel. The pansharpening was performed using a custom bash script, utilizing command-line tools and utilities such as ImageMagick (https://imagemagick.org), listgeo, and geotifcp (https://github.com/OSGeo/libgeotiff). To expedite the pansharpening process, both Landsat scenes were cropped to the study region and merged by bands using the gdal_translate and gdal_merge.py utilities from the GDAL library (https://gdal.org/). For convenience, the Sentinel-2A data tiles T36TUS, T36TVS, and T36TWS were also cropped and merged by bands using custom scripts available at https://doi.org/10.5281/zenodo.13205058.

During visual interpretation, the above-mentioned remote sensing data were compared with satellite images acquired before the destruction of the Kakhovka Hydroelectric Power Plant. In particular, Landsat-9 remote sensing data were compared with Landsat-8 data from June 1, 2023, and Sentinel-2A data were compared with Sentinel-2B data from June 3, 2023.

Repository files
• floodMax_UTM36N.zip — contains the shapefile in UTM36N projection (EPSG:32636);
• floodMax_WGS84.zip — contains the shapefile in geographic coordinates in WGS84 (EPSG:4326);
• floodMax_WGS84.geojson.zip — contains a GeoJSON file in WGS84 coordinates (EPSG:4326).

The web version of the maximum water spread map is available at: https://yumoskalenko.github.io/floodmap_Kakhovka2023/


***This scientific and technical product was created by the scientists of the Black Sea Biosphere Reserve of the National Academy of Sciences of Ukraine during the implementation of research on the topic "Monitoring the condition of natural complexes of the Black Sea Biosphere Reserve (‘Chronicle of Nature’)" (state registration number 0121U109174).***


# Карта максимального розливу води внаслідок катастрофічного спуску Каховського водосховища після підриву Каховської ГЕС російськими окупаційними військами

Карта укладена на основі даних дистанційного зондування Sentinel-2A (рівня обробки L2A) за 8 червня 2023 р. та Landsat-9 (Collection 2 Level-2) за 9 червня 2023 р.

Із даних дистанційного зондування Sentinel-2 були використані наступні гранули:
S2A_MSIL2A_20230608T084601_N0509_R107_T36TUS_20230608T132103.SAFE
S2A_MSIL2A_20230608T084601_N0509_R107_T36TVS_20230608T132103.SAFE
S2A_MSIL2A_20230608T084601_N0509_R107_T36TWS_20230608T132103.SAFE
S2A_MSIL2A_20230608T084601_N0509_R107_T36TVT_20230608T132103.SAFE

Із даних дистанційного зондування Landsat-9 були використані наступні сцени:
LC09_L2SP_179028_20230609_20230611_02_T1
LC09_L2SP_179027_20230609_20230611_02_T1

Контур максимального розливу побудований методом ручного візуального дешифрування даних дистанційного зондування, під час якого дешифрування здійснювали у т.ч. опираючись на власне знання рельєфу місцевості. Ми свідомо відмовилися від автоматичних методів з використанням водних індексів на зразок нормалізованого диференційного водного індексу (NDWI) чи модифікованого нормалізованого диференційного водного індексу (MNDWI), оскільки вони не дають можливості розпізнавати водну поверхню на територіях вкритих лісом чи щільними очеретяними зарослями. Аналогічно, ми відмовилися від використання цифрової моделі рельєфу SRTM через наявність у ній великих площ артефактів для досліджуваного регіону, які полягають у тому, що модель на лісовкритих територіях показує не висоту поверхні землі, а висоту поверхні лісового пологу.

Для візуального дешифрування даних дистанційного зондування Sentinel-2A використали комбінацію спектральних каналів NIR-Red-Green (8-4-3) та SWIR2-NIR-Green (12-8-3). Для візуального дешифрування даних дистанційного зондування Landsat-9 послуговувалися комбінацією каналів SWIR1-NIR-Red (6-5-4) та NIR-Red-Green (5-4-3). Для кращого узгодження роздільності даних дистанційного зондування Sentinel-2A (10 м/піксель) та даних дистанційного зондування Landsat-9 (30 м/піксель) роздільність останніх була покращена за допомогою  панхроматичного каналу (Band 8) шляхом паншарпінгу за методом IHS до 15 м/піксель. Для паншарпінгу був використаний оригінальний скрипт на bash з використанням консольних програм та утиліт ImageMagick (https://imagemagick.org), listgeo та geotifcp (https://github.com/OSGeo/libgeotiff). Для пришвидшення процесу паншарпінгу обидві сцени Landsat були обрізані по регіону дослідження і поканально обʼєднані за допомогою утиліт gdal_translate та gdal_merge.py із бібліотеки GDAL (https://gdal.org/). Для зручності роботи тайли T36TUS, T36TVS та T36TWS із даних дистанційного зондування Sentinel-2A також були обрізані і поканально об'єднані за допомогою оригінальних скриптів доступних за адресою https://doi.org/10.5281/zenodo.13205058.

Під час візуального дешифрування зазначені вище дані дистанційного зондування порівнювалися із супутниковими знімками отриманими до підриву Каховської ГЕС. Зокрема дані дистанційного зондування Landsat-9 порівнювалися із даними дистанційного зондування Landsat-8 за 1 червня 2023 р., а дані дистанційного зондування Sentinel-2A порівнювалися із даними дистанційного зондування Sentinel-2B за 3 червня 2023 р.

Файли репозиторію
floodMax_UTM36N.zip — містить шейп-файл у проекції UTM36N (EPSG:32636);
floodMax_WGS84.zip — vscnbnm шейп-файл у географічних координатах у системі координат WGS84 (EPSG:4326);
floodMax_WGS84.geojson.zip — містить файл у форматі GeoJSON у системі координат WGS84 (EPSG:4326).

Веб-версія карти максимального розливу води доступна за адресою: https://yumoskalenko.github.io/floodmap_Kakhovka2023/

***Дана науково-технічна продукція створена фахівцями Чорноморського біосферного заповідника НАН України в ході виконання досліджень за темою  НДР „Моніторинг стану природних комплексів Чорноморського біосферного заповідника („Літопис природи“)“ (держ. реєстраційний № 0121U109174).***
