<script>
import Logo from './UI/Logo.vue';
import Button from './UI/Button.vue';
import ButtonHead from './UI/ButtonHead.vue';
export default{
    components: {
        Logo, Button, ButtonHead
    }
}
</script>

<template>
    <header>
        <div class="head_left_box">
            <Logo></Logo>
            <div>
                <ButtonHead :text="'Калькулятор'" :isActive="true"></ButtonHead>
                <ButtonHead :text="'О нас'" :isActive="false"></ButtonHead>
                <ButtonHead :text="'Гарантия'" :isActive="false"></ButtonHead>
                <ButtonHead :text="'Отзывы'" :isActive="false"></ButtonHead>
            </div>
        </div>
        <div class="head_right_box">
            <div class="head_rigth_box_text_box">
                <p class="head_rigth_box_text_box_p">Доставляем товары из заграницы в Россию<br>Стоимость от 550 рублей за заказ<br>1 $ = 93 ₽ | 1 € = 99 ₽ | 1 ¥ = 13 ₽</p>
                <div class="head_rigth_box_text_box_line"></div>
                <div class="head_rigth_box_text_box_phone_box">
                    <p class="head_rigth_box_text_box_phone_number">+7 (800) 123 45-67</p>
                    <p class="head_rigth_box_text_box_phone_text">Звонки по России бесплатны</p>  
                </div>
            </div>
            <Button :width="'width: 196px;'" class="head_right_box_button" :text="'Оставить заявку'"></Button>
        </div>
    </header>

</template>
<style scoped>
header{
    width: 1536px;
    padding: 24px;
    display: flex;
    justify-content: space-between;
}
.head_left_box{
    display: flex;
    flex-direction: column;
}
.head_right_box{
    display: flex;
    flex-direction: column;
}
.head_rigth_box_text_box{
    display: flex;
    text-align: right;
}
.head_right_box_button{
    margin-top: 25px;
    align-self: flex-end;
}
.head_rigth_box_text_box_p{
    font-size: 16px;
    font-weight: 400;   
    padding: 0;
    margin: 0;
}
.head_rigth_box_text_box_line{
    width: 2px;
    height: 76px;
    background-color: #A78BFA;
    margin: 0px 15px;
}
.head_rigth_box_text_box_phone_number{
    font-size: 40px;
    font-weight: 900;   
    padding: 0;
    margin: 0;
}
.head_rigth_box_text_box_phone_text{
    font-size: 20px;  
    font-weight: 300;
    padding: 0;
    margin: 0;
}
@media (min-width: 1024px) and (max-width: 1536px) {
    header{
        width: 100%;
    }
}
</style>
