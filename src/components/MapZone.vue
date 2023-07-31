<template>
  <h3>Zona</h3>
  <div class="mapLine__container">
    <l-map :useGlobalLeaflet="false" v-model="zoom" v-model:zoom="zoom" :center="[40.4170, -3.7035]" @move="log('move')">
      <l-tile-layer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"></l-tile-layer>
      <l-control-layers />
      <l-polygon :lat-lngs="[
        [40.5355, -3.8956],
        [40.3121, -3.8956],
        [40.3121, -3.5159],
        [40.5355, -3.5159],
      ]" color="#41b782" :fill="true" :fillOpacity="0.5" fillColor="#41b782" />
    </l-map>
  </div>
</template>

<script lang="ts" setup>

import {
  ref,
  onMounted,
  onUnmounted
} from "vue";

import {
  LMap,
  LTileLayer,
  LControlLayers,
  LPolygon,
} from "@vue-leaflet/vue-leaflet";
import "leaflet/dist/leaflet.css";

const zoom = ref(9);

const log = (a: any) => {
  console.log(a);
}



</script>

<style lang="scss" scoped>
.mapLine {
  &__container {
    display: flex;
    width: 800px;
    height: 600px;
  }
}
</style>
