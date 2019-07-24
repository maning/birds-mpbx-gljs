# Overview
This tutorial will guide you to adding information popups to your map and 
improve the visual style of the data using clustering. 

## Displaying popup to show data information on click. 

* Open your `index.html` in your text editor. 
* Add the following code within your script, after the `circle-color` expressions

```javascript

map.on('click', 'birds', function (e) {
var coordinates = e.features[0].geometry.coordinates.slice();
var description = e.features[0].properties.en_name;

while (Math.abs(e.lngLat.lng - coordinates[0]) > 180) {
coordinates[0] += e.lngLat.lng > coordinates[0] ? 360 : -360;
}

new mapboxgl.Popup()
.setLngLat(coordinates)
.setHTML(description)
.addTo(map);
});

```
The above code does the following: when a click event occurs on a feature in the birds layer, open a popup at the
location of the feature, with description HTML from its properties.

* Save your `index.html` and open the file in your browser.

![](img/pop_up.gif)

## Clustering


![](img/overlapping_circles.png)

![](img/clustered.png)

![](img/clustered_popup.gif)

Congratulations!  You have just added and styled an external data into your Mapbox map!


## See also

* [Display a popup on click](https://docs.mapbox.com/mapbox-gl-js/example/popup-on-click/)
* [Show polygon information on click](https://docs.mapbox.com/mapbox-gl-js/example/polygon-popup-on-click/)
* [Create and style clusters](https://docs.mapbox.com/mapbox-gl-js/example/cluster/)
