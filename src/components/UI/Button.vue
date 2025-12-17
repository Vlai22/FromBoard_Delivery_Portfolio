<template>
    <button :style="width + height">{{ text }}</button>
</template>
<script>
export default{
    props:{
        text:{
            type: String,
            default: "Clock Here!"
        },        
        width:{
            type: String,
            default: 'width :496px;'
        },
        height:{
            type: String,
            default: 'height: 44px;'
        }
    },
}
</script>
<style scoped>
button{
    padding: 10px 28px;
    margin-top: 25px;
    border-radius: 5px;
    background-color: #8B5CF6;
    color: white;
    outline: none;
    border: none;
    font-size: 16px;
    transition: all 0.5s;
}
button:hover{
    background-color: #6D28D9;
}
</style>
