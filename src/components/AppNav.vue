<script>
export default {
    name: 'AppNav',

    data() {
        return {
            links: ["Home", "Prodotti", "Chi Siamo", "Contatti"],

            activeLinkIndex: 1,
        }
    }
}
</script>

<template>
  <nav>
    <img id="logo" src="/img/la-molisana-logo.png" alt="Molisana Logo">

    <ul id="links">

        <li v-for="(currentLink, index) in links" :class="index == activeLinkIndex ? 'active' : ''">
            {{ currentLink }}
        </li> 

    </ul>
  </nav>        
</template>

<style lang="scss">

nav {
    display: flex;
    flex-flow: column;
    align-items: center;


    #logo {
        margin-bottom: 30px;
    }

    ul {
        display: flex;
        list-style-type: none;
        padding: 0;

        li {
            padding: 10px 14px;
            font-weight: 500;

            cursor: pointer;

            &.active {
                background-color: #dae9fe;
            }
        }
    }
}


</style>