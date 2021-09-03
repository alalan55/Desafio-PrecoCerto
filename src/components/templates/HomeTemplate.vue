<template>
    <div class="home-template">
        <Header/>
        <Filtros/>
        <Tabela />
    </div>
</template>

<script>
import{Header, Filtros, Tabela} from '@/components/organisms'
    export default {
        components:{
            Header,
            Filtros,
            Tabela
        }
    }
</script>

<style lang="scss" scoped>

</style>