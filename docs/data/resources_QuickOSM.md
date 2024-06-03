## QuickOSM

[QuickOSM Plugin](https://plugins.qgis.org/plugins/QuickOSM/) is a plugin in QGIS that can generate geospatial datasets based on simple `key`, `value` queries.

### Installation of QuickOSM

1. Open QGIS.
2. Go to `Plugins` > `Manage and Install Plugins...`.
3. Search for `QuickOSM`.
4. Click `Install`.

### Generating Datasets with QuickOSM

#### Queries Table

| GeoPackage File                                                                                                                                                                                                                            | AND/OR | `key`    | `value`          | `in`   | `overpass query src code`                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|----------|------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [admin_boundaries_perimeter.gpkg](..%2F..%2Fmain%2Fdata%2Fcustom_data%2Fgeneral_data%2Fadmin_boundaries_perimeter.gpkg), [admin_boundaries_points.gpkg](..%2F..%2Fmain%2Fdata%2Fcustom_data%2Fgeneral_data%2Fadmin_boundaries_points.gpkg) | -      | boundary | administrative   | Nagano | <details><summary>Show Query</summary><pre>```[out:xml] [timeout:25]; {{geocodeArea:Nagano}} -> .area_0; ( node["boundary"="administrative"](area.area_0); way["boundary"="administrative"](area.area_0); relation["boundary"="administrative"](area.area_0); ); (._;>;); out body;```</pre></details>                                                                   |
| [shrines.gpkg](..%2F..%2Fmain%2Fdata%2Fcustom_data%2Fgeneral_data%2Fshrines.gpkg)                                                                                                                                                          | -      | amenity  | place_of_worship | -      | -                                                                                                                                                                                                                                                                                                                                                                        |
|                                                                                                                                                                                                                                            | AND    | religion | shinto           | Nagano | <details><summary>Show Query</summary><pre>[out:xml] [timeout:25]; {{geocodeArea:Nagano}} -> .area_0; ( node["amenity"="place_of_worship"]["religion"="shinto"](area.area_0); way["amenity"="place_of_worship"]["religion"="shinto"](area.area_0); relation["amenity"="place_of_worship"]["religion"="shinto"](area.area_0); ); (._;>;); out body;</pre></details>       |
| [temples.gpkg](..%2F..%2Fmain%2Fdata%2Fcustom_data%2Fgeneral_data%2Ftemples.gpkg)                                                                                                                                                          | -      | amenity  | place_of_worship | -      |                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                                                                                                                                                                                            | AND    | religion | shinto           | Nagano | <details><summary>Show Query</summary><pre>[out:xml] [timeout:25]; {{geocodeArea:Nagano}} -> .area_0; ( node["amenity"="place_of_worship"]["religion"="buddhist"](area.area_0); way["amenity"="place_of_worship"]["religion"="buddhist"](area.area_0); relation["amenity"="place_of_worship"]["religion"="buddhist"](area.area_0); ); (._;>;); out body;</pre></details> |

### Steps to Generate Data

1. **Open QuickOSM Plugin**:
   - Go to `Vector` > `QuickOSM` > `QuickOSM...`.

2. **Enter Query Parameters**:
   - Fill in the `Key` and `Value` fields with the appropriate query parameters from the table above.

3. **Run Query**:
   - Click `Run Query`.

4. **Save the Data**:
   - Once the data is loaded into QGIS, right-click on the layer and select `Export` > `Save Features As...` to save the data in your desired format (e.g., GeoPackage, Shapefile).
