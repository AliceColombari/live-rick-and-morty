<template>
  <div class="text-center">
      <input type="text" placeholder="Search character" v-model="ricerca" @keyup="faiRicerca">
      <button class="mx-3 ms-btn-blue" @click="faiRicerca">Ricerca</button>
      <button class="ms-btn-yellow">Azzera</button>
  </div>
</template>

<script>
export default {
    name: "RicercaPersonaggio",
    data() {
        return {
            ricerca: "",
        }
    },
    methods: {
        faiRicerca() {
            console.log('Il componennte figlio ha inviato: ' + this.ricerca);
            // emetti ricerca
            this.$emit('ricerca', this.ricerca);
        }
    }

}
</script>

<style scoper lang="scss">
    input {
        width: 600px;
        padding: 5px;
    }

    .ms-btn-blue {
        background-color: rgb(57, 57, 235);
        border: 2px solid rgb(57, 57, 235);
        border-radius: 5px;
        color: #fff;
    }

    .ms-btn-yellow {
        background-color: rgb(241, 198, 2);
        border: 2px solid rgb(241, 198, 2);
        border-radius: 5px;
        color: #000;
    }
</style>