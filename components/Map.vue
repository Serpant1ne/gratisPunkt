<template>
  <LMap
    :zoom="15"
    :center="[49.8728, 8.6512]"
    :use-global-leaflet="false"
    :options="{ zoomControl: false }"
    class="min-h-dvh">
    <!-- Outdoors -->
    <LTileLayer
      url="https://tiles.stadiamaps.com/tiles/outdoors/{z}/{x}/{y}{r}.png"
      attribution='&copy; <a href="https://www.stadiamaps.com/" target="_blank">Stadia Maps</a> &copy; <a href="https://openmaptiles.org/" target="_blank">OpenMapTiles</a> &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
      layer-type="base"
      name="ESRI World Street Map"
      class="z-0" />

    <!-- Stock -->
    <!-- <LTileLayer
      url="https://tile.openstreetmap.org/{z}/{x}/{y}.png"
      attribution='&copy; <a href="https://www.stadiamaps.com/" target="_blank">Stadia Maps</a> &copy; <a href="https://openmaptiles.org/" target="_blank">OpenMapTiles</a> &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
      layer-type="base"
      name="ESRI World Street Map"
      class="z-0" /> -->
  </LMap>
</template>

<script lang="ts" setup></script>

<style></style>
