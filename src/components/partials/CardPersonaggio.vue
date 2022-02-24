<template>
  <div class="col">
        <img :src="personaggio.image">
        <h3>{{personaggio.name}}</h3>
        <div class="linea"></div>
        <h5>{{personaggio.origin}}</h5>
        <h6>{{personaggio.type}}</h6>
    </div>
</template>

<script>
export default {
    name: 'CardPersonaggio',
    props: {
        "personaggio": Object
    }
}
</script>

<style scoper lang="scss">

    .col {
        text-align: center;

        img {
            border-radius: 50%;
            margin-top: 40px;
            box-shadow: 0 0 3px 3px lightgray;
        }

        .linea {
            background: #000;
            height: 1px;
            width: 50px;
            margin: 20px auto;

        }

        h3 {
            margin-top: 20px;
            font-size: 20px;
            font-weight: 600;
        }

        h5 {
            font-size: 16px;
        }

        h6 {
            font-size: 16px;
            font-weight: 600;
        }
       
    }

</style>