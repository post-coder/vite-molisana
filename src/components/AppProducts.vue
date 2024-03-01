<script>
import PastaItem from './PastaItem.vue';

export default {
    name: 'AppProducts',

    components: {
        PastaItem
    },  

    data() {
        return {
            pastas: [
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                    titolo: "N.4 Spaghetto Quadrato Bucato",
                    tipo: "lunga",
                    cottura: 6,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
                    titolo: "N.5 Fettuccine",
                    tipo: "lunga",
                    cottura: 13,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
                    titolo: "N.6 Linguine",
                    tipo: "lunga",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
                    titolo: "N.7 Mezze Linguine",
                    tipo: "lunga",
                    cottura: 11,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
                    titolo: "n.11 Spaghettino Quadrato",
                    tipo: "lunga",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
                    titolo: "N.38 Mezze maniche",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
                    titolo: "N.44 Sedani",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
                    titolo: "N.49 Sedanini",
                    tipo: "corta",
                    cottura: 8,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
                    titolo: "N.53 Lumachine",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/55-chifferi-rigati.jpg",
                    titolo: "N.55 Chifferi rigati",
                    tipo: "corta",
                    cottura: 12,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/05/58-misto-corto.jpg",
                    titolo: "N.58 Misto corto",
                    tipo: "corta",
                    cottura: 9,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/06/84-ditale-quadrato.jpg",
                    titolo: "N.84 Ditale Quadrato",
                    tipo: "cortissima",
                    cottura: 12,
                },
            ]
        }
    },

    
}
</script>

<template>
    <div id="products">   
        
        <div class="pasta-list">

            <PastaItem 
                v-for="currentPasta in pastas" 
                :pastaName="currentPasta.titolo" 
                :pastaImage="currentPasta.src"
            ></PastaItem>

        </div>

    </div>
</template>

<style lang="scss">

#products {
    padding: 50px;

    background-image: url('/img/fondo-pag-speciali.jpg');
    background-size: cover;

    text-align: center;


    .pasta-list {
        display: flex;
        flex-flow: row wrap;
        
        
    }

}

</style>