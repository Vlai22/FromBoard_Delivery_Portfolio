<script>
import Header from './components/Header.vue';
import Calculator from './components/Calculator.vue';
import CardAdvent from './components/CardAdvent.vue';
import Button from './components/UI/Button.vue';
import CardDevis from './components/CardDevis.vue';
import Slider from './components/Slider.vue';
import Input from './components/UI/Input.vue';
import Logo from './components/UI/Logo.vue';
import ButtonHead from './components/UI/ButtonHead.vue';
export default{
  components:{
    Header, Calculator, CardDevis, CardAdvent, Button, Slider, Input, Logo, ButtonHead
  },
  data(){
    return{
      devis:[
        {
          id: 1,
          img: 'devis_1.png',
          title: 'Свидетельство о регистрации в РФ'
        },
        {
          id: 2,
          img: 'devis_2.png',
          title: 'Свидетельство о регистрации в США'
        },
        {
          id: 3,
          img: 'devis_3.png',
          title: 'Свидетельство о регистрации в Китае'
        },
        {
          id: 4,
          img: 'devis_4.png',
          title: 'Свидетельство о регистрации в Великобритании'
        },
      ],
      review:[
        {
          id: 1,
          text: 'Я заказала последний iPhone из США через ваш сервис, и доставка прошла быстро и без каких‑либо проблем. Гарантии качества и надёжная упаковка сделали мой опыт покупки невероятно позитивным',
          name: 'Анна'
        },
        {
          id: 2,
          text: 'Я уже несколько лет заказываю дизайнерскую одежду из Франции через ваш сервис, и он никогда меня не подводил. Важно иметь надежную компанию, которая позаботится о вашем заказе и предоставит все необходимые документы для ввоза в Россию',
          name: 'Ольга'
        },
        {
          id: 3,
          text: 'Я заказал редкий антикварный предмет из Японии через ваш сервис, и остался впечатлен. Все пришло в отличном состоянии, и ваша гарантия качества действительно работает. Спасибо за ваше профессиональное обслуживание',
          name: 'Дмитрий'
        },
        {
          id: 4,
          text: 'Ваш сервис действительно изменил мой способ покупок. Я больше не переживаю о таможенных вопросах и документах - все у вас в порядке. Спасибо за ваше качество и надежность',
          name: 'Екатерина'
        },
        {
          id: 5,
          text: 'Заказал шикарные часы из Швейцарии, и доставка была невероятно быстрой. Ваш сервис делает интернет-шоппинг более доступным и удобным',
          name: 'Игорь'
        },
        {
          id: 6,
          text: 'Я уже несколько лет заказываю дизайнерскую одежду из Франции через ваш сервис, и он никогда меня не подводил. Важно иметь надёжную компанию, которая позаботится о вашем заказе и предоставит все необходимые документы для ввоза в Россию',
          name: 'Алексей'
        },

      ]
    }
  }
}
</script>

<template>
  <Header></Header>
  <main>
        <section class="section_1">
            <div>
                <h1 class="section_1_h1">Без проблемная доставка купленных вещей из США, Европы и Азии в Россию</h1>
                <p class="section_1_p">Сэкономьте на покупках и наслаждайтесь мировыми брендами — наш сервис позволяет вам легко и удобно заказывать товары со всего мира и получать их в России</p>
                <img class="section_1_img" src="../public/img_1.jpg" alt="img_1">
            </div>
            <Calculator></Calculator>
        </section>
        <section class="section_2">
          <h2 class="section_2_h2">Наши преимущества</h2>
          <div class="section_2_box">
            <div>
              <CardAdvent :img="'board.svg'" :text="'Мы берём на себя все формальности и бумажную волокиту, связанную с растаможкой груза'" :title="'Растоможка груза'"></CardAdvent>
              <CardAdvent :img="'package.svg'" :text="'Все товары упаковываются нашими специалистами с особым вниманием к деталям, гарантируя, что они дойдут в безопасности и в отличном состоянии'" :title="'Надёжная упаковка'"></CardAdvent>
              <CardAdvent :img="'delivery.svg'" :text="'Мы предлагаем быструю и выгодную доставку, чтобы вы могли насладиться покупками как можно скорее.'" :title="'Быстро и выгодно'"></CardAdvent>
            </div>
            <div>
              <CardAdvent :img="'best_support.svg'" :text="'Стремимся сделать процесс доставки максимально удобным для вас, чтобы опыт остался приятным и беззаботным'" :title="'Удобный сервис'"></CardAdvent>
              <CardAdvent :img="'clear_info.svg'" :text="'Мы предоставляем полный контроль над каждым этапом доставки, от момента заказа до момента прибытия заказа'" :title="'Прозрачность работы'"></CardAdvent>
              <CardAdvent :img="'garantee.svg'" :text="'Наше страхование обеспечивает полную защиту и покрытие почти все неприятные и неожиданные ситуации'" :title="'Страхование груза'"></CardAdvent>
            </div>
          </div>
        </section>
        <section class="section_3">
            <h2>Гарантии качества</h2>
            <p>Наши гарантии качества включают в себя полный спектр документов, необходимых для ввоза и вывоза товаров, а также для успешного бизнеса на мировом рынке.<br>Мы предоставляем вам надёжность и уверенность</p>
            <div class="section_3_box">
              <CardDevis v-for="devise in $data.devis" :key="devise.id" :img="devise.img" :title="devise.title"></CardDevis>
            </div>
            <Button :width="'whidth: 259px;'" :text="'Показать больше документов'"></Button>
        </section>
        <section class="section_4">
          <h2>Отзывы</h2>
          <Slider :slider_name="'Slider_Reviews'" :slides="review"></Slider>
        </section>
        <section class="section_5">
          <div>
            <h2>Остались вопросы?</h2>
            <div>
            <div>
              <Input style="margin: 25px 25px 0 0;" :type="'text'" :placeholder="'Имя'" :inputmode="'text'"></Input>
              <Input :placeholder="'Почта'" :type="'text'" :inputmode="'email'"></Input>
            </div>
            <div>
              <Input style="margin: 25px 25px 0 0;" :placeholder="'Телефон'" :type="'text'"  ></Input>
              <Input :placeholder="'Тема вопроса'" :type="'text'" :inputmode="'text'"></Input>
            </div>
            <Input :height="'height: 150px'" :width="'width: 497px;'" :placeholder="'Сообщение...'" :type="'text'" :inputmode="'text'" ></Input>
            </div>
            <Button style="margin: 20px 0 64px 0;" :text="'Оставить заявку'" :width="'width: 492px;'"></Button>
          </div>
        </section>
  </main>
  <footer>
      <div class="footer_box_nav">
        <div>
          <Logo></Logo>
          <p>2023 © Ни одно право не защищено, копируйте сколько влезет</p>
        </div>
        <div class="footer_box_nav_a_box">
          <ButtonHead :text="'Калькулятор'"></ButtonHead>
          <ButtonHead :text="'О нас'"></ButtonHead>
          <ButtonHead :text="'Гарантии'"></ButtonHead>
          <ButtonHead :text="'Отзывы'"></ButtonHead>
        </div>
        <div class="footer_box_nav_phone_box">
          <h2>+7 (800) 123 45-67</h2>
          <p>Звонки по России бесплатны</p>
        </div>
      </div>
      <div class="footer_box_info">
        <p>НЕ ЯВЛЯЕТСЯ ПУБЛИЧНОЙ ОФЕРТОЙ. Просим обратить внимание на то, что цены носят информационный и ознакомительный характер, а значит ни в какой мере не являются публичной офертой, которая определена в ст. 437 ГК РФ. Вся информация на сайте может содержать неточности, орфографические и иные ошибки, она не является полной, окончательно и исчерпывающей</p>
        <h5 class="footer_box_info_artist">Разработкой макета занимался <br> Васильев Александр | Что-то на IT’шном</h5>
      </div>
  </footer>
</template>

<style scoped>
body{
  display: flex;
  width: 100%;
  margin: 0;
  padding: 0;
  justify-content: center;
}
main{
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 72px;
  background-color: #E5E7EB;
}
section{
  display: flex;
  width: 1536px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-bottom: 50px;
}
section h1{
  width: 756px;
  text-wrap: wrap;
}
section h2{
  font-size: 30px;
  font-weight: 900;
  text-align: center;
}
section p{
  width: 756px;
  text-wrap: wrap;
  text-align: center;
  font-size: 16px;
  font-weight: 400;
}
.section_1{
  flex-direction: row;
}
.section_1_p{
  text-align: left;
}
.section_1_img{
  width: 756px;
  height: 352px;
  border-radius: 16px;
}
.section_2_box{
  display: flex;
  flex-direction: column;
}
.section_2_box div{
  display: flex;
  flex-direction: row;
}
.section_3_box{
  display: flex;
  flex-direction: row; 
}
.section_5{
  width: 1536px;
  background-color: #F9FAFB;
}
footer{
  background-color: #111827;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
.footer_box_nav{
  width: 1536px;
  display: flex;
  flex-direction: row;
  color: #F9FAFB;
  margin: 40px 0 24px 0;
  justify-content: space-between;
}
.footer_box_nav p{
  font-size: 12px;
}
.footer_box_nav a{
  font-size: 16px;
  color: #F9FAFB;
}
.footer_box_nav_a_box{
  display: flex;
  justify-content: center;
}
.footer_box_nav_phone_box h2{
  font-size: 36px;
  font-weight: 900;
  padding: 0;
  margin: 0;
}
.footer_box_nav_phone_box p{
  font-size: 24px;
  font-weight: 400;
  padding: 0;
  margin: 0;
}
.footer_box_info{
  margin: 0 0 40px 0;
  width: 1536px;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.footer_box_info p{
  color: #4B5563;
  font-size: 12px;
  font-weight: 300;
  text-wrap: wrap;
  padding: 0;
  margin: 0;
  width: 1146px;
}
.footer_box_info_artist{
  width: 242px;
  text-align: right;
  padding: 0;
  margin: 0;
  font-size: 12;
  color: #6B7280;
}
</style>
