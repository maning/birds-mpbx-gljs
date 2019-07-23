This tutorial is a step-by-step guide for creating a fully interactive map using Mapbox GL JS.
We will use IUCN's List of Endangered Birds in the Philippines from 
[Birdlife's Red Data Book](https://web.archive.org/web/20060202013628/http://www.rdb.or.id/) (2005)
to show sightings threaned birds througout the country.

For an overview of how Mapbox works, visit **https://docs.mapbox.com/help/how-mapbox-works/**


## Create mapbox account
* Signup for a mapbox account at: https://account.mapbox.com/auth/signup/

![](img/signup_page.png)

## Creating a blank html page 

* Open a text editor and copy the code below to create a blank html page.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <h1>test</h1>
  </body>
</html>
```

* Save the file as `index.html`.
* Open the file in your browser.


## Creating your first Mapbox map
This step-by-step guide will walk you through your first webmap powered bvy Mapbox GJ JS.

* To start creating your first map, go to: https://www.mapbox.com/install/

![](img/pick_platform.png)

* In the **Pick platform** step, select **JS**

* In the **Pick method** step, choose the **Use the Mapbox CDN**

![](img/pick_method.png)

* Copy the GL JS JavaScript and CSS files in the <head> of your HTML file.

```
<script src='https://api.mapbox.com/mapbox-gl-js/v1.1.1/mapbox-gl.js'></script>
<link href='https://api.mapbox.com/mapbox-gl-js/v1.1.1/mapbox-gl.css' rel='stylesheet' />
```

![](img/install_js.png)


* Add the following code to the <body> of your HTML file.

```
<div id='map' style='width: 400px; height: 300px;'></div>
<script>
  mapboxgl.accessToken = 'pk.eyJ1IjoibWFuaW5nc2FtYmFsZSIsImEiOiJjamx3YTQya2ExNWdlM3FwM3Z1YWp2bHZrIn0.mk2emL4LkX_uwFPq7nHZsA';
  var map = new mapboxgl.Map({
    container: 'map',
    style: 'mapbox://styles/mapbox/streets-v11'
  });
</script>
```

![](img/create_map.png)

* Open your `index.html` in your browser.

# [wip] Adding controls to your mapbox map.

# [wip] Loading GeoJSOn file to your map.

# [wip] Adding interactivity to your map.

## cluster
## icon by type
## pop-up
