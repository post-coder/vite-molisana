<script>
export default {
    name: 'AppFooter',

    data() {
        return {
            links: [
                {
                    title: "Pastificio",
                    list: [
                        'Il pastificio',
                        'Grano',
                        'Filiera',
                        '100 anni di pasta',
                        'Sartoria della pasta'
                    ]
                },
                {
                    title: "Prodotti",
                    list: [
                        'Le classiche',
                        'Le Integrali',
                        'Le Speciali',
                        'Le Biologiche',
                        'Le Gluten-free'
                    ]
                }

            ]
        }
    }
}
</script>


<template>
    <footer>
        <img src="/img/la-molisana-logo.png" alt="Logo Molisana">

        <div class="links">
            <div v-for="linkList in links" class="links-list">
                <h3>{{ linkList.title }}</h3>
                <ul>
                    <li v-for="currentLink in linkList.list">
                        {{ currentLink }}
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>


<style lang="scss">

footer {
    display: flex;
    justify-content: center;
    align-items: flex-start;
    gap: 150px;

    padding: 20px 10px;
    padding-bottom: 150px;

    background-image: url('/img/footer-montagne-bottom.jpg');
    background-position: bottom;
    background-repeat: repeat-x; 


    .links {
        display: flex;
        gap: 100px;

        .links-list {
            padding-right: 200px;

            h3 {
                text-transform: uppercase;
                color: #052c6d;
                font-weight: 400;
            }

            ul {
                padding: 0;
                list-style-type: none;
            }
        }
    }
}

</style>