<template>
    <div class="bg-darkgray">
        <div class="pt-5 container position-relative">

            <div class="position-absolute serie">
                <h5 class="white m-0">CURRENT SERIES</h5>
            </div>

            <div class="row g-5">

                <div class="col-xl-2 col-3" v-for="fumetto in listaFumetti">
                    <div class="carta">
                        <img class="img-comic mb-3" :src="fumetto.thumb" alt="">
                        <span class="white">{{ fumetto.series }}</span>
                    </div>
                </div>

            </div>

            <div class="d-flex justify-content-center mt-5 pb-4">
                <button class="white btn">LOAD MORE</button>
            </div>

        </div>
    </div>

    <div class="bg-blue">
        <div class="p-5 row container m-auto">
            <div class="acquisto d-flex align-items-center justify-content-center" v-for="acquisto in listaAcquisti">
                <img :src="acquisto.img">
                <span class="white p-2">{{ acquisto.stringa }}</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            listaAcquisti: [
                {
                    stringa: "DIGITAL COMICS",
                    img: "buy-comics-digital-comics.png"
                }, {
                    stringa: "DC MERCHANDISE",
                    img: "buy-comics-merchandise.png"
                }, {
                    stringa: "SUBSCRIPTION",
                    img: "buy-comics-subscriptions.png"
                }, {
                    stringa: "COMIC SHOP LOCATOR",
                    img: "buy-comics-shop-locator.png"
                }, {
                    stringa: "DC POWER VISA",
                    img: "buy-dc-power-visa.svg"
                },
            ],
            listaFumetti: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

.btn{
    background-color: #0C7CEC;
    width: 13%;
    border-radius: 0;
}
.serie{
    background-color: #0C7CEC;
    width: fit-content;
    padding: .5rem 1.1rem;
    top: -24px;
    left: 2%;
}
.bg-darkgray {
    background-color: rgb(29, 29, 29);
}

.bg-blue {
    background-color: #0C7CEC;
}

.white {
    color: white;
}

.carta {

    img {
        max-height: 180px;
        aspect-ratio: 1/1;
        object-fit: cover;
        object-position: top;
    }
}

.acquisto {
    width: 20%;

    img {
        width: 15%;
    }

}
</style>