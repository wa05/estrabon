<template>
  <q-layout
    ref="layout"
    view="lHh Lpr fff"
    :left-class="{'bg-grey-2': true}"
  >
    <q-toolbar slot="header" class="glossy">
      <q-toolbar-title>
        Estrabón
        <div slot="subtitle">¿ Qué tanto conoces tu ciudad ?</div>
      </q-toolbar-title>
    </q-toolbar>
    

    <q-tabs slot="navigation">

      <q-route-tab
        class="ancient"
        icon="map"
        to="/map"
        exact
        slot="title"    
      />
      <q-route-tab
        class="ancient"
        icon="poll"
        to="/points"
        exact
        slot="title"
      />
      <q-route-tab
        class="ancient"
        icon="face"
        to="/profile"
       exact
        slot="title"
      />
    </q-tabs>
    


   
      <router-view /> 
    
  </q-layout>
</template>

<script>
import {
  openURL,
  QLayout,
  QToolbar,
  QToolbarTitle,
  QBtn,
  QIcon,
  QList,
  QListHeader,
  QItem,
  QItemSide,
  QItemMain,
  QRouteTab,
  QTabs
} from 'quasar'

export default {
  name: 'index',
  components: {
    QLayout,
    QToolbar,
    QToolbarTitle,
    QBtn,
    QIcon,
    QList,
    QListHeader,
    QItem,
    QItemSide,
    QItemMain,
    QTabs,
    QRouteTab
  },
  data () {
    return {
    }
  },
  methods: {
    launch (url) {
      openURL(url)
    }
  }
}
</script>

<style lang="stylus">
@import '~variables'
  .q-toolbar
    background-color $yellow-10
  .q-tabs-head
    background-color $yellow-9
</style>
