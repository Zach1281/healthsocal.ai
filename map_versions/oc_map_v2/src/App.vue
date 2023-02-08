<template>
  <div>
    <input type="radio" id="map1" value="map1" v-model="showMap">
    <label for="map1">Map 1</label>
    <input type="radio" id="map2" value="map2" v-model="showMap">
    <label for="map2">Map 2</label>
    <div v-if="showMap === 'map1'" id="app">
      <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 750px;" :options="mapOptions">
        <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
        <l-choropleth-layer :data="ocMHData" titleKey="zip" idKey="zip_code" :value="value" :extraValues="extraValues" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
          <template slot-scope="info">
            <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
            <l-reference-chart title="Mental Health Index Averages by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
          </template>
        </l-choropleth-layer>
      </l-map>
    </div>
  <div>
    <div v-if="showMap === 'map2'">
      <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 750px;" :options="mapOptions">
        <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
        <l-choropleth-layer :data="sdohData" titleKey="ZIPCODE" idKey="ZCTA" :value="value" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
          <template slot-scope="info">
            <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
            <l-reference-chart title="Mental Health Index Averages by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
          </template>
        </l-choropleth-layer>
      </l-map>
    </div>
  </div>
</div>
</template>

<script>
import { InfoControl, ReferenceChart, ChoroplethLayer } from 'vue-choropleth'

//import { geojson } from './data/py-departments-geojson'
import { sdohData } from './data/sdohData'
import ocGeojson from './data/ocGeoZipCode.json'
import { ocMHData } from './data/avg_data_zipcode'
import {LMap, LTileLayer} from 'vue2-leaflet';

export default {
  name: "app",
  components: { 
    LMap,
    LTileLayer,
    'l-info-control': InfoControl, 
    'l-reference-chart': ReferenceChart, 
    'l-choropleth-layer': ChoroplethLayer 
  },
  data() {
    return {
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      attribution: '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      ocMHData,
      ocGeojson,
      sdohData,
      showMap: 'map2',
      colorScale: ["71ae46", "ebe12a", "ac2026"],
      value: {
        key: "ACS_PCT_HH_NO_FD_STMP_BLW_POV_ZC",
        metric: "Food Stamps"
      },
      value1:{
        key: "mhi_value",
        metric: "Mental Health Index"
      },
      mapOptions: {
        attributionControl: false
      },
      currentStrokeColor: '3d3213'
    }
  },
  methods: {
    toggleMap1 () {
      this.showMap1 = !this.showMap1
    },
    toggleMap2 () {
      this.showMap2 = !this.showMap2
    }
  }
}

</script>
<style>
@import "../node_modules/leaflet/dist/leaflet.css";
body {
  background-color: #e7d090;
  margin-left: 0px;
  margin-right: 0px;
}

#map {
  background-color: rgb(0, 0, 0);
}
</style>
