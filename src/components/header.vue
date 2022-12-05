<template>
    <nav class="navbar navbar-expand-lg bg-white navbar-dc">
        <div class="container">

            <a class="navbar-brand" href="#">
                <img src="/dc-logo.png" alt="">
            </a>

            <div class="navbar h-100">
                <ul class="navbar-nav">
                    <li class="nav-item" v-for="(link, i) in listaLink">
                        <a class="nav-link active" aria-current="page" href="#" @click="setSelezionato(i)">
                            <h6 :class="(link.selected == true) ? 'selezionato' : ''">{{ link.nome }}</h6>
                        </a>
                    </li>
                </ul>
            </div>

        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            listaLink: [
                { nome: 'CHARACTERS', selected: false },
                { nome: 'COMICS', selected: false },
                { nome: 'MOVIES', selected: false },
                { nome: 'TV', selected: false },
                { nome: 'GAMES', selected: false },
                { nome: 'COLLECTIBLES', selected: false },
                { nome: 'VIDEOS', selected: false },
                { nome: 'FANS', selected: false },
                { nome: 'NEWS', selected: false },
                { nome: 'SHOP', selected: false },
            ]
        }
    },
    methods: {

        setSelezionato(indice) {
            this.listaLink.forEach(element => {
                element.selected=false
            }); {
              
            };
            this.listaLink[indice].selected = true;
        }
    }
}
</script>

<style scoped lang="scss">
.selezionato {
    color: #0C7CEC;
    border-bottom: 2px solid #0C7CEC;
    margin: 0;
}

.navbar-dc {
    width: 100%;
    position: fixed;
    top: 0;
    z-index: 10;
}
</style>