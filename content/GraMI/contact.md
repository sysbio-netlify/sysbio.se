---
title: Contact
menu: GraMI
weight: 60
template: GraMI/single
---
<style>
    .column {
      float: left;
      width: 50%;
    }

    .row:after {
      content: "";
      display: table;
      clear: both;
    }

    .required:after {
        content:" *";
        color: red;
    }

    .map {
        height: 400px;
        width: 90%;
    }

</style>

# Contact

<div class="row">
  <div class="column">
   <div>
    <h2>Postal and delivery address</h2>
    Chalmers University of Technology
    <br>
    Department of Biology and Biological Engineering
    <br>
    Division of Systems and Synthetic Biology
    <br>
    Kemivägen 10
    <br>
    SE-412 96 Gothenburg
    <br>
    Sweden
    <br>
    <h2>Visiting address</h2>
    Chalmers University of Technology
    <br>
    Department of Biology and Biological Engineering
    <br>
    Division of Systems and Synthetic Biology
    <br>
    Kemigården 1
    <br>
    SE-412 96 Gothenburg
   </div>
   <br><br>

   <div id="map" class="map"></div>
    <script src="https://cdn.jsdelivr.net/gh/openlayers/openlayers.github.io@master/en/v6.4.3/build/ol.js"></script>
    <script type="text/javascript">
      coordinates = [11.9773494, 57.6908956];
      var map = new ol.Map({
        target: 'map',
        layers: [
          new ol.layer.Tile({
            source: new ol.source.OSM()
          })
        ],
        view: new ol.View({
          center: ol.proj.fromLonLat(coordinates),
          zoom: 16
        })
      });

  var marker = new ol.Feature({
      geometry: new ol.geom.Point(ol.proj.fromLonLat(coordinates))
  })
  marker.setStyle(
      new ol.style.Style({
        image: new ol.style.Icon({
          //color: 'red',
          crossOrigin: 'anonymous',
          // For Internet Explorer 11
          imgSize: [40, 40],
          src: 'https://api.tiles.mapbox.com/mapbox.js/v2.4.0/images/marker-icon.png',
        }),
      })
    );

  var marker_layer = new ol.layer.Vector({
    source: new ol.source.Vector({
         features: [marker]
     })
  });
  map.addLayer(marker_layer);
</script>

  </div>

  <div class="column">
    <form name="grami-contact" method="POST" netlify-honeypot="bot-field" data-netlify="true">
      <label for="name" class="required">Name:</label><br>
        <input type="text" id="name" name="name" size="50" required><br>
      <label for="name" class="required">Email:</label><br>
        <input type="email" id="email" name="email" size="50" required><br>
      <label for="name" class="required">Subject:</label><br>
        <input type="text" id="subject" name="subject" size="50" required><br>
      <label for="name" class="required">Message:</label><br>
        <textarea id="message" name="message" rows="10" cols="50" required></textarea>
      <br>
      <input type="submit" value="Submit">
    </form>
  </div>
</div>
