<template>
  <h3>lineas</h3>
  <div class="mapLine__container">
    <l-map :useGlobalLeaflet="false" v-model="zoom" v-model:zoom="zoom" :center="[40.4170, -3.7035]" >
      <l-tile-layer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"></l-tile-layer>
      <l-control-layers />
      <l-polyline :lat-lngs="[
        [40.4170, -3.7035],
        [40.4169, -3.7031],
        [40.4167, -3.7035],
        [40.4168, -3.7035],
        [40.4168, -3.7038],
        [40.4169, -3.7038],
        [40.4169, -3.7035],
        [40.4170, -3.7035],
      ]" color="green"></l-polyline>
    </l-map>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import {
  LMap,
  LTileLayer,
  LControlLayers,
  LPolyline
} from "@vue-leaflet/vue-leaflet";
import "leaflet/dist/leaflet.css";

const zoom = ref(20);

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
