<script>
import AppJumbo from './components/AppJumbo.vue';

export default {
  components:  {
    AppJumbo,
  }
}
</script>

<template>
  <AppJumbo></AppJumbo>

  <hr>

  <div class="second-title">
    <h2>
      Testo del titolo
    </h2>
  </div>
</template>

<style lang="scss">
// possiamo importare dei fogli dove ci segnamo tutte le variabili
@use './styles/variables' as *;

// possiamo importare anche i fogli con le mixins
@use './styles/mixins' as *;



.second-title {
  @include centered;
  
  background-color: $primaryColor;
  padding: 12px;
  
  height: 600px;
}
</style>