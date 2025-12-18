<script>
export default{
    name: 'CardSlide',
    props:{
        name:{
            type: String,
            default: 'Test'
        },
        text:{
            type: String,
            default: 'К сожалениюд никто ещё не оставил отзыв, вы можете быть первым!!'
        },
    }
}
</script>
<template>
    <div class="card_box">
        <p>{{ $props.text}}</p>
        <h3>{{ $props.name }}</h3>
        <img src="../img/,,.svg" alt=",,">
    </div>
</template>
<style scoped>
.card_box{
    width: 626px;
    height: 350px;
    position: relative;
    display: flex;
    flex-direction: column;
    border-radius: 16px;
    background-color: #F9FAFB;
    margin-right: 24px;
}
img{
    width: 75px;
    height: 75px;
    position: absolute;
    bottom: 43px;
    right: 16px;
}
h3{
    font-size: 24px;
    font-weight: 300;
    margin-bottom: 32px;
    margin-left: 43px;
    color: #6B7280;
}
p{
    font-size: 24px;
    font-weight: 700;
    text-wrap: wrap;
    margin-top: 32px;
    margin-left: 43px;
}
@media (min-width: 1024px) and (max-width: 1536px) {
    .card_box{
        width: 396px;
    }
    p{
        width: 360px;
    }
}
</style>