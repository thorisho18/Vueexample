
<template>

  
 <l-map
   :center="center"
   :zoom="zoom"
   class="map"
   ref="map"
   @update:zoom="zoomUpdated"
   @update:center="centerUpdated"

   
 >
   <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
  <l-marker :lat-lng="marker" :draggable=true></l-marker>
 </l-map>
     
  
</template>

<script>
import { LMap, LTileLayer } from 'vue2-leaflet';
import 'leaflet/dist/leaflet.css';
import L from 'leaflet'



export default {
 components: {
   LMap,
   LTileLayer
 },
 data () {

     
   return {
     url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
     center: [ -33.918861, 18.423300],
     marker:
     [L.latLng(-33.876115,18.5008116 ),L.latLng(-33.9685533,18.5662383),L.latLng(-33.9685533,18.5662383),L.latLng(-34.0461583,18.7047383),L.latLng(-31.8994016,26.8671716),L.latLng(-31.8942983,26.878175)
     ,L.latLng(-31.9998233,27.5801216)] ,
     
     zoom : 12
   }
   
    
 },
 methods: {
   zoomUpdated (zoom) {
     this.zoom = zoom;
     console.log(this.markers)
   },
   centerUpdated (center) {
     this.center = center;
   }
 }
}

</script>

<style>
 .map {
   position: absolute;
   width: 100px;
   height: 100px;
   overflow :hidden
 }
</style>