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
    <header class="full">
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
    <header class="burger">
        <div class="burger_head_top_box">
            <Logo></Logo>
            <div>
                <p class="burger_head_top_box_phone_number">+7 (800) 123 45-67</p>
                <div class="burger_head_top_box_burger">
                    <div class="burger_head_top_box_burger_line"></div>
                    <div class="burger_head_top_box_burger_line"></div>
                    <div class="burger_head_top_box_burger_line"></div>
                </div>
            </div>
        </div>
        <div id="active_box_burger">
            <div>
                <div class="burger_head_second_box_text_box_line"></div>
                <div class="burger_head_second_box_button_box">
                    <ButtonHead :text="'Калькулятор'" :isActive="true"></ButtonHead>
                    <ButtonHead :text="'О нас'" :isActive="false"></ButtonHead>
                    <ButtonHead :text="'Гарантия'" :isActive="false"></ButtonHead>
                    <ButtonHead :text="'Отзывы'" :isActive="false"></ButtonHead>
                    <Button :width="'width: 196px;'" class="burger_head_second_box_button" :text="'Оставить заявку'"></Button>   
                </div>
                <div class="burger_head_second_box_text_box_line"></div>
            </div>
            <div class="burger_head_last_box">
                <p>Доставляем товары из заграницы в Россию</p>
                <p>Стоимость от 550 рублей за заказ</p>
                <p>1 $ = 93 ₽ | 1 € = 99 ₽ | 1 ¥ = 13 ₽</p>
            </div>
        </div>
    </header>
</template>
<style scoped>
.full{
    width: 1536px;
    padding: 24px;
    display: flex;
    justify-content: space-between;
}
.burger{
    display: none;
    flex-direction: column;
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
.burger_head_top_box{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin: 24px;
}
.burger_head_top_box div{
    display: flex;
    align-items: center;
}
.burger_head_top_box_phone_number{
    font-size: 20px;
    font-weight: 900;
    margin-right: 24px;
}
.burger_head_top_box_burger{
    display: flex;
    flex-direction: column;
}
.burger_head_top_box_burger_line{
    width: 24px;
    height: 4px;
    border-radius: 4px;
    background-color: #A78BFA;
    margin: 1px;
}
.burger_head_second_box_text_box_line{
    width: 640px;
    height: 2px;
    background-color: #A78BFA;
    margin-top: 15px;
    border-radius: 4px;
}
.burger_head_second_box_button_box{
    display: flex;
}
.burger_head_second_box_button{
    margin: 15px 0 0 0;
}
.burger_head_last_box{
    display: flex;
    justify-content: space-between;
}
.burger_head_last_box p{
    width: 180px;
    text-align: center;
}
#active_box_burger{
    display: none;
}
@media (min-width: 1024px) and (max-width: 1536px) {
    .full{
        width: 100%;
    }
}
@media (max-width: 1024px) {
    .burger{
        display: flex;
    }
    .full{
        display: none;
    }
}
</style>
