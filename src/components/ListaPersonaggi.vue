<template>
  <div class="container">
      <div class="row">

          <!-- <div class="col" v-for="(personaggio, indice) in listaPersonaggi" :key="indice">
              <img :src="personaggio.image">
              <h1>{{personaggio.name}}</h1>
              <h6>{{personaggio.origin}}</h6>
              <h6>{{personaggio.gender}}</h6>
          </div> -->

        <CardPersonaggio 
        v-for="(personaggio, indice) in listaPersonaggi" 
        :key="indice" 
        :personaggio="personaggio"
        />

      </div>

  </div>
</template>

<script>

// integro axios nel mio progetto partendo dalla copia presente in node_modules
const axios = require('axios');
import CardPersonaggio from './partials/CardPersonaggio.vue';

export default {
    name: "ListaPersonaggi",
    data() {
        return {
            // creo un oggetto di personaggi
            listaPersonaggi: [],
            loadingInPorgress: true,
            endpoint: 'https://api.sampleapis.com/rickandmorty/characters' 
        }
    },
    components: {
        CardPersonaggio 
    },
    methods: {
        // creo una funzione
        getPersonaggi() {
            // richiesta axios al server remoto - inserisco url personaggi
            axios.get(this.endpoint)
            .then((response) => {
                this.listaPersonaggi = response.data;
                this.loadingInPorgress = false;
            })
            .catch(function(error) {
                // errore
                console.log(error);
            })
        }
    },
    // chiama la funzione una volta creata azione
    created() {
        this.getPersonaggi();
    }
}
</script>

<style scoped lang="scss">

</style>