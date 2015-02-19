# jquery.osmStaticMap
jquery plugin that renders osm map and colored markers in a 2d canvas (like an image).

inspired by siebigteroth/StaticMap4OSM

## Features

This plugin can render static map and put markers in any html canvases. You can easily put multiple maps with hundreds of markers each in a single page. When image is rendered, it no longer takes memory or cpu cycles, making it perfect for heavy-duty data visualization or other use.

Other customizable features includes:

* super slim - 2k minimized;
* map is auto zoomed and placed according to the locations of markers;
* you can decide maximum zoom level;
* self-adjust to different sizes of canvases;
* you can define different groups of markers with different colors;
* stroke color / line width / marker size customizable.

## Usage

basic usage:

```
$('#map-canvas').osmStaticMap({
   markers: [{
       color: 'red',
       points: [
                   {lon: -71.08454704284668,lat: 42.364251817286835},
                   {lon: -71.10222816467285,lat: 42.35790967440147}
               ]
   }]
});

```

full options:

```
$('#map-canvas').osmStaticMap({
    zoom: 17,           // zoom level when there's only a single point
	tileSize: 256,      // tile size in pixels, don't change if unclear about it.
	markers: [{
	    color: 'red',
	    points: [{lon: -71.08755648136139,lat: 42.36059723560794}]
	}],
	url:'http://a.tile.openstreetmap.org/{z}/{x}/{y}.png',  // tile url pattern
	maxZoom:18,         // max zoom level when there are multiple points
	margin: 10,         // minimum margin at the border of the map
	circleRadius: 5,    // radius of the circle marker
	circleStroleLineWidth: 1,
	circleStrokeStyle: '#333333'
});

```