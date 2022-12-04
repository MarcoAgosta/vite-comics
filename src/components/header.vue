<template>
    <nav class="navbar navbar-expand-lg bg-white">
        <div class="container">

            <a class="navbar-brand" href="#">
                <img src="/dc-logo.png" alt="">
            </a>

            <div class="navbar">
                <ul class="navbar-nav">
                    <li class="nav-item"
                    v-for="link in listaLink">
                        <a class="nav-link active" aria-current="page" href="#">
                            <h6>{{link}}</h6>
                        </a>
                    </li>
                </ul>
            </div>

        </div>
    </nav>
</template>

<script>
export default {
    data(){
        return{
            listaLink: [
                'CHARACTERS',
                'COMICS',
                'MOVIES',
                'TV',
                'GAMES',
                'COLLECTIBLES',
                'VIDEOS',
                'FANS',
                'NEWS',
                'SHOP',
            ]
        }
    },
}
</script>