<template>
  <h3>Puntos</h3>
  <div class="mapLine__container">
    <l-map :useGlobalLeaflet="false" v-model="zoom" v-model:zoom="zoom" :center="[40.4167, -3.7035]">
      <l-tile-layer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"></l-tile-layer>
      <l-control-layers />
      <l-marker :lat-lng="[40.4167, -3.7035]">
        <l-popup>
          Madrid
        </l-popup>
      </l-marker>
      <l-marker :lat-lng="[41.3851, 2.1734]">
        <l-popup>
          Barcelona
        </l-popup>
      </l-marker>
      <l-marker :lat-lng="[37.625, -0.9963]">
        <l-popup>
          Cartagena
        </l-popup>
      </l-marker>
    </l-map>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import {
  LMap,
  LTileLayer,
  LMarker,
  LControlLayers,
  LPopup,
} from "@vue-leaflet/vue-leaflet";
import "leaflet/dist/leaflet.css";

const zoom = ref(6);
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
