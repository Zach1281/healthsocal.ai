<template>
    <div>
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
      <!--Creates 5 maps that each represent a different metric, can add more as needed-->
      <input type="radio" id="map1" value="map1" v-model="selectedMap">
      <i class="fa fa-gears"></i>
      <label for="map1">  Mental Health Index     </label>
      <input type="radio" id="map2" value="map2" v-model="selectedMap">
      <i class="fa fa-cutlery"></i>
      <label for="map2">  Food      </label>
      <input type="radio" id="map3" value="map3" v-model="selectedMap">
      <i class="fa fa-dollar"></i>
      <label for="map3">  Economic Stability      </label>
      <input type="radio" id="map4" value="map4" v-model="selectedMap">
      <i class="fa fa-group"></i>
      <label for="map4">  Community and Social Context Stability      </label>
      <input type="radio" id="map5" value="map5" v-model="selectedMap">
      <i class="fa fa-pencil"></i>
      <label for="map5">  Education</label>
      <!--If new map is made, copy l-map and l-tile-layers, but other layers will be different depending on data file used-->
      <div v-if="selectedMap === 'map1'" id="app" style="text-align: left;">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 700px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <!--data links to csv/js data file, titleKey and idKey identify specific column of data
              value links to specific data value/metric in the data file, geojsonIdKey identifies geojson file
              for choropleth layer, geojson is file name itself-->
          <l-choropleth-layer :data="weighted_mhi_data" titleKey="zcta" idKey="zcta" :value="ocValue" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
                <!--info control is the pop up box on the bottom left; item is the numerical data value of the
                    current area that is being hovered over, unit is the metric of the data value, for example
                    MHI map displays Mental Health Index, Economic Map is in percentages, etc.
                    title is the light grey text that appears at the top indicating the title,
                    placeholder is placeholder text that appears when not hovering over an area-->
                <l-info-control :item="info.currentItem" :unit="info.unit" title="Zip Code" placeholder="Hover over a zip code"/>
                <!--reference chart is the box at the top right of the page, showing the map's explanation and scale
                    title is the description/title of the current map
                    colorscale is the scale of colors, by default a green-yellow-red scale
                    min and max can be copied as they are shown to have the program set
                    default values for the min and max, which will be the min and max found in the
                    data respectively-->
              <l-reference-chart title="Mental Health Index Averages by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    <div>
      <div v-if="selectedMap === 'map2'" style="text-align: left;">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 700px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
              <l-choropleth-layer :data="weighted_sdoh_data_city" titleKey="City" idKey="zcta" :value="wfoodValue" :extraValues="wfoodExtraValues" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale" @mouseover="onHover">
                <template slot-scope="info">
                  <l-info-control :item="info.currentItem" :unit="info.unit" title="City" placeholder="Hover over a zip code" @mouseover="onHover"/>
                  <l-reference-chart title="Average Percentage of Households not recieving Food Stamps by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
              </template>
              </l-choropleth-layer>
        </l-map>
      </div>
    </div>
    <div>
      <div v-if="selectedMap === 'map3'" style="text-align: left;">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 700px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="weighted_sdoh_data_city" titleKey="City" idKey="zcta" :value="weconValue" :extraValues="weconExtraValues" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
              <l-info-control :item="info.currentItem" :unit="info.unit" title="City" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Average Percentage of Unemployment (Ages 16+) by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    </div>
    <div>
      <div v-if="selectedMap === 'map4'" style="text-align: left;">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 700px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="weighted_sdoh_data_city" titleKey="City" idKey="zcta" :value="wcomValue" :extraValues="wcomExtraValues" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
              <l-info-control :item="info.currentItem" :unit="info.unit" title="City" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Average Distance to the nearest Health Clinic by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    </div>
    <div>
      <div v-if="selectedMap === 'map5'" style="text-align: left;">
        <l-map :center="[33.7175, -117.8311]" :zoom="10" style="height: 700px;" :options="mapOptions">
          <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
          <l-choropleth-layer :data="weighted_sdoh_data_city" titleKey="City" idKey="zcta" :value="weduValue" :extraValues="weduExtraValues" geojsonIdKey="dpto" :geojson="ocGeojson" :colorScale="colorScale">
            <template slot-scope="info">
              <l-info-control :item="info.currentItem" :unit="info.unit" title="City" placeholder="Hover over a zip code"/>
              <l-reference-chart title="Average Percent of People (Ages 16-19) Unemployed and Not in School by Zip Code" :colorScale="colorScale" :min="info.min" :max="info.max" position="topright"/>
            </template>
          </l-choropleth-layer>
        </l-map>
      </div>
    </div>
  </div>
  </template>
  
  <script>
  /* must import vue components, as well as any data and geojson files needed*/

  import { InfoControl, ReferenceChart, ChoroplethLayer } from 'vue-choropleth'
  //import { geojson } from './data/py-departments-geojson'
  import { sdohData } from '../data/sdohData'
  import ocGeojson from '../data/ocGeoZipCode.json'
  import { ocMHData } from '../data/avg_data_zipcode'
  import { weighted_mhi_data } from '../data/weighted_mhi_data'
  import { weighted_sdoh_data } from '../data/weighted_sdoh_data'
  import { weighted_sdoh_data_city } from '../data/weighted_sdoh_data_city'
  import { LMap, LTileLayer, LGeoJson } from 'vue2-leaflet'
 
  export default {
    name: "app",
    components: { 
      LMap,
      LTileLayer,
      LGeoJson,
      'l-info-control': InfoControl, 
      'l-reference-chart': ReferenceChart, 
      'l-choropleth-layer': ChoroplethLayer,
    },
    data() {
        return {
          /* assign values to all variables that are used above in the map parts, if using OpenStreetMap,
             copy the values for url and attribution to new map */
          url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
          position: 'topright',
          attribution: '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors',
          ocMHData,
          ocGeojson,  
          sdohData,
          weighted_sdoh_data,
          weighted_sdoh_data_city,
          weighted_mhi_data,
          selectedMap: 'map1',
          colorScale: ['#fee8c8','#fdbb84','#e34a33'],
          /* each map has its own value that they represent, if making a new map, create a new
             variable as shown here and assign it a key (the data you want to display from the data file),
             and a metric to represent the data in */
        ocValue: {
          key: "w_mhi_avg",
          metric: "Weighted Mental Health Index Average"
        },
        wfoodValue: {
          key: "w_no_food_stamps",
          metric: "% eligible families with no foodstamps"
        },
        wfoodExtraValues: [
          {
            key: "w_umemployed",
            metric: "% Unemployed"
          },
          {
            key: "distance_clinic",
            metric: "miles to nearest health clinic"
          },
          {
            key: "w_no_school_job",
            metric: "% of people ages 16-19 unemployed and not in school"
          }
        ],
        weconValue: {
          key: "w_umemployed",
          metric: "% of people unemployed"
        },
        weconExtraValues: [
          {
            key: "w_no_food_stamps",
            metric: "% eligible families with no foodstamps"
          },
          {
            key: "distance_clinic",
            metric: "miles to nearest health clinic"
          },
          {
            key: "w_no_school_job",
            metric: "% of people ages 16-19 unemployed and not in school"
          }
        ],
        wcomValue: {
          key: "distance_clinic",
          metric: "miles to nearest health clinic"
        },
        wcomExtraValues: [
          {
            key: "w_no_food_stamps",
            metric: "% eligible families with no foodstamps"
          },
          {
            key: "w_umemployed",
            metric: "% of people unemployed"
          },
          {
            key: "w_no_school_job",
            metric: "% of people ages 16-19 unemployed and not in school"
          }
        ],
        weduValue: {
          key: "w_no_school_job",
          metric: "% of people ages 16-19 unemployed and not in school"
        },
        weduExtraValues: [
          {
            key: "w_no_food_stamps",
            metric: "% eligible families with no foodstamps"
          },
          {
            key: "w_umemployed",
            metric: "% of people unemployed"
          },
          {
            key: "distance_clinic",
            metric: "miles to nearest health clinic"
          }
        ],
          /* if using OpenStreetMap, leave as true to give credit */
          mapOptions: {
            attributionControl: true
          },
          currentStrokeColor: '3d3213'
        }
      
    },
    methods: {
      onChoroplethLayerClick(event) {
        console.log('Choropleth layer clicked!', event);
        onClick();
      },
      onClick(){
        console.log("joe");
      },
      onHover(event) {
      console.log('joe')
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
  template {
    text-align: left;
  }
  </style>
  