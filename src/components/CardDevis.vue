<script>
export default{
    name: 'CardAdvent',
    props:{
        img:{
            type: String,
            default: ''
        },
        title:{
            type: String,
            default: 'Test'
        },
    }
}
</script>

<template>
    <div class="card_box">
        <img :src="img" alt="card_logo_adv">
        <h3>{{ title }}</h3>
    </div>
</template>
<style scoped>
.card_box{
    width: 366px;
    height: 407px;  
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
}
img{
    width: 246px;
    height: 375px;
    margin: 0;
}
h3{
    font-size: 18px;
    font-weight: 900;
    margin: 0;
    text-align: center;
}
</style>
