<template>
  <div id="app">
    <div id="map">
  </div>
  </div>

</template>


 <script>
import "ol/ol.css";
import Map from "ol/Map";
import XYZ from 'ol/source/XYZ';
import View from "ol/View";
import * as proj from 'ol/proj';
// import { defaults as defaultControls, ScaleLine } from "ol/control";
import {Tile as TileLayer} from 'ol/layer';
import {OSM} from 'ol/source';
// import LayerGroup from 'ol/layer/Group';
export default {
  async mounted() {
    await this.initiateMap();
  },
  data(){
    return{
      latitude: this.latitude,
      longitude: this.longitude
    };
  },
  methods: {
    initiateMap() {

      var extent = proj.transformExtent([-1.47734462,50.88276474,-1.38719058,50.92175814],
                                     'EPSG:4326', 'EPSG:3857');
      var center = proj.transform([-1.4322676, 50.90226144],
                                     'EPSG:4326', 'EPSG:3857');
      
      var view = new View({
        projection: 'EPSG:3857',
        center: center,
        zoom: 11
      });
    
    var baseLayer = new TileLayer({
        source: new XYZ({
          urls:['https://aerodyne-abpv2.s3.eu-west-2.amazonaws.com/Maptiler/Southampton/Southampton%20Digital%20Twin/{z}/{x}/{y}.png'
              ],
          
          baseLayer: true,
          minZoom: 11,
          maxZoom: 22,
          tilePixelRatio: 1.000000
        })
      });
      // create map 
      var map = new Map({
        layers: [
          new TileLayer({
            source: new OSM()
          }),baseLayer
        ],
        target: "map",
        renderer: 'canvas',
        view: view
      });
      view.fit(extent, map.getSize());

       map.on('click', function(evt) {
         var coordinates = evt.coordinate;
         let latitude = coordinates[0];
         let longitude = coordinates[1];
         
         alert(`latitude${latitude} longitude${longitude}`)
        // console.log(`${lat},${long}`)
    });

    },
  },
};
 </script>
<style>
#map {
  position: absolute;
  margin: 0;
  padding: 0;
  height: 500px;
  width: 70%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}
#nav a {
  font-weight: bold;
  color: #2c3e50;
}
#nav a.router-link-exact-active {
  color: #42b983;
}

.coordinates{
  border-radius: 0;
  padding: 10px;
  margin-bottom: 10px;
}
</style>





