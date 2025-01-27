# Identify graphics

Display an alert message when a graphic is tapped.

![Image of identify graphics](identify_graphics.png)

## Use case

A user may wish to select a graphic on a map to view relevant information about it.

## How to use the sample

Tap on a graphic to identify it. You will see an alert dialog displayed.

## How it works

1. Create a `GraphicsOverlay` and add it to the `ArcGISMapView`.
2. Add a `Graphic` along with a `SimpleFillSymbol` to the graphics overlay.
3. Identify the location clicked on the map view by the user with a `onTap` method.
4. Identify the graphic on the map view with `identifyGraphicsOverlay(graphicsOverlay, screenPoint, tolerance, maximumResults)`.

## Relevant API

* ArcGISMapView
* Graphic
* GraphicsOverlay

## Tags

graphics, identify
