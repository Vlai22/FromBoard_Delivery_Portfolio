<script>
import Button from './UI/Button.vue';
import Input from './UI/Input.vue';
export default{
    components: {
        Button, Input
    }
}
</script>

<template>
    <div class="claculator_box">
        <h2>Калькулятор доставка</h2>
        <p>Посчитайте, сколько будет стоить перевозка покупки из зарубежа</p>
        <Input :width="'width: 492px;'" :inputmode="'name'" :placeholder="'Имя'"></Input>
        <div>
            <div>
                <Input style="margin: 25px 25px 0 0;" :inputmode="'name'" :placeholder="'Почта'"></Input>
                <Input :inputmode="'name'" :placeholder="'Телефон'"></Input>
            </div>
            <div>
                <Input style="margin: 25px 25px 0 0;" :inputmode="'name'" :placeholder="'Общая площадь, м²'"></Input>
                <Input :inputmode="'name'" :placeholder="'Вес, кг'"></Input>
            </div>
            <div>
                <Input style="margin: 25px 25px 0 0;" :inputmode="'name'" :placeholder="'Страна покупки'"></Input>
                <Input :inputmode="'name'" :placeholder="'Город покупки'"></Input>
            </div>
            <div>
                <Input style="margin: 25px 25px 0 0;" :inputmode="'name'" :placeholder="'Область доставки'"></Input>
                <Input :inputmode="'name'" :placeholder="'Город'"></Input>
            </div>
        </div>
        <Button :text="'Заказать расчёт'" :width="'width: 496px;'"></Button>
    </div>
</template>
<style scoped>
.claculator_box{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 756px;
    height: 584px;
    padding: 24px 27px;
}   
h2{
    font-size: 30px;
    font-weight: 700;
    text-align: center;
    margin: 0;
}
p{
    width: 358px;
    font-size: 16px;
    font-weight: 700;
    text-align: center;
    text-wrap: wrap;
    margin: 0 0 0 0;
} 
</style>
