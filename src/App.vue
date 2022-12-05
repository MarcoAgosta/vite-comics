<script>
export default{
    components: {Header, Main, Footer, Jumbo}

}
import Header from "./components/header.vue"
import Jumbo from "./components/jumbo.vue"
import Main from "./components/main.vue"
import Footer from "./components/footer.vue"
</script>

<template>
<Header></Header>
<Jumbo></Jumbo>
<Main></Main>
<Footer></Footer>
</template>

<style lang="scss">
@use "./styles/general.scss"
</style>
