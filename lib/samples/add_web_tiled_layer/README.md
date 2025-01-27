# Add web tiled layer

Display a tiled web layer.

![Image of add web tiled layer](add_web_tiled_layer.png)

## Use case

Tiled map services are a set of pre-generated images (e.g. "tiles") arranged in folders for each row, column, and zoom level. As you navigate the map, map tiles are requested for the current extent. `ArcGISTiledLayer` and `WMTSLayer` are types of tiled map services used for specific data types. `WebTiledLayer` is useful for displaying other data sources that contain tiles arranged in a row/column/level directory structure, such as OpenStreetMap.

## How to use the sample

Run the sample and a map will appear. As you navigate the map, map tiles will be fetched automatically and displayed on the map.

## How it works

Web tiled services use a uniform addressing scheme with pre-rendered tiles. Image tiles are accessed via a URL template string, with parameters for subdomain, level, column, and row.

* Subdomain is optional and allows the Maps SDK to balance requests among multiple servers for enhanced performance.
* Level, row, and column select the tiles to load based on the visible extent of the map.

To display the web tiled layer, this sample:

1. Creates a `WebTiledLayer` from a URL.
2. Creates a new `Basemap` from the layer.
3. Updates the attribution on the layer. Note: this is a necessary step because web tiled services don't have associated service metadata.
4. Displays the basemap.

For more information about web tiled layers, see the following resources:

* [Wikipedia: tiled web maps](https://en.wikipedia.org/wiki/Tiled_web_map)
* [ArcGIS Pro: Share a web tile layer](http://pro.arcgis.com/en/pro-app/help/sharing/overview/web-tile-layer.htm)

## Relevant API

* Basemap
* WebTiledLayer

## About the data

The basemap in this sample is provided by [ArcGIS Living Atlas of the World](https://www.arcgis.com/home/item.html?id=1e126e7520f9466c9ca28b8f28b5e500). ArcGIS Living Atlas of the World provides tiled services with several unique styles.

## Tags

layer, OGC, tiled, tiles
