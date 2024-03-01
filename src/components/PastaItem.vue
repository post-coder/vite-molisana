<script>
export default {
    name: 'PastaItem',

    // questo componente per essere visualizzato correttamente
    // esige alcune proprietà (props)
    props: {
        // dobbiamo dare un nome a queste proprietà
        // per ognuna di esse dobbiamo indicare nome e TIPO DI DATO
        // String, Number, Boolean, Array, Object
        pastaName: String,
        pastaImage: String
    },

    data() {
    },
}
</script>

<template>

    <div class="pasta">
        <img :src="pastaImage" :alt="pastaName">
        <h4>{{ pastaName }}</h4>
    </div>

</template>

<style lang="scss">

.pasta {
    width: calc(100% / 4);

    padding: 20px;

    border: solid 1px #dae7ff;
    background-color: white;

    img {
        width: 100%;
    }
}

</style>