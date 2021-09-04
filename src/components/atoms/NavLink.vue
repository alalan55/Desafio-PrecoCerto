<template>
<div class="nav-links">
    <slot name="after"/>
    <a href="#" class="link">{{name}}</a>
    <slot name="before"/>
</div>
</template>

<script>
    export default {
        props:{
            name:{type: String, required: true}
        }
        
    }
</script>

<style lang="scss" scoped>
.nav-links{
    
    font-size: 13px;
    font-weight: 500;
    margin: 0 .6rem;
    cursor: pointer;
     display: flex;
     align-items: center;
     justify-content: space-between;

    &:hover{
        color: rgb(194, 213, 212);

        .link{
             color: rgb(194, 213, 212);
        }
    }

    .link{
        padding: 0 .3rem;
        font-weight: 500;
        letter-spacing: 1px;
        text-decoration: none;
        color: white;
    }
}
</style>