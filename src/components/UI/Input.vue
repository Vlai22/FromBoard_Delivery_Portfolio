<template>
    <input  :type="type" :placeholder="placeholder" :inputmode="inputmode" :style="width + height"></input>
</template>
<script>
export default{
    props:{
        type:{
            type: String,
            default: "text"
        },
        inputmode:{
            type: String,
            default: "nameric"
        },
        placeholder:{
            type: String,
            default: "Test"
        },
        width:{
            type: String,
            default: 'width :232px;'
        },
        height:{
            type: String,
            default: 'height: 44px;'
        }
    },
}
</script>
<style scoped>
input{
    border-radius: 4px;
    border: 2px solid black;
    font-size: 16px;
    font-weight: 400;
    margin: 24px 0 0px 0px;
    padding: 0;
}
</style>
