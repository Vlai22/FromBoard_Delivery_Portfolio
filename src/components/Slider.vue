<script>
import CardSlider from './CardSlider.vue';
export default{
    name: 'Slider',
    components:{
        CardSlider
    },
    props:{
        slides:{
            type: Array,
            default: [
                {
                    id: 1,
                    name: 'Test',
                    text: 'К сожалениюд никто ещё не оставил отзыв, вы можете быть первым!!'
                }
            ]
        },
        slider_name:{
            type: String,
        }
    },
    methods:{
        moveleft(){
            let slider = document.getElementById(this.slider_name);
            let box = slider.children[1].children[0];
            let box_width = box.children[0].getBoundingClientRect().width;
            let box_length = Math.round(box.parentNode.getBoundingClientRect().width / box_width)
            let box_pos = Math.round(Math.abs(Number(box.style.marginLeft.replace('px', ''))) / box_width);
            if(Number(box.style.marginLeft.replace('px', '')) == 0){
                box.style.marginLeft = String(-1 * box_width *(this.slides.length-2) - (24*(this.slides.length-2))) + 'px';
            }else if (Number(box.style.marginLeft.replace('px', '')) <= 0){
                box.style.marginLeft = String(-1*(box_width * (box_pos - box_length))) + 'px';
            }
        },
        moveright(){
            let slider = document.getElementById(this.slider_name);
            let box = slider.children[1].children[0];
            let box_width = box.children[0].getBoundingClientRect().width + 24;
            let box_length = Math.round(box.getBoundingClientRect().width / box_width)
            let box_pos = Math.round(Math.abs(Number(box.style.marginLeft.replace('px', ''))) / box_width);
            if(Number(box.style.marginLeft.replace('px', '')) <= -1*box_width*(this.slides.length-2)){
                box.style.marginLeft = '0px';
            }else if (Number(box.style.marginLeft.replace('px', '')) >= -1*box_width*(this.slides.length-2)){
                box.style.marginLeft = String(-1*(box_width * (box_pos + box_length))) + 'px';
            }
        }
    }
}
</script>

<template>
    <div :id="slider_name" class="slider">
        <img class="slider_arrow_left" @click="moveleft()" src="../img/left_arrow.svg" alt="left_arrow">
        <div class="slider_cards_box">
            <div class="slider_cards_box_hide">
                <CardSlider v-for="slide in slides" :key="slide.id" :name="slide.name" :text="slide.text"></CardSlider>
            </div>
        </div>
        <img class="slider_arrow_right" @click="moveright()" src="../img/right_arrow.svg" alt="right_arrow">
    </div>
</template>
<style scoped>
.slider{
    width: 1536px;
    display: flex;
    align-items: center;
}
.slider img{
    width: 60px;
    height: 60px;
}
.slider_arrow_left{
    margin-left: 13px;
    margin-right: 47px;
}
.slider_arrow_right{
    margin-left: 47px;
    margin-right: 13px;
}
.slider_cards_box{
    width: 1276px;
    overflow: hidden;
    padding: 0;
}
.slider_cards_box_hide{
    padding: 0;
    display: flex;
    transition: all 1s;
}
@media (min-width: 1024px) and (max-width: 1536px) {
    .slider{
        width: 1026px;
    }
    .slider_arrow_left{
    margin-left: 10px;
    margin-right: 35px;
    }
    .slider_arrow_right{
        margin-left: 35px;
        margin-right: 10px;
    }
}
@media (max-width: 1024px) {
    .slider{
        width: 640px;
    }
    .slider_arrow_left{
        margin-left: 7px;
        margin-right: 32px;
    }
    .slider_arrow_right{
        margin-left: 32px;
        margin-right: 7px;
    }
}
</style>
