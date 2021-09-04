<template>
    <header>
        <NavBar class="links"/>
        <UserNavBar class="user"/>
    </header>
</template>

<script>
import {NavBar,UserNavBar} from '@/components/molecules'
    export default {
        components:{
            NavBar,
            UserNavBar
        }
    }
</script>

<style lang="scss" scoped>
header{
    padding: .1rem 1.5rem;
    width: 100%;
    height: 75px;
    background: #333F48;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .links{
        flex: 5;
    }
    .user{
        flex: 1;
    }
}

</style>