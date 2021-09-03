<template>
<div class="nav-link">
    <slot name="after"/>
    <router-link :to="link" class="link">{{name}}</router-link>
    <slot name="before"/>
</div>
</template>

<script>
    export default {
        props:{
            link:{type: String, required: true},
            name:{type: String, required: true}
        }
        
    }
</script>

<style lang="scss" scoped>
.nav-link{
    font-size: 13px;
    font-weight: 500;
    margin: 0 .6rem;
    cursor: pointer;
     display: flex;
     align-items: center;
     justify-content: space-between;

    &:hover{
        color: rgb(194, 213, 212);
    }

    .link{
        padding: 0 .3rem;
        font-weight: 500;
        letter-spacing: 1px;
    }
}
</style>