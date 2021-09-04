<template>
  <HomeTemplate :produtos="produtos"/>
</template>

<script>
import{produtos} from '@/assets/mock'
import{HomeTemplate} from '@/components/templates'


export default {
  name: "App",
  components: {
    HomeTemplate,
  },
  data(){
    return{
      produtos: null
    }
  },
  created(){
    this.produtos = produtos
  }
};
</script>

<style lang="scss">

</style>
