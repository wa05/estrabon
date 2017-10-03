<template>
  <q-layout>
  	<gmap-map
  	  :center="center"
  	  gestureHandling="none"
    	:zoom="zoom"
    	style="width: 100%; height: 400px"
    	:options="options"
  	>
    <gmap-marker
      :key="index"
      v-for="(m, index) in markers"
      :position="m.position"
      :clickable="true"
      :draggable="false"
      @click="center=m.position"
    ></gmap-marker>
  	</gmap-map>
  </q-layout>
</template>

<script>
  import * as VueGoogleMaps from 'vue2-google-maps'
  import Vue from 'vue'
  import {
    QLayout
  } from 'quasar'

  Vue.use(VueGoogleMaps, {
    load: {
      key: 'AIzaSyAoreMUeY1WL0_DbIt2kbWX-Ozp_RxsLiE'
    }
  })

  export default {
    components: {
      QLayout
    },
    data () {
      return {
        options: {
          gestureHandling: 'greedy'
        },
        center: {
          lat: -32.964641,
          lng: -60.650486
        },
        zoom: 16,
        markers: [
          {
            position: {
              lat: -32.953886,
              lng: -60.656629
            }
          }
        ]
      }
    }
  }
</script>

<style>
</style>
