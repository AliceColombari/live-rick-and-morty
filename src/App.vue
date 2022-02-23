<template>
  <div id="app">
    <MyHeader messaggio="Rick and Morty App"/>
    <ListaPersonaggi/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import ListaPersonaggi from './components/ListaPersonaggi.vue';


export default {
  name: 'App',
  components: {
    MyHeader,
    ListaPersonaggi,
  }
}
</script>

<style lang="scss">
  @import './style/general.scss';
</style>
