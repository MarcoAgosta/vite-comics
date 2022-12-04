<script>
export default{
    components: {Header, Main, Footer}

}
import Header from "./components/header.vue"
import Main from "./components/main.vue"
import Footer from "./components/footer.vue"
</script>

<template>
<Header></Header>
<Main></Main>
<Footer></Footer>
</template>

<style lang="scss">
@use "./styles/general.scss"
</style>
