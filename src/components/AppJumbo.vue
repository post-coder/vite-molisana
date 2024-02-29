<script>
export default {
  name: 'AppJumbo',
}
</script>

<template>

    <div id="jumbo">
        <div class="jumbo-content">
            <h1>Titolo della pagina</h1>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Ullam placeat enim beatae, voluptatum ut adipisci vel. Iusto magni iure, tempore, aspernatur blanditiis, exercitationem dicta quo molestias accusamus assumenda rem repellendus.
            </p>

            <div class="square">
                contenuto
            </div>
            <div class="pulsante">
    
                <button class="btn active">Scopri di più</button>
            </div>
        </div>
        <button>
            Altro pulsante
        </button>
    </div>

    
</template>

<style lang="scss">
@use '../styles/variables' as *;
@use '../styles/mixins' as *;




#jumbo {
    @include centered;

    height: 600px;
    padding: 40px;

    background-color: #111;
    border: $primaryColor solid 2px;
    border-radius: $spaceDimension;

    margin-bottom: 2em;

    .jumbo-content {
        max-width: 600px;
    }

    /* possiamo annidare i selettori
    
    il selettore risultante in questo caso è #jumbo .btn
    */
    .btn {
        width: 200px;

        @include styleBtn($primaryColor, white);

        &:hover {
            transform: scale(1.1);
        }
    }

    

    .square {
        @include centered;

        height: 200px;
        width: 200px;

        border: solid 1px $primaryColor;

        margin-bottom: 1em;
    }

}


button {
    @include styleBtn(#00ff00, black)
}

</style>