<template>
  <v-container class="main__container">
    <MapLine />
     <MapPoint />
   <MapZone />
  </v-container>
</template>

<script lang="ts" setup>
import MapLine from '@/components/MapLine.vue'
import MapPoint from '@/components/MapPoint.vue'
import MapZone from '@/components/MapZone.vue'

</script>

<style lang="scss" scoped>
.main__container {
  margin: 2rem auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 2rem;
}
</style>
