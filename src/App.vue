<template>
  <div id="app">
    <div id="information">
      <div id="current-weather">
        <current-weather />
      </div>
      <hr>
      <div id="forecast">
        <forecast></forecast>
        <hr>
      </div>
    </div>
    <div id="map">
      <google-map></google-map>
    </div>
  </div>
</template>

<script>
  import CurrentWeather from './currentWeather.vue'
  import GoogleMap from './components/googleMap.vue'
  import Forecast from './components/ForeCast.vue'
  export default {
    name: 'app',
    components: {
      CurrentWeather,
      GoogleMap,
      Forecast
    }
  }
</script>

<style lang="scss">
$point-color:#fe3f32;
body{
  background-color:#fafafa;
}
  #app{
    position:absolute;
    left:50%;
    top:50%;
    width:1000px;
    height:600px;
    margin-top:-300px;
    margin-left:-500px;
    border-radius:3px;
    background-color:#444;
    box-shadow:0px 2px 2px 2px rgba(0,0,0,0.3);
    &:after{
      content:"";
      display: block;
      clear:both;
    }
    #information{
      float:left;
      width:600px;
      #current-weather{
        height:180px;
        padding-top:20px;
      }
      #forecast{
        height:400px;
      }
    }
    #map{
      float:left;
      width:400px;
      height:600px;
    }
  }
  hr{
    width:80%;
    margin:80px auto;
    border:0;
    border-top:1px solid #999;
  }
</style>
