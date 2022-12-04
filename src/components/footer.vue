<template>
    <div class="background-comics">
        <div class="container row m-auto p-5 overflow-hidden">
            <div class="col-5">
                <div class="row g-0">
                    <div class="col-4">
                        <h5 class="white">DC COMICS</h5>
                        <ul class="lista">
                            <li class="gray" v-for="oggetto in listaDc">{{ oggetto }}</li>
                        </ul>
                        <h5 class="white">SHOP</h5>
                        <ul class="lista">
                            <li class="gray" v-for="oggetto in listaShop">{{ oggetto }}</li>
                        </ul>
                    </div>

                    <div class="col-4">
                        <h5 class="white">DC</h5>
                        <ul class="lista">
                            <li class="gray" v-for="oggetto in listaD">{{oggetto}}</li>
                        </ul>
                    </div>
                </div>
            </div>

            <div class="col-5 offset-1 position-relative">
                <img class="position-absolute sfondo-dc" src="/dc-logo-bg.png" alt="Logo DC di sfondo">
            </div>
        </div>

        <div class="background-gray">
            <div class="container pt-4 pb-4 m-auto row">
                <div class="col-6">
                    <button class="btn btn-outline sign-up-btn white">SIGN-UP NOW!</button>
                </div>

                <div class="col-4 offset-2 d-flex align-items-center justify-content-between p-0">
                    <h5 class="blue m-0">FOLLOW US</h5>
                    <div class="d-flex justify-content-between p-0 icone">
                        <a href="#" v-for="icona in listaIcona"><img :src="icona" alt=""></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            listaDc: [
                "Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"
            ],
            listaShop: [
                "Shop DC", "Shop DC Collectibles"
            ],
            listaD: [
                "Terms Of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"
            ],
            listaIcona: [
                "footer-facebook.png",
                "footer-periscope.png",
                "footer-pinterest.png",
                "footer-twitter.png",
                "footer-youtube.png"
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.background-comics {
    background-image: url(/footer-bg.jpg);
}

.white {
    color: white;
}

.gray {
    color: gray
}

.lista {
    list-style: none;
    padding: 0;
}

.sfondo-dc {
    width: 100%;
    transform: translate(0, -20%);
}

.background-gray {
    background-color: #383838;
}

.blue {
    color: #0C7CEC;
}

.sign-up-btn {
    border: 2px solid #0C7CEC;
    border-radius: 0;
    padding: .7rem;
}

.icone {
    width: 65%;
}
</style>