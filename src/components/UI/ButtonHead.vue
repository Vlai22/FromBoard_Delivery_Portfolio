<template>
    <a :class="{ active: isActive }">{{text}}</a>
</template>
<script>
export default{
    props:{
        text:{
            type: String,
            default: 'Link'
        },
        isActive:{
            type: Boolean,
            default: false
        }
    },

}
</script>
<style scoped>
a{
    text-decoration: none;
    font-size: 16px;  
    font-weight: 700; 
    margin: 25px 25px;
    color: black;
    border-bottom: 1px solid transparent;
}
a.active{
    color: #8B5CF6;
    border-bottom: 1px dashed #8B5CF6;
}
a:hover{
    color: #8B5CF6;
    transition: all 0.5s;
}
</style>
