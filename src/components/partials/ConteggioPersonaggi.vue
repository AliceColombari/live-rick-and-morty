<template>
  <p>I personaggi in totale sono: {{conteggio}}</p>
</template>

<script>
export default {
    name: 'ConteggioPersonaggi',
    props: ["conteggio"]
}
</script>

<style scoped lang="scss">
    p {
        text-align: center;
        margin: 50px auto;
        color: gray;
        font-size: 20px;
        font-weight: 300;
    }
</style>