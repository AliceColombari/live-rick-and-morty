<template>
  <div>
    <h1>{{messaggio}}</h1>
  </div>
</template>

<script>
export default {
  name: 'MyHeader',
  props: {
    "messaggio": String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  h1 {
    text-align: center;
    margin: 40px auto;
    font-weight: bold;
  }

</style>
