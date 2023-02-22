<template>
    <div>
      <input type="radio" id="map1" value="map1" v-model="selectedMap" @change="updateMap">
      <label for="map1">MHI</label>
      <input type="radio" id="map2" value="map2" v-model="selectedMap" @change="updateMap">
      <label for="map2">Food</label>
      <input type="radio" id="map3" value="map3" v-model="selectedMap" @change="updateMap">
      <label for="map3">Economic Stability</label>
      <input type="radio" id="map4" value="map4" v-model="selectedMap" @change="updateMap">
      <label for="map4">Community and Social Context Stability</label>
      <input type="radio" id="map5" value="map5" v-model="selectedMap" @change="updateMap">
      <label for="map5">Education</label>
      <div v-if="selectedMap === 'map1'" id="app">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 750px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="ocMHData" titleKey="zip" idKey="zip_code" :value="ocValue" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
                <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Mental Health Index Averages by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    <div>
      <div v-if="selectedMap === 'map2'">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 750px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="sdohData" titleKey="ZIPCODE" idKey="ZCTA" :value="foodValue" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
              <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Social Determinants of Health by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    </div>
    <div>
      <div v-if="selectedMap === 'map3'">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 750px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="sdohData" titleKey="ZIPCODE" idKey="ZCTA" :value="econValue" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
              <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Social Determinants of Health by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    </div>
    <div>
      <div v-if="selectedMap === 'map4'">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 750px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="sdohData" titleKey="ZIPCODE" idKey="ZCTA" :value="comValue" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
              <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Social Determinants of Health by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    </div>
    <div>
      <div v-if="selectedMap === 'map5'">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 750px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="sdohData" titleKey="ZIPCODE" idKey="ZCTA" :value="eduValue" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
              <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Social Determinants of Health by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
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
  import { sdohData } from '../data/sdohData'
  import ocGeojson from '../data/ocGeoZipCode.json'
  import { ocMHData } from '../data/averaged_data_zipcode'
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
          selectedMap: 'map1',
          colorScale: ["71ae46", "ebe12a", "ac2026"],
          foodValue: {
            key: "ACS_PCT_HH_NO_FD_STMP_BLW_POV_ZC",
            metric: "Food Stamps"
          },
          ocValue: {
            key: "mhi_avg",
            metric: "Mental Health Index"
          },
          econValue:{
            key: "ACS_PCT_UNEMPLOY_ZC",
            metric: "% Unemployed"
          },
          comValue: {
            key: "POS_DIST_CLINIC_ZP",
            metric: "Distance Nearest Health Clinic"
          },
          eduValue: {
            key: "ACS_TOT_POP_WT_ZC",
            metric: "% Teens and Adults Unemployed and Not in School"
          },
          mapOptions: {
            attributionControl: false
          },
          currentStrokeColor: '3d3213'
        }
      
    },
    methods: {
      updateMap(){
        
      }
    }
  }
  </script>
  <style>
  body {
    background-color: #e7d090;
    margin-left: 0px;
    margin-right: 0px;
  }
  #map {
    background-color: rgb(0, 0, 0);
  }
  .info-control-wrapper {
    background-color: blueviolet;
  }
  </style>