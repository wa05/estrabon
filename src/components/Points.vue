<template>
  <div>
  	<q-card inline class="col-12">
  		<q-card-media>
    		<img src="~assets/castagnino.png">
  		</q-card-media>
 		<q-card-title>
    		Museo Castagnino
    		<q-rating slot="subtitle" v-model="stars" :max="4" />
    		<div slot="right" class="row items-center">
      		<q-icon name="place" /> Pellegrini 2332 
    		</div>
  		</q-card-title>
  		<q-card-main>
    		<p></p>
    		<p class="text-faded"></p>
  		</q-card-main>
	</q-card>
	<q-card inline class="col-12">
  		<q-card-media>
    		<img src="~assets/macro.jpg">
  		</q-card-media>
 		<q-card-title>
    		Museo Macro
    		<q-rating slot="subtitle" v-model="stars" :max="4" />
    		<div slot="right" class="row items-center">
      		<q-icon name="place" /> Italia y el rio
    		</div>
  		</q-card-title>
  		<q-card-main>
    		<p></p>
    		<p class="text-faded"></p>
  		</q-card-main>
	</q-card>
  </div>
</template>

<script>
import {
  QRating,
  QIcon,
  QCard,
  QCardMedia,
  QCardTitle
} from 'quasar'

export default {
  components: {
    QRating,
    QIcon,
    QCard,
    QCardMedia,
    QCardTitle
  },
  data () {
    return {
      stars: 3
    }
  }
}
</script>

<style>
</style>
