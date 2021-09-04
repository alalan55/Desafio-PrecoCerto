<template>
    <div class="home-template">
        <Header/>
        <Filtros/>
        <Tabela :produtos="produtos" />
    </div>
</template>

<script>
import{Header, Filtros, Tabela} from '@/components/organisms'
    export default {
        props:['produtos'],
        components:{
            Header,
            Filtros,
            Tabela
        },
        created(){
            console.log('vim do pai', this.produtos)
        }
    }
</script>

<style lang="scss" scoped>

</style>