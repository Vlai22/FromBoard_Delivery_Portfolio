<script>
export default{
    name: 'CardAdvent',
    props:{
        img:{
            type: String,
            default: '/board.svg'
        },
        title:{
            type: String,
            default: 'Test'
        },
        text:{
            type: String,
            default: 'test'
        }
    }
}
</script>

<template>
    <div class="card_box">
        <img :src="img" alt="card_logo_adv">
        <div>
            <h3>{{ title }}</h3>
            <p>{{ text }}</p>
        </div>
    </div>
</template>
<style scoped>
.card_box{
    width: 372px;
    height: 140px;
    padding: 24px;   
    display: flex;
}
img{
    width: 136px;
    height: 136px;
    margin: 0 24px 0 0;
}
h3{
    font-size: 24px;
    font-weight: 900;
    margin: 0;
}
p{
    font-size: 14px;
    font-weight: 400;
    width: 300px;
    text-wrap: wrap;
    margin: 5px 0 0 0;
}
</style>
