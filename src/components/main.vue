<template>
    <div class="bg-darkgray">
        <div class="p-5 container">

            <h2 class="m-5 white"> Content goes here </h2>

        </div>
    </div>

    <div class="bg-blue">
        <div class="p-5 row container m-auto">
            <div class="acquisto d-flex align-items-center justify-content-center"
            v-for="acquisto in listaAcquisti">
                <img :src="acquisto.img">
                <span class="white p-2">{{acquisto.stringa}}</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            listaAcquisti:[
                {
                    stringa: "DIGITAL COMICS",
                    img: "buy-comics-digital-comics.png"
                },{
                    stringa: "DC MERCHANDISE",
                    img: "buy-comics-merchandise.png"
                },{
                    stringa: "SUBSCRIPTION",
                    img: "buy-comics-subscriptions.png"
                },{
                    stringa: "COMIC SHOP LOCATOR",
                    img: "buy-comics-shop-locator.png"
                },{
                    stringa: "DC POWER VISA",
                    img: "buy-dc-power-visa.svg"
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.bg-darkgray {
    background-color: rgb(29, 29, 29);
}

.bg-blue{
    background-color: #0C7CEC;
}

.white {
    color: white;
}

.acquisto{
    width: 20%;

    img{
        width: 15%;
    }

}
</style>